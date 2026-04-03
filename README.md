local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local TextButtonFarm = Instance.new("TextButton")
local TextButtonSpeed = Instance.new("TextButton")

-- GUI setup
ScreenGui.Parent = game.CoreGui
Frame.Parent = ScreenGui
Frame.Size = UDim2.new(0, 200, 0, 150)
Frame.Position = UDim2.new(0.1, 0, 0.1, 0)
Frame.BackgroundColor3 = Color3.fromRGB(30,30,30)

-- Botão Auto Farm
TextButtonFarm.Parent = Frame
TextButtonFarm.Size = UDim2.new(1, 0, 0.5, 0)
TextButtonFarm.Text = "Auto Farm"

-- Botão Speed
TextButtonSpeed.Parent = Frame
TextButtonSpeed.Position = UDim2.new(0,0,0.5,0)
TextButtonSpeed.Size = UDim2.new(1, 0, 0.5, 0)
TextButtonSpeed.Text = "Speed Boost"

local farming = false

TextButtonFarm.MouseButton1Click:Connect(function()
    farming = not farming
    while farming do
        wait(1)
        print("Farmando mobs... (exemplo)")
        -- Aqui você colocaria lógica de ataque automático
    end
end)

TextButtonSpeed.MouseButton1Click:Connect(function()
    local player = game.Players.LocalPlayer
    if player.Character then
        player.Character.Humanoid.WalkSpeed = 50
    end
end)
