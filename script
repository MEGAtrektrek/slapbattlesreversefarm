if not game:IsLoaded() then
    game.Loaded:Wait()
end
repeat wait() until game.Players.LocalPlayer
wait()

if workspace:FindFirstChild("Safespot") == nil then
	local Safespot = Instance.new("Part",workspace)
	Safespot.Name = "Safespot"
	Safespot.Position = Vector3.new(10000,-50,10000)
	Safespot.Size = Vector3.new(500,10,500)
	Safespot.Anchored = true
	Safespot.CanCollide = true
	Safespot.Transparency = .5
	
	local Safespot1 = Instance.new("Part",workspace)
	Safespot1.Name = "DefendPart"
	Safespot1.Position = Vector3.new(10000.2, 13, 9752.45)
	Safespot1.Size = Vector3.new(500, 117, 5)
	Safespot1.Anchored = true
	Safespot1.CanCollide = true
	Safespot1.Transparency = .5
	Safespot1.Parent = game.workspace.Safespot
	
	local Safespot2 = Instance.new("Part",workspace)
	Safespot2.Name = "DefendPart1"
	Safespot2.Position = Vector3.new(10248.2, 13, 10002.4)
	Safespot2.Size = Vector3.new(5, 117, 496)
	Safespot2.Anchored = true
	Safespot2.CanCollide = true
	Safespot2.Transparency = .5
	Safespot2.Parent = game.workspace.Safespot
	
	local Safespot3 = Instance.new("Part",workspace)
	Safespot3.Name = "DefendPart2"
	Safespot3.Position = Vector3.new(9998.13, 13, 10247.2)
	Safespot3.Size = Vector3.new(497, 117, 6)
	Safespot3.Anchored = true
	Safespot3.CanCollide = true
	Safespot3.Transparency = .5
	Safespot3.Parent = game.workspace.Safespot
	
	local Safespot4 = Instance.new("Part",workspace)
	Safespot4.Name = "DefendPart3"
	Safespot4.Position = Vector3.new(9752.71, 13, 9999.28)
	Safespot4.Size = Vector3.new(7, 117, 490)
	Safespot4.Anchored = true
	Safespot4.CanCollide = true
	Safespot4.Transparency = .5
	Safespot4.Parent = game.workspace.Safespot
	
	local Safespot5 = Instance.new("Part",workspace)
	Safespot5.Name = "DefendPart4"
	Safespot5.Position = Vector3.new(10001.1, 76, 9999.66)
	Safespot5.Size = Vector3.new(491, 10, 491)
	Safespot5.Anchored = true
	Safespot5.CanCollide = true
	Safespot5.Transparency = .5
	Safespot5.Parent = game.workspace.Safespot
end


local function Get()
	fireclickdetector(workspace.Lobby.Reverse.ClickDetector)
	game:GetService("ReplicatedStorage"):WaitForChild("ReverseAbility"):FireServer()
	wait()
	fireclickdetector(workspace.Lobby.Replica.ClickDetector)
	repeat task.wait()
		firetouchinterest(game.Players.LocalPlayer.Character:WaitForChild("Head"), workspace.Lobby.Teleport2.TouchInterest.Parent, 0)
		firetouchinterest(game.Players.LocalPlayer.Character:WaitForChild("Head"), workspace.Lobby.Teleport2.TouchInterest.Parent, 1)
	until game.Players.LocalPlayer.Character:FindFirstChild("entered")
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = workspace["Safespot"].CFrame * CFrame.new(0,10,0)
	wait(0.135)
	game:GetService("ReplicatedStorage").Duplicate:FireServer()
	wait(Setting.Time)
	local module = loadstring(game:HttpGet"https://raw.githubusercontent.com/LeoKholYt/roblox/main/lk_serverhop.lua")()
	module:Teleport(game.PlaceId)
end

if game.Players.LocalPlayer.Character:FindFirstChild("entered") == nil then
	coroutine.wrap(Get)()
	for i, v in ipairs(workspace.Arena.island5.Slapples:GetDescendants()) do
                if v.Name == "Glove" and v:FindFirstChildWhichIsA("TouchTransmitter") then
                    firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart, v, 0)
        firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart, v, 1)
                end
            end
	while wait() do 
		if game.Players.LocalPlayer.Character:FindFirstChild("entered") and game.Players.LocalPlayer.Character.Humanoid.Health ~= 0 then
			for i, v in pairs(workspace:GetChildren()) do 
				if v.Name:match(game.Players.LocalPlayer.Name) and v:FindFirstChild("HumanoidRootPart") then
					for i = 1,Setting.Amount do
						if game.Players.LocalPlayer.Character:FindFirstChild("entered") and game.Players.LocalPlayer.Character.Humanoid.Health ~= 0 then
							game:GetService("ReplicatedStorage").b:FireServer(v:WaitForChild("Head"),true)
						end
					end
				end
			end
		end
	end
end
