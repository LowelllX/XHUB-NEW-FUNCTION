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
     
    else
   
    end
end)

AutoFarmSection:CreateToggle("Enable Auto Shake", false, function(state)
    AutoShakeEnabled = state
    if AutoShakeEnabled then
       
    else
        
    end
end)

AutoFarmSection:CreateToggle("Enable Auto Reel", false, function(state)
    AutoReelEnabled = state
    if AutoReelEnabled then
        
    else
        
    end
end)

game:GetService("RunService").Heartbeat:Connect(function()
    if AutoFarmEnabled then
        
    end
    
    if AutoShakeEnabled then
    end
    if AutoReelEnabled then
    end

    elseif CastMode == "Blatant" then
        local rod = LocalCharacter and LocalCharacter:FindFirstChildOfClass("Tool")
        if rod and rod:FindFirstChild("values") and string.find(rod.Name, "Rod") then
            task.wait(0.1)
            local Random = math.random(90, 99)
            rod.events.cast:FireServer(Random)
        end
    end
end)
