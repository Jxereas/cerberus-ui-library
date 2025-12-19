# Cerberus UI

Cerberus UI is a lightweight Roblox UI library designed for building clean, modular in-game interfaces using tabs, sections, and common UI components.

---

## Features

- Window system with optional screen boundary locking
- Tab and section-based layout
- Common UI components including:
  - Titles and labels
  - Buttons and toggles
  - Dropdowns and search bars
  - Sliders
  - Keybinds
  - Text boxes
  - Color wheel picker
- Simple callback-based interaction model
- Designed for client-side use

---

## Installation

Load the library directly using `loadstring`:

```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Jxereas/cerberus-ui/main/cerberus.lua"))()
```

---

## Basic Usage

```lua
local window = Library.new("Cerberus UI")
window:LockScreenBoundaries(true)

local tab = window:Tab("Main")
local section = tab:Section("Example")

section:Button("Click Me", function()
    print("Button pressed")
end)
```

---

## Documentation
Full usage examples and API documentation can be found here:

[Cerberus UI Library Documentation](DOCUMENTATION.md)

---

## License
This project is licensed under the MIT License.
See the [LICENSE](LICENSE) file for details.
