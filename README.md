
local kavoUi = loadstring(game:HttpGet("https://pastebin.com/raw/vff1bQ9F"))()
local window = kavoUi.CreateLib("Goose hub v1","BloodTheme")

---Tabs

local Tab1 = window:NewTab("Main")
local Tab1Section = Tab1:NewSection("Main")
local Tab2 = window:NewTab("Tools")
local Tab2Section = Tab2:NewSection("Tools")
local Tab3 = window:NewTab("Credits")
local Tab3Section = Tab3:NewSection("Made By Johnny 2.0")
local Tab3Section = Tab3:NewSection("Subscribe To Orange cat gamer 6969"On Youtube")

---Buttons

Tab1Section:NewButton("Fly","Loads Fly Script",function()
loadstring(game:HttpGet('https://pastebin.com/raw/YSL3xKYU'))()
end)

Tab1Section:NewButton("Hitbox","Increase Range",function()
_G.HeadSize = 25
_G.Disabled = true

game:GetService('RunService').RenderStepped:connect(function()
if _G.Disabled then
for i,v in next, game:GetService('Players'):GetPlayers() do
if v.Name ~= game:GetService('Players').LocalPlayer.Name then
pcall(function()
v.Character.HumanoidRootPart.Size = Vector3.new(_G.HeadSize,_G.HeadSize,_G.HeadSize)
v.Character.HumanoidRootPart.Transparency = 0.7
v.Character.HumanoidRootPart.BrickColor = BrickColor.new("Really black")
v.Character.HumanoidRootPart.Material = "Neon"
v.Character.HumanoidRootPart.CanCollide = false
end)
end
end
end
end)
end)

Tab1Section:NewButton("Big Hitbox","Increase large Range",function()
_G.HeadSize = 50
_G.Disabled = true

game:GetService('RunService').RenderStepped:connect(function()
if _G.Disabled then
for i,v in next, game:GetService('Players'):GetPlayers() do
if v.Name ~= game:GetService('Players').LocalPlayer.Name then
pcall(function()
v.Character.HumanoidRootPart.Size = Vector3.new(_G.HeadSize,_G.HeadSize,_G.HeadSize)
v.Character.HumanoidRootPart.Transparency = 0.7
v.Character.HumanoidRootPart.BrickColor = BrickColor.new("Really black")
v.Character.HumanoidRootPart.Material = "Neon"
v.Character.HumanoidRootPart.CanCollide = false
end)
end
end
end
end)
end)

Tab1Section:NewToggle("Infinite Jumps"," Infinite Jumps",function()
local InfiniteJumpEnabled = true
game:GetService("UserInputService").JumpRequest:connect(function()
	if InfiniteJumpEnabled then
		game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass'Humanoid':ChangeState("Jumping")
	end
end)
end)

Tab1Section:NewButton("Speed","Increase speed",function()
function isNumber(str)
  if tonumber(str) ~= nil or str == 'inf' then
    return true
  end
end
local tspeed = 1
local hb = game:GetService("RunService").Heartbeat
local tpwalking = true
local player = game:GetService("Players")
local lplr = player.LocalPlayer
local chr = lplr.Character
local hum = chr and chr:FindFirstChildWhichIsA("Humanoid")
while tpwalking and hb:Wait() and chr and hum and hum.Parent do
  if hum.MoveDirection.Magnitude > 0 then
    if tspeed and isNumber(tspeed) then
      chr:TranslateBy(hum.MoveDirection * tonumber(tspeed))
    else
      chr:TranslateBy(hum.MoveDirection)
    end
  end
end
end)

Tab1Section:NewButton("Infinite Yeild","Loads Iy",function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
end)

Tab1Section:NewButton("Esp Antena","location",function()
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")

local function createBox()
    local box = Instance.new("BoxHandleAdornment")
    box.Size = Vector3.new(1,100, 1)
    box.Color3 = Color3.new(1,0,0)
    box.Transparency = 0.1
    box.ZIndex = 5
    return box
end

local function updateEsp(player, box)
    local character = player.Character
    if character and character:FindFirstChild("HumanoidRootPart") then
        box.Visible = true
        box.Adornee = character.HumanoidRootPart
        box.Parent = character.HumanoidRootPart
    else
        box.Visible = false
        box.Adornee = nil
        box.Parent = nil
    end
end

local function onPlayerAdded(player)
    local box = createBox()
    updateEsp(player, box)
    player.CharacterAdded:Connect(function()
        updateEsp(player, box)
    end)
    player.CharacterRemoving:Connect(function()
        updateEsp(player, box)
    end)
end

for _, player in ipairs(Players:GetPlayers()) do
    onPlayerAdded(player)
end

Players.PlayerAdded:Connect(function(player)
    onPlayerAdded(player)
end)

RunService.RenderStepped:Connect(function()
    for _, player in ipairs(Players:GetPlayers()) do
        updateEsp(player)
    end
end)
end)

Tab1Section:NewButton("Esp","location",function()
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")

local function createBox()
    local box = Instance.new("BoxHandleAdornment")
    box.Size = Vector3.new(5, 5, 2)
    box.Color3 = Color3.new(1,0,0)
    box.Transparency = 0.1
    box.ZIndex = 5
    return box
end

local function updateEsp(player, box)
    local character = player.Character
    if character and character:FindFirstChild("HumanoidRootPart") then
        box.Visible = true
        box.Adornee = character.HumanoidRootPart
        box.Parent = character.HumanoidRootPart
    else
        box.Visible = false
        box.Adornee = nil
        box.Parent = nil
    end
end

local function onPlayerAdded(player)
    local box = createBox()
    updateEsp(player, box)
    player.CharacterAdded:Connect(function()
        updateEsp(player, box)
    end)
    player.CharacterRemoving:Connect(function()
        updateEsp(player, box)
    end)
end

for _, player in ipairs(Players:GetPlayers()) do
    onPlayerAdded(player)
end

Players.PlayerAdded:Connect(function(player)
    onPlayerAdded(player)
end)

RunService.RenderStepped:Connect(function()
    for _, player in ipairs(Players:GetPlayers()) do
        updateEsp(player)
    end
end)
end)

Tab1Section:NewButton("Ping Counter","Counts Ping",function()
loadstring(game:HttpGet("https://pastebin.com/raw/MvKKJ331",true))()
end)

Tab1Section:NewButton("Fps Counter","Counts Fps",function()
loadstring(game:HttpGet("https://pastebin.com/raw/ySHJdZpb",true))()
end)

Tab2Section:NewButton("No Clip Tool","Go throw walls",function()
mouse = game.Players.LocalPlayer:GetMouse()
tool = Instance.new("Tool")
tool.RequiresHandle = false
tool.Name = ("Equip To Noclip")
tool.Activated:Connect(function()
game.Players.LocalPlayer.Character.Humanoid.MaxHealth = math.huge
game.Players.LocalPlayer.Character.Humanoid.Health = math.huge
while true do
		game:GetService("RunService").Stepped:wait()
		game.Players.LocalPlayer.Character.Head.CanCollide = false
		game.Players.LocalPlayer.Character.Torso.CanCollide = false
end
end)
tool.Parent = game.Players.LocalPlayer.Backpack
end)

Tab2Section:NewButton("Speed Tool","fast",function()
mouse = game.Players.LocalPlayer:GetMouse()
tool = Instance.new("Tool")
tool.RequiresHandle = false
tool.Name = "Click To Speed Up"
tool.Activated:connect(function()
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 100
end)
tool.Parent = game.Players.LocalPlayer.Backpack
end)

Tab2Section:NewButton("Click to Tp","Teleport",function()
mouse = game.Players.LocalPlayer:GetMouse()
tool = Instance.new("Tool")
tool.RequiresHandle = false
tool.Name = "Equip to Click TP"
tool.Activated:connect(function()
local pos = mouse.Hit+Vector3.new(0,2.5,0)
pos = CFrame.new(pos.X,pos.Y,pos.Z)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = pos
end)
tool.Parent = game.Players.LocalPlayer.Backpack
end)

game.StarterGui:SetCore("SendNotification",  {
 Title = "Goose Hub V1";
 Text = "Made by Orangecatgamer696969. Subscribe him on youtube";
 Icon = "";
 Duration = 10;
})
