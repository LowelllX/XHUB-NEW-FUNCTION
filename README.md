-- โหลด Fluent UI Framework
local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/SaveManager.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()

-- สร้างหน้าต่าง UI
local Window = Fluent:CreateWindow("Auto Farm Script", Enum.KeyCode.RightControl)

-- สร้างแท็บหลักที่มี Auto Farm
local MainTab = Window:CreateTab("Main", Enum.KeyCode.F)

-- สร้าง Section สำหรับ Auto Farm
local AutoFarmSection = MainTab:CreateSection("Auto Farm", "Vertical")

-- ตัวแปรที่ใช้ในการเปิด-ปิดฟังก์ชัน
local AutoFarmEnabled = false
local AutoShakeEnabled = false
local AutoReelEnabled = false

-- สร้าง Toggle สำหรับ Auto Farm
AutoFarmSection:CreateToggle("Enable Auto Farm", false, function(state)
    AutoFarmEnabled = state
    if AutoFarmEnabled then
        -- เพิ่มโค้ดสำหรับ Auto Farm ที่นี่
        print("Auto Farm Enabled")
        -- ตัวอย่าง: เริ่มทำงาน Auto Farm
    else
        -- หยุดการทำงาน Auto Farm
        print("Auto Farm Disabled")
    end
end)

-- สร้าง Toggle สำหรับ Auto Shake
AutoFarmSection:CreateToggle("Enable Auto Shake", false, function(state)
    AutoShakeEnabled = state
    if AutoShakeEnabled then
        -- เพิ่มโค้ดสำหรับ Auto Shake ที่นี่
        print("Auto Shake Enabled")
        -- ตัวอย่าง: เริ่มทำงาน Auto Shake
    else
        -- หยุดการทำงาน Auto Shake
        print("Auto Shake Disabled")
    end
end)

-- สร้าง Toggle สำหรับ Auto Reel
AutoFarmSection:CreateToggle("Enable Auto Reel", false, function(state)
    AutoReelEnabled = state
    if AutoReelEnabled then
        -- เพิ่มโค้ดสำหรับ Auto Reel ที่นี่
        print("Auto Reel Enabled")
        -- ตัวอย่าง: เริ่มทำงาน Auto Reel
    else
        -- หยุดการทำงาน Auto Reel
        print("Auto Reel Disabled")
    end
end)

-- ตัวอย่างการทำงานของฟังก์ชัน Auto Farm (แค่เป็นโค้ดพื้นฐาน)
game:GetService("RunService").Heartbeat:Connect(function()
    if AutoFarmEnabled then
        -- โค้ดที่ต้องการให้ทำเมื่อเปิด Auto Farm
        -- เช่น ไปหาวัตถุหรือทำฟาร์มอัตโนมัติ
    end
    
    if AutoShakeEnabled then
        -- โค้ดที่ต้องการให้ทำเมื่อเปิด Auto Shake
        -- เช่น สั่นเครื่องมือหรือกิจกรรมต่าง ๆ
    end
    
    if AutoReelEnabled then
        -- โค้ดที่ต้องการให้ทำเมื่อเปิด Auto Reel
        -- เช่น หมุน Reel หรือทำการหมุนต่าง ๆ
    end
end)
