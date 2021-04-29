--[[
O SCRIPT N TA OBFUSCADO POR QUE QUEBRA O SCRIPT, MAIS FODASE VAI SER ASSIM MSM
RECOMENDO USAR O LOADSTRING() CASO ELES ATUALIZE EU VOU ATUALIZAR AK TBM
SCRIPT DE FLY N FOI EU QUE FIZ CREDITOS PARA O MANO DA TOOLBOX
]]

local Player = game:GetService("Players")
local StarterGui = game:GetService("StarterGui")
local bindable = Instance.new("BindableFunction")


if game.PlaceId == 4753194980 then
	game:GetService("UserInputService").MouseIconEnabled = true
	local mt = getrawmetatable(game)
	setreadonly(mt, false)
	local oldmt = mt.__namecall
	mt.__namecall = newcclosure(function(Self, ...)
		local method = getnamecallmethod()
		if method == 'Kick' then
			print ("Bypassed by gameleaks")
			wait(1)
			return nil
		end
		return oldmt(Self, ...)
	end)
	setreadonly(mt, true)

	for i,v in pairs(game.Workspace:GetDescendants())do
		if v.Name == "RankDoor"then
			v:Destroy()
		end
	end

	for i,v in pairs(game.ReplicatedStorage:GetChildren())do
		if v:IsA("Folder")then
			if v.Name == "ClientEvents" or v.Name == "ServerEvents" or v.Name == "DefaultChatSystemChatEvents" then
			else
				v:Destroy()
			end
		end
	end
	local digits = {[0] = '', 'UM', 'DOIS', 'TRÊS', 'QUATRO', 'CINCO', 'SEIS', 'SETE', 'OITO', 'NOVE'}
	local teens = {'DEZ', 'ONZE', 'DOZE', 'TREZE', 'QUARTOZE', 'QUINZE', 'DEZESSEIS', 'DEZESSETE', 'DEZOITO', 'DEZENOVE'}
	local doubles = {'VINTE', 'TRINTA', 'QUARENTA', 'CINQUENTA', 'SESSENTA', 'SETENTA', 'OITENTA', 'NOVENTA'}
	local powers = {'CENTO', 'MIL', 'MILHÃO', 'BILHÃO', 'TRILHÃO'}
	local splits = {}
	local words = {}

	function SplitNumber()
		local strNum = strNum
		if #strNum >= 3 and #strNum < 36 then
			for i = 0, math.ceil(#strNum/3)-1 do
				local first = (-2-(3*i)) < -#strNum and -#strNum + 1 or (-2-(3*i))
				local split = strNum:sub(#strNum + first , #strNum - (3*i) )
				splits[i+1] = split
			end
			for i = #splits, 1, -1 do
				local number = ''
				if #splits[i] == 3 and splits[i] ~= '000' then
					number = digits[tonumber(splits[i]:sub(1,1))]..' '..(tonumber(splits[i]:sub(1,1)) == 0 and '' or powers[1])
					number = number..' '..ToWords(splits[i]:sub(2))..' '..(i ~= 1 and powers[i] or '')
				elseif splits[i] == '000' then
					number = ''
				else
					number = ToWords(splits[i]:sub(1))..' '..(i ~= 1 and powers[i] or '')
				end
				words[#words+1] = number
			end
		end
		return table.concat(words,' ')
	end

	function ToWords(num)
		num = tonumber(num)
		strNum = tostring(num)
		if #strNum == 1 then
			return digits[num]
		elseif #strNum == 2 and num < 20 then
			return teens[num-9]
		elseif #strNum == 2 and num >= 20 then
			return doubles[tonumber(strNum:sub(1,1))-1].." E "..digits[tonumber(strNum:sub(2,2))]
		elseif #strNum > 2 and num >= 20 then
			return SplitNumber()
		end
	end
	
	local Yeh = false

	-- Instances:

	local ScreenGui = Instance.new("ScreenGui")
	local Main = Instance.new("Frame")
	local Bar1 = Instance.new("Frame")
	local Close = Instance.new("TextButton")
	local UITextSizeConstraint = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint = Instance.new("UIAspectRatioConstraint")
	local Tittle = Instance.new("TextLabel")
	local UITextSizeConstraint_2 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_2 = Instance.new("UIAspectRatioConstraint")
	local Line = Instance.new("Frame")
	local Frame = Instance.new("Frame")
	local UIListLayout = Instance.new("UIListLayout")
	local Cheat1 = Instance.new("Frame")
	local TextLabel = Instance.new("TextLabel")
	local UITextSizeConstraint_3 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_3 = Instance.new("UIAspectRatioConstraint")
	local TextBox = Instance.new("TextBox")
	local UITextSizeConstraint_4 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_4 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_5 = Instance.new("UIAspectRatioConstraint")
	local Cheat2 = Instance.new("Frame")
	local TextLabel_2 = Instance.new("TextLabel")
	local UITextSizeConstraint_5 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_6 = Instance.new("UIAspectRatioConstraint")
	local TextBox_2 = Instance.new("TextBox")
	local UITextSizeConstraint_6 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_7 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_8 = Instance.new("UIAspectRatioConstraint")
	local Cheat3 = Instance.new("Frame")
	local TextLabel_3 = Instance.new("TextLabel")
	local UITextSizeConstraint_7 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_9 = Instance.new("UIAspectRatioConstraint")
	local TextBox_3 = Instance.new("TextBox")
	local UITextSizeConstraint_8 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_10 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_11 = Instance.new("UIAspectRatioConstraint")
	local Cheat4 = Instance.new("Frame")
	local TextLabel_4 = Instance.new("TextLabel")
	local UITextSizeConstraint_9 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_12 = Instance.new("UIAspectRatioConstraint")
	local TextButton = Instance.new("TextButton")
	local UITextSizeConstraint_10 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_13 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_14 = Instance.new("UIAspectRatioConstraint")
	local AutoFarm = Instance.new("Frame")
	local TextLabel_5 = Instance.new("TextLabel")
	local UITextSizeConstraint_11 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_15 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_16 = Instance.new("UIAspectRatioConstraint")
	local Cheat5 = Instance.new("Frame")
	local TextLabel_6 = Instance.new("TextLabel")
	local UITextSizeConstraint_12 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_17 = Instance.new("UIAspectRatioConstraint")
	local TextButton_2 = Instance.new("TextButton")
	local UITextSizeConstraint_13 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_18 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_19 = Instance.new("UIAspectRatioConstraint")
	local Cheat6 = Instance.new("Frame")
	local TextLabel_7 = Instance.new("TextLabel")
	local UITextSizeConstraint_14 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_20 = Instance.new("UIAspectRatioConstraint")
	local TextButton_3 = Instance.new("TextButton")
	local UITextSizeConstraint_15 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_21 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_22 = Instance.new("UIAspectRatioConstraint")
	local Credits = Instance.new("Frame")
	local TextLabel_8 = Instance.new("TextLabel")
	local UITextSizeConstraint_16 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_23 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_24 = Instance.new("UIAspectRatioConstraint")
	local TextButton_4 = Instance.new("TextButton")
	local UITextSizeConstraint_17 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_25 = Instance.new("UIAspectRatioConstraint")
	local TextButton_5 = Instance.new("TextButton")
	local UITextSizeConstraint_18 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_26 = Instance.new("UIAspectRatioConstraint")
	local TextButton_6 = Instance.new("TextButton")
	local UITextSizeConstraint_19 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_27 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_28 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_29 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_30 = Instance.new("UIAspectRatioConstraint")
	local Bar2 = Instance.new("Frame")
	local Close_2 = Instance.new("TextButton")
	local UITextSizeConstraint_20 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_31 = Instance.new("UIAspectRatioConstraint")
	local Tittle_2 = Instance.new("TextLabel")
	local UITextSizeConstraint_21 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_32 = Instance.new("UIAspectRatioConstraint")
	local Line_2 = Instance.new("Frame")
	local Frame_2 = Instance.new("Frame")
	local UIListLayout_2 = Instance.new("UIListLayout")
	local Cheat1_2 = Instance.new("Frame")
	local TextLabel_9 = Instance.new("TextLabel")
	local UITextSizeConstraint_22 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_33 = Instance.new("UIAspectRatioConstraint")
	local TextButton_7 = Instance.new("TextButton")
	local UITextSizeConstraint_23 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_34 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_35 = Instance.new("UIAspectRatioConstraint")
	local Cheat2_2 = Instance.new("Frame")
	local TextLabel_10 = Instance.new("TextLabel")
	local UITextSizeConstraint_24 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_36 = Instance.new("UIAspectRatioConstraint")
	local TextButton_8 = Instance.new("TextButton")
	local UITextSizeConstraint_25 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_37 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_38 = Instance.new("UIAspectRatioConstraint")
	local Cheat3_2 = Instance.new("Frame")
	local TextLabel_11 = Instance.new("TextLabel")
	local UITextSizeConstraint_26 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_39 = Instance.new("UIAspectRatioConstraint")
	local TextButton_9 = Instance.new("TextButton")
	local UITextSizeConstraint_27 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_40 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_41 = Instance.new("UIAspectRatioConstraint")
	local Cheat4_2 = Instance.new("Frame")
	local TextLabel_12 = Instance.new("TextLabel")
	local UITextSizeConstraint_28 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_42 = Instance.new("UIAspectRatioConstraint")
	local TextButton_10 = Instance.new("TextButton")
	local UITextSizeConstraint_29 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_43 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_44 = Instance.new("UIAspectRatioConstraint")
	local Cheat5_2 = Instance.new("Frame")
	local TextLabel_13 = Instance.new("TextLabel")
	local UITextSizeConstraint_30 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_45 = Instance.new("UIAspectRatioConstraint")
	local TextButton_11 = Instance.new("TextButton")
	local UITextSizeConstraint_31 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_46 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_47 = Instance.new("UIAspectRatioConstraint")
	local Cheat6_2 = Instance.new("Frame")
	local TextLabel_14 = Instance.new("TextLabel")
	local UITextSizeConstraint_32 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_48 = Instance.new("UIAspectRatioConstraint")
	local TextButton_12 = Instance.new("TextButton")
	local UITextSizeConstraint_33 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_49 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_50 = Instance.new("UIAspectRatioConstraint")
	local Cheat7 = Instance.new("Frame")
	local TextLabel_15 = Instance.new("TextLabel")
	local UITextSizeConstraint_34 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_51 = Instance.new("UIAspectRatioConstraint")
	local TextButton_13 = Instance.new("TextButton")
	local UITextSizeConstraint_35 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_52 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_53 = Instance.new("UIAspectRatioConstraint")
	local Cheat8 = Instance.new("Frame")
	local TextLabel_16 = Instance.new("TextLabel")
	local UITextSizeConstraint_36 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_54 = Instance.new("UIAspectRatioConstraint")
	local TextButton_14 = Instance.new("TextButton")
	local UITextSizeConstraint_37 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_55 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_56 = Instance.new("UIAspectRatioConstraint")
	local Cheat9 = Instance.new("Frame")
	local TextLabel_17 = Instance.new("TextLabel")
	local UITextSizeConstraint_38 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_57 = Instance.new("UIAspectRatioConstraint")
	local TextButton_15 = Instance.new("TextButton")
	local UITextSizeConstraint_39 = Instance.new("UITextSizeConstraint")
	local UIAspectRatioConstraint_58 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_59 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_60 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_61 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_62 = Instance.new("UIAspectRatioConstraint")
	local UIAspectRatioConstraint_63 = Instance.new("UIAspectRatioConstraint")

	--Properties:

	ScreenGui.Parent = game.CoreGui
	ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	ScreenGui.ResetOnSpawn = false

	Main.Name = "Main"
	Main.Parent = ScreenGui
	Main.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Main.BackgroundTransparency = 1.000
	Main.Position = UDim2.new(-0.17567569, 0, -0.197211161, 0)
	Main.Size = UDim2.new(1.203668, 0, 1.24501991, 0)

	Bar1.Name = "Bar1"
	Bar1.Parent = Main
	Bar1.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
	Bar1.BorderSizePixel = 0
	Bar1.Position = UDim2.new(0.247, 0, 0.194, 0)
	Bar1.Size = UDim2.new(0.137931034, 0, 0.0335999988, 0)
	Bar1.Draggable = true
	Bar1.Active = true
	Bar1.Selectable = true

	Close.Name = "Close"
	Close.Parent = Bar1
	Close.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Close.BackgroundTransparency = 1.000
	Close.Position = UDim2.new(0.860540152, 0, 0.095238097, 0)
	Close.Size = UDim2.new(0.0813953504, 0, 0.809523821, 0)
	Close.Font = Enum.Font.Gotham
	Close.Text = "-"
	Close.TextColor3 = Color3.fromRGB(255, 255, 255)
	Close.TextScaled = true
	Close.TextSize = 14.000
	Close.TextWrapped = true
	Close.MouseButton1Click:Connect(function()
		if Frame.Visible == true then
			Frame.Visible = false
			Close.Text = "+"
		else
			Frame.Visible = true
			Close.Text = "-"
		end
	end)

	UITextSizeConstraint.Parent = Close
	UITextSizeConstraint.MaxTextSize = 17

	UIAspectRatioConstraint.Parent = Close
	UIAspectRatioConstraint.AspectRatio = 0.802

	Tittle.Name = "Tittle"
	Tittle.Parent = Bar1
	Tittle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Tittle.BackgroundTransparency = 1.000
	Tittle.Position = UDim2.new(0.220930234, 0, 0.142857149, 0)
	Tittle.Size = UDim2.new(0.558139563, 0, 0.666666687, 0)
	Tittle.Font = Enum.Font.Gotham
	Tittle.Text = "Main"
	Tittle.TextColor3 = Color3.fromRGB(255, 255, 255)
	Tittle.TextScaled = true
	Tittle.TextSize = 14.000
	Tittle.TextWrapped = true

	UITextSizeConstraint_2.Parent = Tittle
	UITextSizeConstraint_2.MaxTextSize = 14

	UIAspectRatioConstraint_2.Parent = Tittle
	UIAspectRatioConstraint_2.AspectRatio = 6.678

	Line.Name = "Line"
	Line.Parent = Bar1
	Line.BackgroundColor3 = Color3.fromRGB(0, 141, 0)
	Line.BorderSizePixel = 0
	Line.Position = UDim2.new(0, 0, 1, 0)
	Line.Size = UDim2.new(1, 0, 0.142857149, 0)

	Frame.Parent = Line
	Frame.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
	Frame.BorderSizePixel = 0
	Frame.Position = UDim2.new(-0.00176026102, 0, 0.795740783, 0)
	Frame.Size = UDim2.new(1, 0, 72.6666641, 0)

	UIListLayout.Parent = Frame
	UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder

	Cheat1.Name = "Cheat1"
	Cheat1.Parent = Frame
	Cheat1.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat1.BackgroundTransparency = 1.000
	Cheat1.BorderSizePixel = 0
	Cheat1.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel.Parent = Cheat1
	TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel.BackgroundTransparency = 1.000
	TextLabel.BorderSizePixel = 0
	TextLabel.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel.Font = Enum.Font.Gotham
	TextLabel.Text = "[S] Speed :"
	TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel.TextScaled = true
	TextLabel.TextSize = 14.000
	TextLabel.TextWrapped = true
	TextLabel.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_3.Parent = TextLabel
	UITextSizeConstraint_3.MaxTextSize = 14

	UIAspectRatioConstraint_3.Parent = TextLabel
	UIAspectRatioConstraint_3.AspectRatio = 5.970

	TextBox.Parent = Cheat1
	TextBox.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextBox.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextBox.Position = UDim2.new(0.651162803, 0, 0.208333328, 0)
	TextBox.Size = UDim2.new(0.290697664, 0, 0.625, 0)
	TextBox.ClearTextOnFocus = false
	TextBox.Font = Enum.Font.Gotham
	TextBox.PlaceholderColor3 = Color3.fromRGB(255, 255, 255)
	TextBox.Text = 16
	TextBox.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextBox.TextScaled = true
	TextBox.TextSize = 14.000
	TextBox.TextWrapped = true
	TextBox:GetPropertyChangedSignal("Text"):Connect(function()
		TextBox.Text = TextBox.Text:gsub('%D+', '');
	end)
	TextBox.Changed:Connect(function()
		while wait(.3)do
			if Player.LocalPlayer.Character:FindFirstChild("Humanoid") then
				Player.LocalPlayer.Character.Humanoid.WalkSpeed = TextBox.Text
			end
		end
	end)

	UITextSizeConstraint_4.Parent = TextBox
	UITextSizeConstraint_4.MaxTextSize = 14

	UIAspectRatioConstraint_4.Parent = TextBox
	UIAspectRatioConstraint_4.AspectRatio = 2.995

	UIAspectRatioConstraint_5.Parent = Cheat1
	UIAspectRatioConstraint_5.AspectRatio = 6.980

	Cheat2.Name = "Cheat2"
	Cheat2.Parent = Frame
	Cheat2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat2.BackgroundTransparency = 1.000
	Cheat2.BorderSizePixel = 0
	Cheat2.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel_2.Parent = Cheat2
	TextLabel_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_2.BackgroundTransparency = 1.000
	TextLabel_2.BorderSizePixel = 0
	TextLabel_2.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel_2.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel_2.Font = Enum.Font.Gotham
	TextLabel_2.Text = "[J] Jump :"
	TextLabel_2.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_2.TextScaled = true
	TextLabel_2.TextSize = 14.000
	TextLabel_2.TextWrapped = true
	TextLabel_2.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_5.Parent = TextLabel_2
	UITextSizeConstraint_5.MaxTextSize = 14

	UIAspectRatioConstraint_6.Parent = TextLabel_2
	UIAspectRatioConstraint_6.AspectRatio = 5.970

	TextBox_2.Parent = Cheat2
	TextBox_2.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextBox_2.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextBox_2.Position = UDim2.new(0.651162803, 0, 0.208333328, 0)
	TextBox_2.Size = UDim2.new(0.290697664, 0, 0.625, 0)
	TextBox_2.ClearTextOnFocus = false
	TextBox_2.Font = Enum.Font.Gotham
	TextBox_2.PlaceholderColor3 = Color3.fromRGB(255, 255, 255)
	TextBox_2.Text = 50
	TextBox_2.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextBox_2.TextScaled = true
	TextBox_2.TextSize = 14.000
	TextBox_2.TextWrapped = true
	TextBox_2:GetPropertyChangedSignal("Text"):Connect(function()
		TextBox_2.Text = TextBox_2.Text:gsub('%D+', '');
	end)
	TextBox_2.Changed:Connect(function()
		while wait(.3)do
			if Player.LocalPlayer.Character:FindFirstChild("Humanoid") then
				Player.LocalPlayer.Character.Humanoid.JumpPower = TextBox_2.Text
			end
		end
	end)

	UITextSizeConstraint_6.Parent = TextBox_2
	UITextSizeConstraint_6.MaxTextSize = 14

	UIAspectRatioConstraint_7.Parent = TextBox_2
	UIAspectRatioConstraint_7.AspectRatio = 2.995

	UIAspectRatioConstraint_8.Parent = Cheat2
	UIAspectRatioConstraint_8.AspectRatio = 6.980

	Cheat3.Name = "Cheat3"
	Cheat3.Parent = Frame
	Cheat3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat3.BackgroundTransparency = 1.000
	Cheat3.BorderSizePixel = 0
	Cheat3.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel_3.Parent = Cheat3
	TextLabel_3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_3.BackgroundTransparency = 1.000
	TextLabel_3.BorderSizePixel = 0
	TextLabel_3.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel_3.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel_3.Font = Enum.Font.Gotham
	TextLabel_3.Text = "[G] Gravity :"
	TextLabel_3.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_3.TextScaled = true
	TextLabel_3.TextSize = 14.000
	TextLabel_3.TextWrapped = true
	TextLabel_3.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_7.Parent = TextLabel_3
	UITextSizeConstraint_7.MaxTextSize = 14

	UIAspectRatioConstraint_9.Parent = TextLabel_3
	UIAspectRatioConstraint_9.AspectRatio = 6.963

	TextBox_3.Parent = Cheat3
	TextBox_3.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextBox_3.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextBox_3.Position = UDim2.new(0.651162803, 0, 0.208333328, 0)
	TextBox_3.Size = UDim2.new(0.290697664, 0, 0.625, 0)
	TextBox_3.ClearTextOnFocus = false
	TextBox_3.Font = Enum.Font.Gotham
	TextBox_3.PlaceholderColor3 = Color3.fromRGB(255, 255, 255)
	TextBox_3.Text = 196.2
	TextBox_3.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextBox_3.TextScaled = true
	TextBox_3.TextSize = 14.000
	TextBox_3.TextWrapped = true
	TextBox_3:GetPropertyChangedSignal("Text"):Connect(function()
		TextBox_3.Text = TextBox_3.Text:gsub('%D+', '');
	end)
	TextBox_3.Changed:Connect(function()
		workspace.Gravity = TextBox_3.Text
	end)

	UITextSizeConstraint_8.Parent = TextBox_3
	UITextSizeConstraint_8.MaxTextSize = 14

	UIAspectRatioConstraint_10.Parent = TextBox_3
	UIAspectRatioConstraint_10.AspectRatio = 3.150

	UIAspectRatioConstraint_11.Parent = Cheat3
	UIAspectRatioConstraint_11.AspectRatio = 6.980

	Cheat4.Name = "Cheat4"
	Cheat4.Parent = Frame
	Cheat4.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat4.BackgroundTransparency = 1.000
	Cheat4.BorderSizePixel = 0
	Cheat4.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel_4.Parent = Cheat4
	TextLabel_4.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_4.BackgroundTransparency = 1.000
	TextLabel_4.BorderSizePixel = 0
	TextLabel_4.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel_4.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel_4.Font = Enum.Font.Gotham
	TextLabel_4.Text = "[F] Fly :"
	TextLabel_4.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_4.TextScaled = true
	TextLabel_4.TextSize = 14.000
	TextLabel_4.TextWrapped = true
	TextLabel_4.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_9.Parent = TextLabel_4
	UITextSizeConstraint_9.MaxTextSize = 14

	UIAspectRatioConstraint_12.Parent = TextLabel_4
	UIAspectRatioConstraint_12.AspectRatio = 6.925

	TextButton.Parent = Cheat4
	TextButton.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextButton.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextButton.Position = UDim2.new(0.691860497, 0, 0.208333328, 0)
	TextButton.Size = UDim2.new(0.209302321, 0, 0.583333313, 0)
	TextButton.Font = Enum.Font.Gotham
	TextButton.Text = "E"
	TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton.TextScaled = true
	TextButton.TextSize = 14.000
	TextButton.TextWrapped = true

	UITextSizeConstraint_10.Parent = TextButton
	UITextSizeConstraint_10.MaxTextSize = 14

	UIAspectRatioConstraint_13.Parent = TextButton
	UIAspectRatioConstraint_13.AspectRatio = 2.705

	UIAspectRatioConstraint_14.Parent = Cheat4
	UIAspectRatioConstraint_14.AspectRatio = 6.980

	AutoFarm.Name = "AutoFarm"
	AutoFarm.Parent = Frame
	AutoFarm.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	AutoFarm.BorderSizePixel = 0
	AutoFarm.Position = UDim2.new(0, 0, 0.33488372, 0)
	AutoFarm.Size = UDim2.new(1, 0, 0.0688073412, 0)

	TextLabel_5.Parent = AutoFarm
	TextLabel_5.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_5.BackgroundTransparency = 1.000
	TextLabel_5.Size = UDim2.new(1, 0, 1, 0)
	TextLabel_5.Font = Enum.Font.Gotham
	TextLabel_5.Text = "Auto Farm"
	TextLabel_5.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_5.TextScaled = true
	TextLabel_5.TextSize = 14.000
	TextLabel_5.TextWrapped = true

	UITextSizeConstraint_11.Parent = TextLabel_5
	UITextSizeConstraint_11.MaxTextSize = 14

	UIAspectRatioConstraint_15.Parent = TextLabel_5
	UIAspectRatioConstraint_15.AspectRatio = 11.168

	UIAspectRatioConstraint_16.Parent = AutoFarm
	UIAspectRatioConstraint_16.AspectRatio = 11.168

	Cheat5.Name = "Cheat5"
	Cheat5.Parent = Frame
	Cheat5.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat5.BackgroundTransparency = 1.000
	Cheat5.BorderSizePixel = 0
	Cheat5.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel_6.Parent = Cheat5
	TextLabel_6.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_6.BackgroundTransparency = 1.000
	TextLabel_6.BorderSizePixel = 0
	TextLabel_6.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel_6.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel_6.Font = Enum.Font.Gotham
	TextLabel_6.Text = "[M] Money Farm :"
	TextLabel_6.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_6.TextScaled = true
	TextLabel_6.TextSize = 14.000
	TextLabel_6.TextWrapped = true
	TextLabel_6.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_12.Parent = TextLabel_6
	UITextSizeConstraint_12.MaxTextSize = 11

	UIAspectRatioConstraint_17.Parent = TextLabel_6
	UIAspectRatioConstraint_17.AspectRatio = 6.470

	TextButton_2.Parent = Cheat5
	TextButton_2.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextButton_2.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextButton_2.Position = UDim2.new(0.691860497, 0, 0.208333328, 0)
	TextButton_2.Size = UDim2.new(0.209302321, 0, 0.583333313, 0)
	TextButton_2.Font = Enum.Font.Gotham
	TextButton_2.Text = "Em breve"
	TextButton_2.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton_2.TextScaled = true
	TextButton_2.TextSize = 14.000
	TextButton_2.TextWrapped = true

	UITextSizeConstraint_13.Parent = TextButton_2
	UITextSizeConstraint_13.MaxTextSize = 14

	UIAspectRatioConstraint_18.Parent = TextButton_2
	UIAspectRatioConstraint_18.AspectRatio = 2.504

	UIAspectRatioConstraint_19.Parent = Cheat5
	UIAspectRatioConstraint_19.AspectRatio = 6.980

	Cheat6.Name = "Cheat6"
	Cheat6.Parent = Frame
	Cheat6.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat6.BackgroundTransparency = 1.000
	Cheat6.BorderSizePixel = 0
	Cheat6.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel_7.Parent = Cheat6
	TextLabel_7.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_7.BackgroundTransparency = 1.000
	TextLabel_7.BorderSizePixel = 0
	TextLabel_7.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel_7.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel_7.Font = Enum.Font.Gotham
	TextLabel_7.Text = "Auto JJ's"
	TextLabel_7.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_7.TextScaled = true
	TextLabel_7.TextSize = 14.000
	TextLabel_7.TextWrapped = true
	TextLabel_7.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_14.Parent = TextLabel_7
	UITextSizeConstraint_14.MaxTextSize = 13

	UIAspectRatioConstraint_20.Parent = TextLabel_7
	UIAspectRatioConstraint_20.AspectRatio = 6.470

	TextButton_3.Parent = Cheat6
	TextButton_3.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextButton_3.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextButton_3.Position = UDim2.new(0.691860497, 0, 0.208333328, 0)
	TextButton_3.Size = UDim2.new(0.209302321, 0, 0.583333313, 0)
	TextButton_3.Font = Enum.Font.Gotham
	TextButton_3.Text = ""
	TextButton_3.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton_3.TextScaled = true
	TextButton_3.TextSize = 14.000
	TextButton_3.TextWrapped = true
	TextButton_3.MouseButton1Click:Connect(function()
		if Yeh == true then
			Yeh = false
			TextButton_3.Text = ""
		else
			Yeh = true
			TextButton_3.Text = "X"
		end
	end)

	UITextSizeConstraint_15.Parent = TextButton_3
	UITextSizeConstraint_15.MaxTextSize = 14

	UIAspectRatioConstraint_21.Parent = TextButton_3
	UIAspectRatioConstraint_21.AspectRatio = 2.504

	UIAspectRatioConstraint_22.Parent = Cheat6
	UIAspectRatioConstraint_22.AspectRatio = 6.980

	Credits.Name = "Credits"
	Credits.Parent = Frame
	Credits.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	Credits.BorderSizePixel = 0
	Credits.Position = UDim2.new(0, 0, 0.33488372, 0)
	Credits.Size = UDim2.new(1, 0, 0.0688073412, 0)

	TextLabel_8.Parent = Credits
	TextLabel_8.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_8.BackgroundTransparency = 1.000
	TextLabel_8.BorderSizePixel = 2
	TextLabel_8.Size = UDim2.new(1, 0, 1, 0)
	TextLabel_8.Font = Enum.Font.Gotham
	TextLabel_8.Text = "Credits"
	TextLabel_8.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_8.TextScaled = true
	TextLabel_8.TextSize = 14.000
	TextLabel_8.TextWrapped = true

	UITextSizeConstraint_16.Parent = TextLabel_8
	UITextSizeConstraint_16.MaxTextSize = 14

	UIAspectRatioConstraint_23.Parent = TextLabel_8
	UIAspectRatioConstraint_23.AspectRatio = 11.168

	UIAspectRatioConstraint_24.Parent = Credits
	UIAspectRatioConstraint_24.AspectRatio = 11.168

	TextButton_4.Parent = Frame
	TextButton_4.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
	TextButton_4.BorderColor3 = Color3.fromRGB(34, 34, 34)
	TextButton_4.BorderSizePixel = 0
	TextButton_4.Position = UDim2.new(0, 0, 0.80930233, 0)
	TextButton_4.Size = UDim2.new(1, 0, 0.0642201826, 0)
	TextButton_4.Font = Enum.Font.Gotham
	TextButton_4.Text = "Discord"
	TextButton_4.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton_4.TextScaled = true
	TextButton_4.TextSize = 14.000
	TextButton_4.TextWrapped = true
	TextButton_4.MouseButton1Click:Connect(function()
		setclipboard("https://www.youtube.com/channel/UCpQ-1MmZCpMiBm-SXk2ewaw/featured")
		StarterGui:SetCore("SendNotification", {
			Title = "Link copied!",
			Text = "Paste in browser",
			Duration = 5,
			Callback = bindable,
		})
	end)

	UITextSizeConstraint_17.Parent = TextButton_4
	UITextSizeConstraint_17.MaxTextSize = 14

	UIAspectRatioConstraint_25.Parent = TextButton_4
	UIAspectRatioConstraint_25.AspectRatio = 11.966

	TextButton_5.Parent = Frame
	TextButton_5.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
	TextButton_5.BorderColor3 = Color3.fromRGB(34, 34, 34)
	TextButton_5.BorderSizePixel = 0
	TextButton_5.Position = UDim2.new(0, 0, 0.80930233, 0)
	TextButton_5.Size = UDim2.new(1, 0, 0.0642201826, 0)
	TextButton_5.Font = Enum.Font.Gotham
	TextButton_5.Text = "YouTube"
	TextButton_5.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton_5.TextScaled = true
	TextButton_5.TextSize = 14.000
	TextButton_5.TextWrapped = true
	TextButton_5.MouseButton1Click:Connect(function()
		setclipboard("https://www.youtube.com/channel/UCpQ-1MmZCpMiBm-SXk2ewaw/featured")
		StarterGui:SetCore("SendNotification", {
			Title = "Link copied!",
			Text = "Paste in browser",
			Duration = 5,
			Callback = bindable,
		})
	end)

	UITextSizeConstraint_18.Parent = TextButton_5
	UITextSizeConstraint_18.MaxTextSize = 14

	UIAspectRatioConstraint_26.Parent = TextButton_5
	UIAspectRatioConstraint_26.AspectRatio = 11.966

	TextButton_6.Parent = Frame
	TextButton_6.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
	TextButton_6.BorderColor3 = Color3.fromRGB(34, 34, 34)
	TextButton_6.BorderSizePixel = 0
	TextButton_6.Position = UDim2.new(0, 0, 0.80930233, 0)
	TextButton_6.Size = UDim2.new(1, 0, 0.0642201826, 0)
	TextButton_6.Font = Enum.Font.Gotham
	TextButton_6.Text = "GameLeaks 2.0"
	TextButton_6.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton_6.TextScaled = true
	TextButton_6.TextSize = 14.000
	TextButton_6.TextWrapped = true

	UITextSizeConstraint_19.Parent = TextButton_6
	UITextSizeConstraint_19.MaxTextSize = 14

	UIAspectRatioConstraint_27.Parent = TextButton_6
	UIAspectRatioConstraint_27.AspectRatio = 11.966

	UIAspectRatioConstraint_28.Parent = Frame
	UIAspectRatioConstraint_28.AspectRatio = 0.768

	UIAspectRatioConstraint_29.Parent = Line
	UIAspectRatioConstraint_29.AspectRatio = 55.839

	UIAspectRatioConstraint_30.Parent = Bar1
	UIAspectRatioConstraint_30.AspectRatio = 7.977

	Bar2.Name = "Bar2"
	Bar2.Parent = Main
	Bar2.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
	Bar2.BorderSizePixel = 0
	Bar2.Position = UDim2.new(0.413, 0, 0.194, 0)
	Bar2.Size = UDim2.new(0.137931034, 0, 0.0335999988, 0)
	Bar2.Draggable = true
	Bar2.Active = true
	Bar2.Selectable = true

	Close_2.Name = "Close"
	Close_2.Parent = Bar2
	Close_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Close_2.BackgroundTransparency = 1.000
	Close_2.Position = UDim2.new(0.860540152, 0, 0.095238097, 0)
	Close_2.Size = UDim2.new(0.0813953504, 0, 0.809523821, 0)
	Close_2.Font = Enum.Font.Gotham
	Close_2.Text = "-"
	Close_2.TextColor3 = Color3.fromRGB(255, 255, 255)
	Close_2.TextScaled = true
	Close_2.TextSize = 14.000
	Close_2.TextWrapped = true
	Close_2.MouseButton1Click:Connect(function()
		if Frame_2.Visible == true then
			Frame_2.Visible = false
			Close_2.Text = "+"
		else
			Frame_2.Visible = true
			Close_2.Text = "-"
		end
	end)

	UITextSizeConstraint_20.Parent = Close_2
	UITextSizeConstraint_20.MaxTextSize = 17

	UIAspectRatioConstraint_31.Parent = Close_2
	UIAspectRatioConstraint_31.AspectRatio = 0.802

	Tittle_2.Name = "Tittle"
	Tittle_2.Parent = Bar2
	Tittle_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Tittle_2.BackgroundTransparency = 1.000
	Tittle_2.Position = UDim2.new(0.220930234, 0, 0.142857149, 0)
	Tittle_2.Size = UDim2.new(0.558139563, 0, 0.666666687, 0)
	Tittle_2.Font = Enum.Font.Gotham
	Tittle_2.Text = "Teleports"
	Tittle_2.TextColor3 = Color3.fromRGB(255, 255, 255)
	Tittle_2.TextScaled = true
	Tittle_2.TextSize = 14.000
	Tittle_2.TextWrapped = true

	UITextSizeConstraint_21.Parent = Tittle_2
	UITextSizeConstraint_21.MaxTextSize = 14

	UIAspectRatioConstraint_32.Parent = Tittle_2
	UIAspectRatioConstraint_32.AspectRatio = 6.678

	Line_2.Name = "Line"
	Line_2.Parent = Bar2
	Line_2.BackgroundColor3 = Color3.fromRGB(0, 141, 0)
	Line_2.BorderSizePixel = 0
	Line_2.Position = UDim2.new(0, 0, 1, 0)
	Line_2.Size = UDim2.new(1, 0, 0.142857149, 0)

	Frame_2.Parent = Line_2
	Frame_2.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
	Frame_2.BorderSizePixel = 0
	Frame_2.Position = UDim2.new(-0.00176026102, 0, 0.795740783, 0)
	Frame_2.Size = UDim2.new(1, 0, 72.6666641, 0)

	UIListLayout_2.Parent = Frame_2
	UIListLayout_2.SortOrder = Enum.SortOrder.LayoutOrder

	Cheat1_2.Name = "Cheat1"
	Cheat1_2.Parent = Frame_2
	Cheat1_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat1_2.BackgroundTransparency = 1.000
	Cheat1_2.BorderSizePixel = 0
	Cheat1_2.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel_9.Parent = Cheat1_2
	TextLabel_9.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_9.BackgroundTransparency = 1.000
	TextLabel_9.BorderSizePixel = 0
	TextLabel_9.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel_9.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel_9.Font = Enum.Font.Gotham
	TextLabel_9.Text = "Spawm :"
	TextLabel_9.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_9.TextScaled = true
	TextLabel_9.TextSize = 14.000
	TextLabel_9.TextWrapped = true
	TextLabel_9.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_22.Parent = TextLabel_9
	UITextSizeConstraint_22.MaxTextSize = 14

	UIAspectRatioConstraint_33.Parent = TextLabel_9
	UIAspectRatioConstraint_33.AspectRatio = 6.470

	TextButton_7.Parent = Cheat1_2
	TextButton_7.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextButton_7.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextButton_7.Position = UDim2.new(0.691860497, 0, 0.208333328, 0)
	TextButton_7.Size = UDim2.new(0.209302321, 0, 0.583333313, 0)
	TextButton_7.Font = Enum.Font.Gotham
	TextButton_7.Text = "Ir"
	TextButton_7.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton_7.TextScaled = true
	TextButton_7.TextSize = 14.000
	TextButton_7.TextWrapped = true
	TextButton_7.MouseButton1Click:Connect(function()
		if Player.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
			Player.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(46, 192, -439)
		end
	end)

	UITextSizeConstraint_23.Parent = TextButton_7
	UITextSizeConstraint_23.MaxTextSize = 14

	UIAspectRatioConstraint_34.Parent = TextButton_7
	UIAspectRatioConstraint_34.AspectRatio = 2.504

	UIAspectRatioConstraint_35.Parent = Cheat1_2
	UIAspectRatioConstraint_35.AspectRatio = 6.980

	Cheat2_2.Name = "Cheat2"
	Cheat2_2.Parent = Frame_2
	Cheat2_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat2_2.BackgroundTransparency = 1.000
	Cheat2_2.BorderSizePixel = 0
	Cheat2_2.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel_10.Parent = Cheat2_2
	TextLabel_10.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_10.BackgroundTransparency = 1.000
	TextLabel_10.BorderSizePixel = 0
	TextLabel_10.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel_10.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel_10.Font = Enum.Font.Gotham
	TextLabel_10.Text = "Farda EB :"
	TextLabel_10.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_10.TextScaled = true
	TextLabel_10.TextSize = 14.000
	TextLabel_10.TextWrapped = true
	TextLabel_10.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_24.Parent = TextLabel_10
	UITextSizeConstraint_24.MaxTextSize = 14

	UIAspectRatioConstraint_36.Parent = TextLabel_10
	UIAspectRatioConstraint_36.AspectRatio = 6.470

	TextButton_8.Parent = Cheat2_2
	TextButton_8.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextButton_8.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextButton_8.Position = UDim2.new(0.691860497, 0, 0.208333328, 0)
	TextButton_8.Size = UDim2.new(0.209302321, 0, 0.583333313, 0)
	TextButton_8.Font = Enum.Font.Gotham
	TextButton_8.Text = "Ir"
	TextButton_8.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton_8.TextScaled = true
	TextButton_8.TextSize = 14.000
	TextButton_8.TextWrapped = true
	TextButton_8.MouseButton1Click:Connect(function()
		if Player.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
			Player.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-785, 193, 0)
		end
	end)

	UITextSizeConstraint_25.Parent = TextButton_8
	UITextSizeConstraint_25.MaxTextSize = 14

	UIAspectRatioConstraint_37.Parent = TextButton_8
	UIAspectRatioConstraint_37.AspectRatio = 2.504

	UIAspectRatioConstraint_38.Parent = Cheat2_2
	UIAspectRatioConstraint_38.AspectRatio = 6.980

	Cheat3_2.Name = "Cheat3"
	Cheat3_2.Parent = Frame_2
	Cheat3_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat3_2.BackgroundTransparency = 1.000
	Cheat3_2.BorderSizePixel = 0
	Cheat3_2.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel_11.Parent = Cheat3_2
	TextLabel_11.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_11.BackgroundTransparency = 1.000
	TextLabel_11.BorderSizePixel = 0
	TextLabel_11.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel_11.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel_11.Font = Enum.Font.Gotham
	TextLabel_11.Text = "Farda FE :"
	TextLabel_11.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_11.TextScaled = true
	TextLabel_11.TextSize = 14.000
	TextLabel_11.TextWrapped = true
	TextLabel_11.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_26.Parent = TextLabel_11
	UITextSizeConstraint_26.MaxTextSize = 14

	UIAspectRatioConstraint_39.Parent = TextLabel_11
	UIAspectRatioConstraint_39.AspectRatio = 6.470

	TextButton_9.Parent = Cheat3_2
	TextButton_9.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextButton_9.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextButton_9.Position = UDim2.new(0.691860497, 0, 0.208333328, 0)
	TextButton_9.Size = UDim2.new(0.209302321, 0, 0.583333313, 0)
	TextButton_9.Font = Enum.Font.Gotham
	TextButton_9.Text = "Ir"
	TextButton_9.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton_9.TextScaled = true
	TextButton_9.TextSize = 14.000
	TextButton_9.TextWrapped = true
	TextButton_9.MouseButton1Click:Connect(function()
		if Player.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
			Player.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(164, 193, 64)
		end
	end)

	UITextSizeConstraint_27.Parent = TextButton_9
	UITextSizeConstraint_27.MaxTextSize = 14

	UIAspectRatioConstraint_40.Parent = TextButton_9
	UIAspectRatioConstraint_40.AspectRatio = 2.504

	UIAspectRatioConstraint_41.Parent = Cheat3_2
	UIAspectRatioConstraint_41.AspectRatio = 6.980

	Cheat4_2.Name = "Cheat4"
	Cheat4_2.Parent = Frame_2
	Cheat4_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat4_2.BackgroundTransparency = 1.000
	Cheat4_2.BorderSizePixel = 0
	Cheat4_2.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel_12.Parent = Cheat4_2
	TextLabel_12.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_12.BackgroundTransparency = 1.000
	TextLabel_12.BorderSizePixel = 0
	TextLabel_12.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel_12.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel_12.Font = Enum.Font.Gotham
	TextLabel_12.Text = "Farda PE :"
	TextLabel_12.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_12.TextScaled = true
	TextLabel_12.TextSize = 14.000
	TextLabel_12.TextWrapped = true
	TextLabel_12.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_28.Parent = TextLabel_12
	UITextSizeConstraint_28.MaxTextSize = 14

	UIAspectRatioConstraint_42.Parent = TextLabel_12
	UIAspectRatioConstraint_42.AspectRatio = 6.470

	TextButton_10.Parent = Cheat4_2
	TextButton_10.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextButton_10.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextButton_10.Position = UDim2.new(0.691860497, 0, 0.208333328, 0)
	TextButton_10.Size = UDim2.new(0.209302321, 0, 0.583333313, 0)
	TextButton_10.Font = Enum.Font.Gotham
	TextButton_10.Text = "Ir"
	TextButton_10.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton_10.TextScaled = true
	TextButton_10.TextSize = 14.000
	TextButton_10.TextWrapped = true
	TextButton_10.MouseButton1Click:Connect(function()
		if Player.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
			Player.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(167, 193, 64)
		end
	end)

	UITextSizeConstraint_29.Parent = TextButton_10
	UITextSizeConstraint_29.MaxTextSize = 14

	UIAspectRatioConstraint_43.Parent = TextButton_10
	UIAspectRatioConstraint_43.AspectRatio = 2.504

	UIAspectRatioConstraint_44.Parent = Cheat4_2
	UIAspectRatioConstraint_44.AspectRatio = 6.980

	Cheat5_2.Name = "Cheat5"
	Cheat5_2.Parent = Frame_2
	Cheat5_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat5_2.BackgroundTransparency = 1.000
	Cheat5_2.BorderSizePixel = 0
	Cheat5_2.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel_13.Parent = Cheat5_2
	TextLabel_13.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_13.BackgroundTransparency = 1.000
	TextLabel_13.BorderSizePixel = 0
	TextLabel_13.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel_13.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel_13.Font = Enum.Font.Gotham
	TextLabel_13.Text = "Farda CIGS :"
	TextLabel_13.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_13.TextScaled = true
	TextLabel_13.TextSize = 14.000
	TextLabel_13.TextWrapped = true
	TextLabel_13.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_30.Parent = TextLabel_13
	UITextSizeConstraint_30.MaxTextSize = 14

	UIAspectRatioConstraint_45.Parent = TextLabel_13
	UIAspectRatioConstraint_45.AspectRatio = 6.470

	TextButton_11.Parent = Cheat5_2
	TextButton_11.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextButton_11.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextButton_11.Position = UDim2.new(0.691860497, 0, 0.208333328, 0)
	TextButton_11.Size = UDim2.new(0.209302321, 0, 0.583333313, 0)
	TextButton_11.Font = Enum.Font.Gotham
	TextButton_11.Text = "Ir"
	TextButton_11.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton_11.TextScaled = true
	TextButton_11.TextSize = 14.000
	TextButton_11.TextWrapped = true
	TextButton_11.MouseButton1Click:Connect(function()
		if Player.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
			Player.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(481, 193, 80)
		end
	end)

	UITextSizeConstraint_31.Parent = TextButton_11
	UITextSizeConstraint_31.MaxTextSize = 14

	UIAspectRatioConstraint_46.Parent = TextButton_11
	UIAspectRatioConstraint_46.AspectRatio = 2.504

	UIAspectRatioConstraint_47.Parent = Cheat5_2
	UIAspectRatioConstraint_47.AspectRatio = 6.980

	Cheat6_2.Name = "Cheat6"
	Cheat6_2.Parent = Frame_2
	Cheat6_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat6_2.BackgroundTransparency = 1.000
	Cheat6_2.BorderSizePixel = 0
	Cheat6_2.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel_14.Parent = Cheat6_2
	TextLabel_14.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_14.BackgroundTransparency = 1.000
	TextLabel_14.BorderSizePixel = 0
	TextLabel_14.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel_14.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel_14.Font = Enum.Font.Gotham
	TextLabel_14.Text = "Recrutamento :"
	TextLabel_14.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_14.TextScaled = true
	TextLabel_14.TextSize = 14.000
	TextLabel_14.TextWrapped = true
	TextLabel_14.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_32.Parent = TextLabel_14
	UITextSizeConstraint_32.MaxTextSize = 14

	UIAspectRatioConstraint_48.Parent = TextLabel_14
	UIAspectRatioConstraint_48.AspectRatio = 6.470

	TextButton_12.Parent = Cheat6_2
	TextButton_12.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextButton_12.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextButton_12.Position = UDim2.new(0.691860497, 0, 0.208333328, 0)
	TextButton_12.Size = UDim2.new(0.209302321, 0, 0.583333313, 0)
	TextButton_12.Font = Enum.Font.Gotham
	TextButton_12.Text = "Ir"
	TextButton_12.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton_12.TextScaled = true
	TextButton_12.TextSize = 14.000
	TextButton_12.TextWrapped = true
	TextButton_12.MouseButton1Click:Connect(function()
		if Player.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
			Player.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-6, 193, -83)
		end
	end)

	UITextSizeConstraint_33.Parent = TextButton_12
	UITextSizeConstraint_33.MaxTextSize = 14

	UIAspectRatioConstraint_49.Parent = TextButton_12
	UIAspectRatioConstraint_49.AspectRatio = 2.504

	UIAspectRatioConstraint_50.Parent = Cheat6_2
	UIAspectRatioConstraint_50.AspectRatio = 6.980

	Cheat7.Name = "Cheat7"
	Cheat7.Parent = Frame_2
	Cheat7.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat7.BackgroundTransparency = 1.000
	Cheat7.BorderSizePixel = 0
	Cheat7.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel_15.Parent = Cheat7
	TextLabel_15.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_15.BackgroundTransparency = 1.000
	TextLabel_15.BorderSizePixel = 0
	TextLabel_15.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel_15.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel_15.Font = Enum.Font.Gotham
	TextLabel_15.Text = "Câmeras :"
	TextLabel_15.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_15.TextScaled = true
	TextLabel_15.TextSize = 14.000
	TextLabel_15.TextWrapped = true
	TextLabel_15.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_34.Parent = TextLabel_15
	UITextSizeConstraint_34.MaxTextSize = 14

	UIAspectRatioConstraint_51.Parent = TextLabel_15
	UIAspectRatioConstraint_51.AspectRatio = 6.470

	TextButton_13.Parent = Cheat7
	TextButton_13.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextButton_13.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextButton_13.Position = UDim2.new(0.691860497, 0, 0.208333328, 0)
	TextButton_13.Size = UDim2.new(0.209302321, 0, 0.583333313, 0)
	TextButton_13.Font = Enum.Font.Gotham
	TextButton_13.Text = "Ir"
	TextButton_13.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton_13.TextScaled = true
	TextButton_13.TextSize = 14.000
	TextButton_13.TextWrapped = true
	TextButton_13.MouseButton1Click:Connect(function()
		if Player.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
			Player.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-566, 193, -50)
		end
	end)

	UITextSizeConstraint_35.Parent = TextButton_13
	UITextSizeConstraint_35.MaxTextSize = 14

	UIAspectRatioConstraint_52.Parent = TextButton_13
	UIAspectRatioConstraint_52.AspectRatio = 2.504

	UIAspectRatioConstraint_53.Parent = Cheat7
	UIAspectRatioConstraint_53.AspectRatio = 6.980

	Cheat8.Name = "Cheat8"
	Cheat8.Parent = Frame_2
	Cheat8.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat8.BackgroundTransparency = 1.000
	Cheat8.BorderSizePixel = 0
	Cheat8.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel_16.Parent = Cheat8
	TextLabel_16.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_16.BackgroundTransparency = 1.000
	TextLabel_16.BorderSizePixel = 0
	TextLabel_16.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel_16.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel_16.Font = Enum.Font.Gotham
	TextLabel_16.Text = "Caverna :"
	TextLabel_16.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_16.TextScaled = true
	TextLabel_16.TextSize = 14.000
	TextLabel_16.TextWrapped = true
	TextLabel_16.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_36.Parent = TextLabel_16
	UITextSizeConstraint_36.MaxTextSize = 14

	UIAspectRatioConstraint_54.Parent = TextLabel_16
	UIAspectRatioConstraint_54.AspectRatio = 6.470

	TextButton_14.Parent = Cheat8
	TextButton_14.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextButton_14.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextButton_14.Position = UDim2.new(0.691860497, 0, 0.208333328, 0)
	TextButton_14.Size = UDim2.new(0.209302321, 0, 0.583333313, 0)
	TextButton_14.Font = Enum.Font.Gotham
	TextButton_14.Text = "Ir"
	TextButton_14.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton_14.TextScaled = true
	TextButton_14.TextSize = 14.000
	TextButton_14.TextWrapped = true
	TextButton_14.MouseButton1Click:Connect(function()
		if Player.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
			Player.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-63, 193, 323)
		end
	end)

	UITextSizeConstraint_37.Parent = TextButton_14
	UITextSizeConstraint_37.MaxTextSize = 14

	UIAspectRatioConstraint_55.Parent = TextButton_14
	UIAspectRatioConstraint_55.AspectRatio = 2.504

	UIAspectRatioConstraint_56.Parent = Cheat8
	UIAspectRatioConstraint_56.AspectRatio = 6.980

	Cheat9.Name = "Cheat9"
	Cheat9.Parent = Frame_2
	Cheat9.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Cheat9.BackgroundTransparency = 1.000
	Cheat9.BorderSizePixel = 0
	Cheat9.Size = UDim2.new(1, 0, 0.110091746, 0)

	TextLabel_17.Parent = Cheat9
	TextLabel_17.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_17.BackgroundTransparency = 1.000
	TextLabel_17.BorderSizePixel = 0
	TextLabel_17.Position = UDim2.new(0.0406976752, 0, 0.208333328, 0)
	TextLabel_17.Size = UDim2.new(0.540697694, 0, 0.583333313, 0)
	TextLabel_17.Font = Enum.Font.Gotham
	TextLabel_17.Text = "Parkour :"
	TextLabel_17.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_17.TextScaled = true
	TextLabel_17.TextSize = 14.000
	TextLabel_17.TextWrapped = true
	TextLabel_17.TextXAlignment = Enum.TextXAlignment.Left

	UITextSizeConstraint_38.Parent = TextLabel_17
	UITextSizeConstraint_38.MaxTextSize = 14

	UIAspectRatioConstraint_57.Parent = TextLabel_17
	UIAspectRatioConstraint_57.AspectRatio = 6.470

	TextButton_15.Parent = Cheat9
	TextButton_15.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
	TextButton_15.BorderColor3 = Color3.fromRGB(0, 134, 0)
	TextButton_15.Position = UDim2.new(0.691860497, 0, 0.208333328, 0)
	TextButton_15.Size = UDim2.new(0.209302321, 0, 0.583333313, 0)
	TextButton_15.Font = Enum.Font.Gotham
	TextButton_15.Text = "Ir"
	TextButton_15.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextButton_15.TextScaled = true
	TextButton_15.TextSize = 14.000
	TextButton_15.TextWrapped = true
	TextButton_15.MouseButton1Click:Connect(function()
		if Player.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
			Player.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-281, 243, 104)
		end
	end)

	UITextSizeConstraint_39.Parent = TextButton_15
	UITextSizeConstraint_39.MaxTextSize = 14

	UIAspectRatioConstraint_58.Parent = TextButton_15
	UIAspectRatioConstraint_58.AspectRatio = 2.504

	UIAspectRatioConstraint_59.Parent = Cheat9
	UIAspectRatioConstraint_59.AspectRatio = 6.980

	UIAspectRatioConstraint_60.Parent = Frame_2
	UIAspectRatioConstraint_60.AspectRatio = 0.768

	UIAspectRatioConstraint_61.Parent = Line_2
	UIAspectRatioConstraint_61.AspectRatio = 55.839

	UIAspectRatioConstraint_62.Parent = Bar2
	UIAspectRatioConstraint_62.AspectRatio = 7.977

	UIAspectRatioConstraint_63.Parent = Main
	UIAspectRatioConstraint_63.AspectRatio = 1.943

	repeat wait() until game.Players.LocalPlayer and game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:findFirstChild("Torso") and game.Players.LocalPlayer.Character:findFirstChild("Humanoid") 
	local mouse = game.Players.LocalPlayer:GetMouse() 
	repeat wait() until mouse
	local plr = game.Players.LocalPlayer 
	local torso = plr.Character.Torso 
	local flying = false
	local deb = true 
	local ctrl = {f = 0, b = 0, l = 0, r = 0} 
	local lastctrl = {f = 0, b = 0, l = 0, r = 0} 
	local maxspeed = 80 
	local speed = 10 
	function Fly() 
		local bg = Instance.new("BodyGyro", torso) 
		bg.P = 9e4 
		bg.maxTorque = Vector3.new(9e9, 9e9, 9e9) 
		bg.cframe = torso.CFrame 
		local bv = Instance.new("BodyVelocity", torso) 
		bv.velocity = Vector3.new(0,0.1,0) 
		bv.maxForce = Vector3.new(9e9, 9e9, 9e9) 
		repeat wait() 
			plr.Character.Humanoid.PlatformStand = true 
			if ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0 then 
				speed = speed+.5+(speed/maxspeed) 
				if speed > maxspeed then 
					speed = maxspeed 
				end 
			elseif not (ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0) and speed ~= 0 then 
				speed = speed-1 
				if speed < 0 then 
					speed = 0 
				end 
			end 
			if (ctrl.l + ctrl.r) ~= 0 or (ctrl.f + ctrl.b) ~= 0 then 
				bv.velocity = ((game.Workspace.CurrentCamera.CoordinateFrame.lookVector * (ctrl.f+ctrl.b)) + ((game.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(ctrl.l+ctrl.r,(ctrl.f+ctrl.b)*.2,0).p) - game.Workspace.CurrentCamera.CoordinateFrame.p))*speed 
				lastctrl = {f = ctrl.f, b = ctrl.b, l = ctrl.l, r = ctrl.r} 
			elseif (ctrl.l + ctrl.r) == 0 and (ctrl.f + ctrl.b) == 0 and speed ~= 0 then 
				bv.velocity = ((game.Workspace.CurrentCamera.CoordinateFrame.lookVector * (lastctrl.f+lastctrl.b)) + ((game.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(lastctrl.l+lastctrl.r,(lastctrl.f+lastctrl.b)*.2,0).p) - game.Workspace.CurrentCamera.CoordinateFrame.p))*speed 
			else 
				bv.velocity = Vector3.new(0,0.1,0) 
			end 
			bg.cframe = game.Workspace.CurrentCamera.CoordinateFrame * CFrame.Angles(-math.rad((ctrl.f+ctrl.b)*50*speed/maxspeed),0,0) 
		until not flying 
		ctrl = {f = 0, b = 0, l = 0, r = 0} 
		lastctrl = {f = 0, b = 0, l = 0, r = 0} 
		speed = 0 
		bg:Destroy() 
		bv:Destroy() 
		plr.Character.Humanoid.PlatformStand = false 
	end 
	mouse.KeyDown:connect(function(key) 
		if key:lower() == "e" then 
			if flying then flying = false
			else 
				flying = true
				Fly() 
			end 
		elseif key:lower() == "w" then 
			ctrl.f = 1 
		elseif key:lower() == "s" then 
			ctrl.b = -1 
		elseif key:lower() == "a" then 
			ctrl.l = -1 
		elseif key:lower() == "d" then 
			ctrl.r = 1 
		end 
	end) 
	mouse.KeyUp:connect(function(key) 
		if key:lower() == "w" then 
			ctrl.f = 0 
		elseif key:lower() == "s" then 
			ctrl.b = 0 
		elseif key:lower() == "a" then 
			ctrl.l = 0 
		elseif key:lower() == "d" then 
			ctrl.r = 0 
		end 
	end)
	Fly()

	counter = 1
	local Event = game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest
	while wait(2)do
		if Yeh == false then
		else
			Event:FireServer(ToWords(counter) .. " !", "All")
			counter += 1
		end
	end
else
	StarterGui:SetCore("SendNotification", {
		Title = "Error",
		Text = "Game not supported!",
		Duration = 5,
		Callback = bindable,
	})
end
