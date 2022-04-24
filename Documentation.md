# Orion Library
This documentation is for the stable release of Orion Library.

## Booting the Library
```lua
local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
```

## Creating a Window
```lua
local Window = OrionLib:MakeWindow({Name = "Title of the library"})
```

## Creating a Tab
```lua
local Tab = Window:MakeTab({
	Name = "Tab 1",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
```


## Notifying the user
```lua
OrionLib:MakeNotification({
	Name = "Title!",
	Content = "Notification content... what will it say??",
	Image = "rbxassetid://4483345998",
	Time = 5
})
```

## Creating a Button
```lua
Tab:AddButton({
	Name = "Button!",
	Callback = function()
      	print("button pressed")
  	end    
})
```

## Creating a Checkbox toggle
```lua
Tab:AddToggle({
	Name = "This is a toggle!",
	Default = false,
	Callback = function(Value)
		print(Value)
	end    
})
```

## Creating a Color Picker
```lua
Tab:AddColorpicker({
	Name = "Colorpicker",
	Default = Color3.fromRGB(255, 0, 0),
	Callback = function(Value)
		print(Value)
	end	  
})
```
### Setting the color picker's value
```lua
ColorPicker:Set(Color3.fromRGB(255,255,255))
```

## Creating a Slider
```lua
Tab:AddSlider({
	Name = "Slider",
	Min = 0,
	Max = 20,
	Default = 5,
	Increment = 1,
	ValueName = "bananas",
	Callback = function(Value)
		print(Value)
	end    
})
```
### Change Slider Value
```lua
Slider:Set(2)
```
Make sure you make your slider a variable (local CoolSlider = Tab:AddSlider...) for this to work.

## Creating a Label
```lua
Tab:AddLabel("Label")
```
## Changing an existing label
```lua
CoolLabel:Set("Label New!")
```

## Creating a Paragraph
```lua
Tab:AddParagraph("Paragraph","Paragraph Content")
```
## Changing an existing paragraph
```lua
CoolParagraph:Set("Paragraph New!")
```

## Creating an Adaptive Input
```lua
Tab:AddTextbox({
	Name = "Textbox",
	Default = "default box input",
	TextDisappear = true,
	Callback = function(Value)
		print(Value)
	end	  
})
```

## Creating a Keybind
```lua
Tab:AddBind({
	Name = "Bind",
	Default = Enum.KeyCode.E,
	Callback = function()
		print("press")
	end    
})
```
### Selecting a bind
```lua
Bind:Set(Enum.KeyCode.E)
```

## Creating a Dropdown menu
```lua
Tab:AddDropdown({
	Name = "Dropdown",
	Default = "1",
	Options = {"1", "2"},
	Callback = function(Value)
		print(Value)
	end    
})
```
### Adding a set of new Dropdown buttons to an existing menu
```lua
Dropdown:Refresh(List<table>,true)
```
The above boolean value "true" is whether or not the current buttons will be deleted.
### Selecting a dropdown option
```lua
Dropdown:Set("dropdown option")
```

## Destroying the Interface
```lua
OrionLib:Destroy()
```
