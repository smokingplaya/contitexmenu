# Contitex Menu v1.2
Contitex Menu - is a new way to create your own Context Menu.
We create buttons and other objects using meta-tables, which makes the code more beautiful and interesting, as well as clearer.

Also, you can edit colors, or fonts of Context Menu on 20-25 lines.

If you wanna create object, create it on 123 line.
You also can delete already created objects.

### How to create button?
```
ContitexMenu:New()
  :SetButton(true)
  :SetName("Write there text of button")
  :SetIcon(Path to icon) -- Optional
  :SetOnClick(function() print("Sure bro, that's work") end)
  :SetVisible(function()
    return LocalPlayer():isMayor()
  end)
```

### How to create spacer?
```
ContitexMenu:New()
  :SetSpacer(true)
  :SetVisible(function()
    return LocalPlayer():isMayor()
  end)
```

### How to create SubMenu?
```
ContitexMenu:New()
    :SetSubMenu(true)
    :SetName("Write there text of group")
    :SetIcon(Path to icon)
    :SetSubMenuTable({
        [(Key; may be int, or string, and if key is a string, key = icon] = "Write there text of button" -- Key = path to icon, value = text
    })
    :SetOnClick(function(text) print("Sure bro, that's work. Text: " .. text) end)
    :SetVisible(function()
        return LocalPlayer():isMayor()
    end)
```
