local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/SaveManager.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()

local Window = Fluent:CreateWindow("Auto Farm Script", Enum.KeyCode.RightControl)

local MainTab = Window:CreateTab("Main", Enum.KeyCode.F)

local AutoFarmSection = MainTab:CreateSection("Auto Farm", "Vertical")

local AutoFarmEnabled = false
local AutoShakeEnabled = false
local AutoReelEnabled = false

AutoFarmSection:CreateToggle("Enable Auto Farm", false, function(state)
    AutoFarmEnabled = state
    if AutoFarmEnabled then
        -- Add Auto Farm code here
    else
        -- Stop Auto Farm
    end
end)

AutoFarmSection:CreateToggle("Enable Auto Shake", false, function(state)
    AutoShakeEnabled = state
    if AutoShakeEnabled then
        -- Add Auto Shake code here
    else
        -- Stop Auto Shake
    end
end)

AutoFarmSection:CreateToggle("Enable Auto Reel", false, function(state)
    AutoReelEnabled = state
    if AutoReelEnabled then
        -- Add Auto Reel code here
    else
        -- Stop Auto Reel
    end
end)

game:GetService("RunService").Heartbeat:Connect(function()
    if AutoFarmEnabled then
        -- Code for Auto Farm
    end
    
    if AutoShakeEnabled then
        -- Code for Auto Shake
    end
    
    if AutoReelEnabled then
        -- Code for Auto Reel
    end
end)
