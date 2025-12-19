# Cerberus UI Documentation

A lightweight Roblox UI library designed for building clean, modular in-game interfaces with tabs, sections, and common UI components.

---

## Loading

```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Jxereas/cerberus-ui-library/refs/heads/main/cerberus.lua"))()
```

---

## Creating a Window

```lua
local window = Library.new("Window") -- Args(<string> Name, <boolean?> ConstrainToScreen)

window:LockScreenBoundaries(true) -- Args(<boolean> ConstrainToScreen)
```

---

## Tabs and Sections

```lua
local tab = window:Tab("Tab") -- Args(<string> Name, <string?> TabImage)

local section = tab:Section("Section") -- Args(<string> Name)
```

---

## Components

### Title
```lua
local title = section:Title("Title") -- Args(<string> Name)
title:ChangeText("Title") -- Args(<String> NewText)
```

### Label
```lua
local label = section:Label("Label") -- Args(<String> LabelText, <Number?> TextSize, <Color3?> TextColor)
label:ChangeText("Label") -- Args(<String> NewText, <Boolean?> PlayAnimation)
```

### Toggle
```lua
local toggle = section:Toggle("Toggle", function(bool)
   print("Toggle is: "..tostring(bool))
end) -- Args(<String> Name, <Function> Callback)
toggle:Set(false) -- Args(<Boolean> ToggleState, <Function?> Callback)
```

### Button
```lua
section:Button("Button", function()
   print("Pressed button!")
end) -- Args(<String> Name, <Function> Callback)
```

### Dropdown
```lua
local dropdown = section:Dropdown("Dropdown") -- Args(<String> Name)
dropdown:ChangeText("Dropdown") -- Args(<String> NewText)
dropdown:Toggle("Toggle") -- Dropdowns and searchbars can go inside dropdowns
```

### Slider
```lua
section:Slider("Slider", function(val)
   print("Slider Value is: "..val)
end) -- Args(<String> Name, <Function> Callback, <Number?> MaximumValue, <Number?> MinimumValue)
```

### Search Bar
```lua
local searchBar = section:SearchBar("Search...") -- Args(<String> PlaceholderText)
searchBar:Toggle("Toggle") -- Searchbars and dropdowns can go inside searchbars
```

### Keybind
```lua
section:Keybind("Keybind", function()
   print("Keybind pressed!")
end) -- Args(<String> Name, <Function> Callback, <String> DefaultKey)
```

### Textbox
```lua
section:TextBox("Textbox", function(txt)
   print("Textbox string is: "..txt)
end) -- Args(<String> Name, <Function> Callback)
```

### Color Wheel
```lua
section:ColorWheel("ColorWheel", function(color)
   print("ColorWheel color is: "..tostring(color))
end) -- Args(<String> Name, <Function> Callback)
```
