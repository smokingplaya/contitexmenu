# Contitex Menu v1
Contitex Menu - is a new way to create your own Context Menu.

### How do I create my own button?
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

### How do I create spacer?
```
ContitexMenu:New()
  :SetButton(false)
  :SetSpacer(true)
  :SetVisible(function()
    return LocalPlayer():isMayor()
  end)
```
