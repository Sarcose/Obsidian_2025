

categories:

tools, resources, plants, organization
### List with rough prices & priority
*priority: low, med, high*
*prices: price/10, with 100 clamping at 0.9 and higher being set at 1*

##### Tool
- Cardboard: free
- Grow Containers (pots, grow bags, 5 gallon buckets): $10-20
- Hoe: $15-20
- Garden gloves: $10
- Wheelbarrow: $80
- Garden Cart: $50
- Thermometer: $10
- Thermometer w/moisture meter: $35
- Spray Nozzle: $10
- Lamp: $25
- Heated mat: $15~
- Jeans: $20
- Tiller: expensive
- Clippers: $8
- Straw hat: $10
- Garden Rake: $20
##### Resource
- Landscape Fabric: $20
- Labels: $15
- Dowels/Stakes: $10
##### Plant
- Seed budget: $40
##### Organizing
- Something for a worktable in the lower storage room
##### Soil
- Straw Mulch
- Soil mix:
	- Hardwood Mulch - 1 bag (medium priority) $20
	- Leaf Bagged Product -  2 bags (higher priority) $40
	- Peat Moss - 1 bag (higher priority) $20
	- Pearlite - small amount (lower priority) $10

### Sorted by price vs priority

```mermaid

%%{init: {"quadrantChart": {
	"chartWidth": 200, "chartHeight": 150, "pointLabelFontSize":10}

}}%%
quadrantChart
	classDef label color: #109060, radius: 0
	classDef tool color: #964B00, radius: 5
	classDef resource color: #000000, radius: 5
	classDef plant color: #4E9C35, radius: 5
	classDef organization color: #9155C5, radius: 5
	classDef soil color: #A52A2A, radius: 5

	Key:::label: [0.06, 1]
	Tool:::label: [0.1, 0.9]
	Resource:::label: [0.165, 0.8]
	Plant:::label: [0.11, 0.7]
	Organizing:::label: [0.18, 0.6]
	Soil:::label: [0.09, 0.5]
	.:::soil:[0.4,0.43]
	.:::organization:[0.4,0.53]
	.:::plant:[0.4,0.63]
	.:::resource:[0.4,0.73]
	.:::tool:[0.4,0.83]
```

```mermaid

%%{init: {"quadrantChart": {
	"chartWidth": 800, "chartHeight": 800}, "themeVariables": {"quadrant1TextFill": "#ff0000"} 

}}%%
quadrantChart
	title Priority vs Price
	classDef label color: #109060, radius: 0
	Low:::label: [0.5, 0.02] 
	High:::label: [0.5, 1] 
	Cheap:::label: [0.025, 0.515]
	Pricey:::label: [0.975, 0.515]

	classDef tool color: #964B00, radius: 5
	classDef resource color: #000000, radius: 5
	classDef plant color: #4E9C35, radius: 5
	classDef organization color: #9155C5, radius: 5
	classDef soil color: #A52A2A, radius: 5

	
	

	Spray Nozzle $10:::tool:[0.1,0.9]
	Hoe $15-20:::tool: [0.15, 0.87]
	Jeans $20:::tool:[0.20, 0.76]
	Thermometer $10:::tool:[0.13, 0.73]
	Thermometer w/moisture meter $35:::tool:[0.35, 0.73]
	Pots $10-20:::tool: [0.15, 0.7]
	Tiller $$:::tool:[0.97,0.7]
	Wheelbarrow $80:::soil:[0.8,0.6]
	Garden Cart $15:::soil:[0.5,0.6]
	Lamp $25:::tool:[0.26,0.46]
	Heat Mat $15-20:::tool:[0.15,0.3]
	Clippers $8:::tool:[0.08,0.55]
	Straw Hat $10:::tool:[0.1,0.5]
	Garden Rake $20:::tool:[0.21,0.5]
	Gloves $10-20:::tool:[0.17, 0.23]

	Landscape Fabric $15:::resource:[0.2,0.67]
	Metal Labels $15:::resource:[0.15,0.35]
	Dowels $10:::resource:[0.1,0.4]

	Seed budget $40:::plant: [0.4, 0.95]

	Straw Mulch $20:::soil:[0.2,0.8]
	Soil Mix $80:::soil:[0.8,0.8]
	Pearlite $10:::soil:[0.1,0.15]
```


