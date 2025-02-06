This is for using a personal Obsidian vault separately from my work vault, and backing it up automatically. The basic idea is this:

- [[#Todo List:|Todo List:]]
- [[#What's Next:|What's Next:]]

### Todo List:

- [x] Use a github repo
- [x] Correctly get the push workflow working
- [ ] Automate pushing
- [ ] Protection -- currently discards and rebases to remove things like "cursor position" -- this can be dangerous. Need to know not to press htokey when it's already open. 


### Workflow So Far
- Open vault with pull script
- Close vault with push script

**macOS**: 
- ⌃⌘⌥P    :   KBM open personal vault -- pull fresh from repo, open using Obsidian URI
- ⌃⌘⌥S    :   KBM save and close personal vault -- push commit and use ⌘⇧W to close
**Windows**
- pull_vault.bat     :   Bat file to pull the vault and open using Obsidian URI
- push_vault.bat   : Bat file to push the vault. Does not yet close the Window.

### What's Next:

- Autohotkey on Windows to call `pull_vault.bat` and `push_vault.bat`
	- In said autohotkey script, close the Obsidian program altogether (a bit easier on Windows since we don't run multiple vaults there)
- Research what hotkeys I **truly** use on Obsidian, put them together equivalently in Windows and create the AHK hint bubble for it