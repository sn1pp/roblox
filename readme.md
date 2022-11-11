# Roblox explorer icons for developers

## Prepairing:
 - **Classes**: ImageLabel / ImageButton
 - **Image ID**: rbxasset://textures//ClassImages.png
 - **ImageRectSize**: 16x16

## Code
```lua
local function getClassIconOffsetX(class)
  return game:GetService("HttpService"):JSONDecode(
    game:GetService("HttpService"):RequestAsync{
      Url = "https://raw.githubusercontent.com/sn1pp/roblox/main/icons-dump.json",
      Method = "GET"
    }.Body
  )[class]
end

print(getClassIconOffset("Model"))
```

**Made by sn1p**
