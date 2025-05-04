```lua
-- Spaceplane.lua
local Class = require("classic")

local Spaceplane = Class:extend()

function Spaceplane:new(ownerSpace, drawDistance)
    self.ownerSpace = ownerSpace -- The space that owns this spaceplane
    self.spaces = {} -- List of { space = Space, position = {x, y, z}, rotation = radians }
    self.drawDistance = drawDistance or 1000 -- Configurable max draw distance
    self.projection = "flat" -- Or "fisheye", "bubble", etc.
end

function Spaceplane:addSpace(space, position, rotation)
    table.insert(self.spaces, {
        space = space,
        position = position or { x = 0, y = 0, z = 0 },
        rotation = rotation or 0
    })
end

function Spaceplane:update(dt)
    for _, entry in ipairs(self.spaces) do
        if not entry.space.hibernating then
            entry.space:update(dt)
        end
    end
end

function Spaceplane:draw()
    for _, entry in ipairs(self.spaces) do
        local space = entry.space
        local pos = entry.position
        local rot = entry.rotation

        -- Distance check
        local dx = pos.x
        local dy = pos.y
        local dz = pos.z
        local distance = math.sqrt(dx * dx + dy * dy + dz * dz)
        if distance <= self.drawDistance then

            -- Optional projection transforms
            local drawX, drawY = pos.x, pos.y
            if self.projection == "fisheye" then
                local distortion = 1 + 0.003 * distance^2
                drawX = pos.x * distortion
                drawY = pos.y * distortion
            elseif self.projection == "bubble" then
                local angle = math.atan2(pos.y, pos.x)
                local radius = math.sqrt(pos.x^2 + pos.y^2)
                local warpedRadius = radius * radius / 256
                drawX = math.cos(angle) * warpedRadius
                drawY = math.sin(angle) * warpedRadius
            end

            love.graphics.push()
            love.graphics.translate(drawX, drawY)
            love.graphics.rotate(rot)
            love.graphics.draw(space.canvas, 0, 0, 0, 1, 1, space.canvas:getWidth()/2, space.canvas:getHeight()/2)
            love.graphics.pop()
        end
    end
end

-- Messaging Helpers
function Spaceplane:getSpaces()
    local result = {}
    for _, entry in ipairs(self.spaces) do
        table.insert(result, entry.space)
    end
    return result
end

function Spaceplane:getContainedSpacesOf(space)
    local result = {}
    for _, entry in ipairs(self.spaces) do
        if entry.space == space then
            table.insert(result, entry.space)
        end
    end
    return result
end

function Spaceplane:getOwnerSpace()
    return self.ownerSpace
end

return Spaceplane
