#local Players = game:GetService("Players")
local player = Players.LocalPlayer

local gui = Instance.new("ScreenGui")
gui.Name = "SA_HUB"
gui.Parent = player.PlayerGui

local frame = Instance.new("Frame")
frame.Size = UDim2.fromOffset(260, 300)
frame.Position = UDim2.new(0.5, -130, 0.5, -150)
frame.BackgroundColor3 = Color3.fromRGB(15, 15, 20)
frame.Parent = gui

Instance.new("UICorner", frame).CornerRadius =
    UDim.new(0, 12)

local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 50)
title.BackgroundTransparency = 1
title.Text = "SA HUB"
title.TextColor3 = Color3.fromRGB(180, 80, 255)
title.TextSize = 26
title.Font = Enum.Font.GothamBold
title.Parent = frame

local function button(name, y)
    local b = Instance.new("TextButton")
    b.Size = UDim2.new(0.85, 0, 0, 40)
    b.Position = UDim2.new(0.075, 0, 0, y)
    b.BackgroundColor3 = Color3.fromRGB(75, 35, 110)
    b.TextColor3 = Color3.new(1,1,1)
    b.Text = name
    b.TextSize = 14
    b.Font = Enum.Font.GothamBold
    b.Parent = frame
    Instance.new("UICorner", b)
    return b
end

button("BEST BRAINROT", 65)
button("XRAY BASE", 115)
button("INVISIBLE 90%", 165)
button("BRAINROT ESP", 215)

print("SA HUB carregado!")
