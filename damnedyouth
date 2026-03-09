-- Poeseria Hub Trade UI
-- LocalScript

local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")

-- ScreenGui
local gui = Instance.new("ScreenGui")
gui.Name = "TradeHubUI"
gui.Parent = playerGui

-- Main Frame
local frame = Instance.new("Frame")
frame.Size = UDim2.new(0,300,0,230)
frame.Position = UDim2.new(0.5,-150,0.5,-115)
frame.BackgroundColor3 = Color3.fromRGB(10,10,15)
frame.BorderSizePixel = 0
frame.Parent = gui

local corner = Instance.new("UICorner")
corner.CornerRadius = UDim.new(0,12)
corner.Parent = frame

-- Title
local title = Instance.new("TextLabel")
title.Size = UDim2.new(1,0,0,30)
title.BackgroundTransparency = 1
title.Text = "Poseria Hub"
title.TextColor3 = Color3.fromRGB(200,150,255)
title.Font = Enum.Font.GothamBold
title.TextSize = 18
title.Parent = frame

-- Username Box
local username = Instance.new("TextBox")
username.Size = UDim2.new(0.9,0,0,30)
username.Position = UDim2.new(0.05,0,0,40)
username.PlaceholderText = "Search Username..."
username.Text = ""
username.BackgroundColor3 = Color3.fromRGB(30,30,35)
username.TextColor3 = Color3.new(1,1,1)
username.Font = Enum.Font.Gotham
username.TextSize = 14
username.Parent = frame

local boxCorner = Instance.new("UICorner")
boxCorner.CornerRadius = UDim.new(0,8)
boxCorner.Parent = username


-- Toggle creator
local function createToggle(text, yPos)

	local holder = Instance.new("Frame")
	holder.Size = UDim2.new(0.9,0,0,35)
	holder.Position = UDim2.new(0.05,0,0,yPos)
	holder.BackgroundTransparency = 1
	holder.Parent = frame

	local label = Instance.new("TextLabel")
	label.Size = UDim2.new(0.7,0,1,0)
	label.BackgroundTransparency = 1
	label.Text = text
	label.TextColor3 = Color3.new(1,1,1)
	label.Font = Enum.Font.Gotham
	label.TextSize = 14
	label.TextXAlignment = Enum.TextXAlignment.Left
	label.Parent = holder

	local toggle = Instance.new("TextButton")
	toggle.Size = UDim2.new(0,40,0,20)
	toggle.Position = UDim2.new(1,-45,0.5,-10)
	toggle.Text = ""
	toggle.BackgroundColor3 = Color3.fromRGB(80,80,80)
	toggle.Parent = holder

	local tCorner = Instance.new("UICorner")
	tCorner.CornerRadius = UDim.new(1,0)
	tCorner.Parent = toggle

	local enabled = false

	toggle.MouseButton1Click:Connect(function()
		enabled = not enabled

		if enabled then
			toggle.BackgroundColor3 = Color3.fromRGB(170,85,255)
		else
			toggle.BackgroundColor3 = Color3.fromRGB(80,80,80)
		end

		print(text.." = "..tostring(enabled))
	end)

end


createToggle("FREEZE TRADE", 80)
createToggle("AUTO ACCEPT", 120)
createToggle("FAST TRADE", 160)
