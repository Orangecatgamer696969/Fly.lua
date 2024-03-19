# Fly.lua
Fly script lol
local character = script.Parent:WaitForChild("Humanoid")
local bodyVelocity = Instance.new("BodyVelocity")
bodyVelocity.Parent = character

local function fly()
  bodyVelocity.Velocity = Vector3.new(0, 15, 0) -- Adjust speed as needed
  character.Jump = true -- Makes the jump animation play
end

local function stopFlying()
  bodyVelocity.Velocity = Vector3.new(0, 0, 0)
  character.Jump = false
end

script.Parent.KeyUp:Connect(function(key)
  if key == "w" then
    stopFlying()
  end
end)

script.Parent.KeyDown:Connect(function(key)
  if key == "w" then
    fly()
  end
end)
