# Wally V3 Backup
<p>I did not create this UILib</p>
<p>Thanks Akia on V3rmillion for making the post</p>
<p>https://v3rmillion.net/showthread.php?tid=1040650</p>
<p>Scroll down to find directions of refreshing and global variables</p>

# Wally V3 Code
```lua
local library = loadstring(game:HttpGet(('https://raw.githubusercontent.com/GemstoneDev/Wally-V3-Backup/main/script/main.lua')))()

local w = library:CreateWindow("A") -- Creates the window

local b = w:CreateFolder("B") -- Creates the folder(U will put here your buttons,etc)

b:Label("Pretty Useless NGL",{
    TextSize = 25; -- Self Explaining
    TextColor = Color3.fromRGB(255,255,255); -- Self Explaining
    BgColor = Color3.fromRGB(69,69,69); -- Self Explaining
    
}) 

b:Button("Button",function()
    print("Skid")
end)

b:Toggle("Toggle",function(bool)
    shared.toggle = bool
    print(shared.toggle)
end)

b:Slider("Slider",{
    min = 10; -- min value of the slider
    max = 50; -- max value of the slider
    precise = true; -- max 2 decimals
},function(value)
    print(value)
end)

b:Dropdown("Dropdown",{"A","B","C"},true,function(mob) --true/false, replaces the current title "Dropdown" with the option that t
    print(mob)
end)

b:Bind("Bind",Enum.KeyCode.C,function() --Default bind
    print("Yes")
end)

b:ColorPicker("ColorPicker",Color3.fromRGB(255,0,0),function(color) --Default color
    print(color)
end)

b:Box("Box","number",function(value) -- "number" or "string"
    print(value)
end)

b:DestroyGui()

```
# How to refresh a dropdown

1. Create the dropdown as a variable
```lua
local dropdownvar = b:Dropdown("Example",table,function(contents)
    print(contents)
end)
```
2. Refrash it using the function
```lua
dropdownvar:Refresh(table)
```

# How to refresh a label
1. Create a label as a variabe
```lua
local labelvar = b:Label("Example Label",{
    TextSize = 25; 
    TextColor = Color3.fromRGB(255,255,255);
    BgColor = Color3.fromRGB(69,69,69);
})
```
2. Refresh it using the function
```lua
labelvar:Refresh("New Label Text")
```

# How to change the menu default colors
1. Find the type of item you want to change. In this case we will change the Button Color.
```lua
_G.ButtonColor
```
2. Change the color with the code below
```lua
_G.ButtonColor = Color3.fromRGB(255,255,255)
```

# Global Variables
```lua
_G.MainColor
_G.SecondaryColor
_G.TertiaryColor
_G.ArrowColor
_G.MainTextColor
_G.PointerColor
_G.ButtonTextColor
_G.SliderColor
_G.ButtonColor
_G.ToggleColor
_G.DraggerCircleColor
_G.BindColor
```
