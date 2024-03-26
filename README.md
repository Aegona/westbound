
local DrRayLibrary = loadstring(game:HttpGet("https://raw.githubusercontent.com/AZYsGithub/DrRay-UI-Library/main/DrRay.lua"))()
local window = DrRayLibrary:Load("???? Hub - Westbound - { BETA }", "Default")

local tab = DrRayLibrary.newTab("Main", "ImageIdHere")



tab.newToggle("Rob Money Farm", "Grayridge Only!!!!", true, function(toggleState)
    if toggleState then
                tp()
        _G.Test = true
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 0
    else
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 16
                _G.Test = false
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1496.59277, 120.54232, 1610.9126, -0.917180359, 6.31933901e-08, 0.398472279, 4.67873171e-08, 1, -5.08968334e-08, -0.398472279, -2.80381265e-08, -0.917180359)
 
    end
end)

tab.newButton("TP Random", "TP", function()game:GetService("ReplicatedStorage"):WaitForChild("GeneralEvents"):WaitForChild("Spawn"):FireServer()
end)

tab.newButton("Reset Character", "Change Health to 0", function()
    game.Players.LocalPlayer.Character.Humanoid.Health = 0
end)

function tp()
    local args = {
        [1] = "Grayridge",
        [2] = false,
        [3] = false
    }
    
    game:GetService("ReplicatedStorage"):WaitForChild("GeneralEvents"):WaitForChild("Spawn"):FireServer(unpack(args))    
    
    wait(2)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1496.59277, 120.54232, 1610.9126, -0.917180359, 6.31933901e-08, 0.398472279, 4.67873171e-08, 1, -5.08968334e-08, -0.398472279, -2.80381265e-08, -0.917180359)
    wait(.1)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1465.77869, 132.84996, 1642.27722, -0.149249285, 4.46420012e-10, -0.988799572, -1.94223677e-08, 1, 3.38308648e-09, 0.988799572, 1.97097521e-08, -0.149249285)
    wait(0.2)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1475.2981, 132.849579, 1670.52173, 0.997966886, 7.79490534e-08, -0.0637350082, -7.90242325e-08, 1, -1.43487107e-08, 0.0637350082, 1.93561487e-08, 0.997966886)
    wait(0.1)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1475.2981, 132.849579, 1670.52173, 0.997966886, 7.79490534e-08, -0.0637350082, -7.90242325e-08, 1, -1.43487107e-08, 0.0637350082, 1.93561487e-08, 0.997966886)
    wait(0.1)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1475.2981, 132.849579, 1670.52173, 0.997966886, 7.79490534e-08, -0.0637350082, -7.90242325e-08, 1, -1.43487107e-08, 0.0637350082, 1.93561487e-08, 0.997966886)
    wait(0.1)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1475.2981, 132.849579, 1670.52173, 0.997966886, 7.79490534e-08, -0.0637350082, -7.90242325e-08, 1, -1.43487107e-08, 0.0637350082, 1.93561487e-08, 0.997966886)
    wait(1)

end



spawn(function()
    while wait() do
        if _G.Test then

            local replicatedStorage = game:GetService("ReplicatedStorage")
            local generalEvents = replicatedStorage:WaitForChild("GeneralEvents")
            local robEvent = generalEvents:WaitForChild("Rob")
                     
            local cashRegister = workspace:WaitForChild("CashRegister")

            local args = {
                [1] = "Register",
                [2] = {
                    ["Part"] = cashRegister:WaitForChild("Union"),
                    ["Active"] = true,
                    ["ActiveValue"] = cashRegister:WaitForChild("Active"),
                    ["OpenPart"] = cashRegister:WaitForChild("Open")
                }
            }
         
            robEvent:FireServer(unpack(args))
            wait(0.1)

        end
        end
        end)
