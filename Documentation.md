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

## Creating a Label
```lua
Tab:AddLabel("Label")
```

## Creating a Paragraph
```lua
Tab:AddParagraph("Paragraph","Paragraph Content")
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

## Destroying the Interface
```lua
OrionLib:Destroy()
```
