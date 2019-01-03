# DisplayBox
FFXI Gearswap Addition

Include the file in any gearswap project, and call **text_setup()** to set up the box.

Add your own color pairs by calling **addTextColorPair(stringForText, color)**.

Best practice involves having an **updateTable()** function that is called whenever you update a required variable, like follows:

```lua
function updateTable()
    addToTable("(F10) MP Body", MPSet)
    addToTable("(F11) MB Set", MBSet)
    addToTable("(F12) Idle Set", sets.Idle.index[Idle_Index])
    addToTable("(END) Weapon Locked", weaponLocked)
    update_message()
end
```

##Available functions to call

```lua
text_setup() --Will instantiate the entire system, call first
addToTable(string, variable) --Your string to display, and the variable it relies on
addTextColorPair(string, newColor) --Your string you want to change color, and the color it should be
update_message() --Will rewrite the text box with the latest data values the system has received
print_table() --Will output all the information you've given it so far
```
