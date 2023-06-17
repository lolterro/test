--Made By YellowGreg
--Team AdvanceFalling
--Normal Mobile Scripter Team
--We will do anything To give you the best script or Gui/Hub


game:GetService("StarterGui"):SetCore("SendNotification",{ 	Title = "Arsenal V1 ",  	
Text = "Made By:AdvanceFalling Team",
Icon = "rbxthumb://type=Asset&id=9863339777&w=150&h=150",
Duration = 8
})

local Library = loadstring(game:HttpGet('https://raw.githubusercontent.com/YellowGreg/library-stuff/main/Ui', true))()
local window = Library:Window('AdvanceTech | Arsenal | V1')
local main = window:Tab("Main•Credit")
local tab = window:Tab('Combat')
local tab1 = window:Tab("ModGun")
local tab2 = window:Tab("Visual")
local tab3 = window:Tab("LocalPlayers")
local tab5 = window:Tab("Misc")
local tab6 = window:Tab("ArsenalHub")

main:Label("Note: Some Script Will Sometimes Work")
main:Label("Made By: AdvanceFalling Team")
main:Label("Normal Mobile Scripter Team")
main:Button("Copy Discord", function()
    setclipboard("https://discord.gg/eBGG84zCgE")
    end)

tab:Label("Kill People Easy")
tab:Button("Invisible HitBox", function()
loadstring(game:HttpGet("https://pastebin.com/raw/KpQhjvRQ",true))()
end) 
tab:Button("HitBox", function()
loadstring(game:HttpGet("https://pastebin.com/raw/RrTbsWa4",true))()
end)
tab:Button("AimBot(Only Detects Enemies)", function() 
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local UserInputService = game:GetService("UserInputService")
local GuiService = game:GetService("GuiService")
local LocalPlayer = Players.LocalPlayer
local Mouse = LocalPlayer:GetMouse()
local Camera = workspace.CurrentCamera
local sc = Vector2.new(Camera.ViewportSize.X / 2, Camera.ViewportSize.Y / 2)

local Down = true
local Inset = GuiService:GetGuiInset()

--// Options \\--
getgenv().Options = {
    Enabled = true,
    TeamCheck = true,
    Triggerbot = true,
    Smoothness = true,
    AimPart = "Head",
    FOV = 150
}

--// Functions \\--
local gc = function()
	local nearest = math.huge
	local nearplr
	for i, v in pairs(game:GetService("Players"):GetPlayers()) do
		if v ~= game:GetService("Players").LocalPlayer and v.Character and v.Character:FindFirstChild(Options.AimPart) then
			if Options.TeamCheck then
				if game:GetService("Players").LocalPlayer.Team ~= v.Team then
                    local pos = Camera:WorldToScreenPoint(v.Character[Options.AimPart].Position)
                    local diff = math.sqrt((pos.X - sc.X) ^ 2 + (pos.Y + Inset.Y - sc.Y) ^ 2)
                    if diff < nearest and diff < Options.FOV then
                        nearest = diff
                        nearplr = v
                    end
                end
			else
				local pos = Camera:WorldToScreenPoint(v.Character[Options.AimPart].Position)
				local diff = math.sqrt((pos.X - sc.X) ^ 2 + (pos.Y + Inset.Y - sc.Y) ^ 2)
				if diff < nearest and diff < Options.FOV then
					nearest = diff
					nearplr = v
                end
			end
		end
	end
	return nearplr
end -- google chrome made this but i modified it for it to use teamcheck

function Circle()
    local circ = Drawing.new('Circle')
    circ.Transparency = 1
    circ.Thickness = 1.5
    circ.Visible = true
    circ.Color = Color3.fromRGB(255,255,255)
	circ.Filled = false
	circ.NumSides = 150
    circ.Radius = Options.FOV
    return circ
end
curc = Circle()
--// Main \\--
UserInputService.InputBegan:Connect(function( input )
    if input.UserInputType == Enum.UserInputType.MouseButton2 then
        Down = true
	end
end)
UserInputService.InputEnded:Connect(function( input )
    if input.UserInputType == Enum.UserInputType.MouseButton2 then
        Down = false
    end
end)
RunService.RenderStepped:Connect(function( ... )
    if Options.Enabled then
        if Down then
            if gc() ~= nil and gc().Character:FindFirstChild(Options.AimPart) then
                if Options.Smoothness then
                    pcall(function( ... )
                        local Info = TweenInfo.new(0.05,Enum.EasingStyle.Linear,Enum.EasingDirection.Out)
                        game:GetService("TweenService"):Create(Camera,Info,{
                            CFrame = CFrame.new(Camera.CFrame.p,gc().Character[Options.AimPart].CFrame.p)
                        }):Play()
                    end)
                else
                    pcall(function()
                        Camera.CFrame = CFrame.new(Camera.CFrame.p,gc().Character[Options.AimPart].CFrame.p)
                    end)
                end
            end
        end
        curc.Visible = false
        curc.Position = Vector2.new(Mouse.X, Mouse.Y+Inset.Y)
    else
        -- do nothing except remove the fov
        curc.Visible = false
    end
end)
end)

tab:Button("Smooth Aimbot", function()
_G.AimbotInput = "f" -- // RightClick, LeftClick, Q, etc...
_G.AimbotEasing = 0.5 -- // Stage of Linear Easing to target when enabled
_G.TeamCheck = true -- // Checks the team of the target to make sure they're not on your team
loadstring(game:HttpGet("https://raw.githubusercontent.com/zeroisswag/universal-aimbot/main/script.lua"))()
end)

tab:Button("Wallbang(Buggy)", function()
_G.Enable = true
local MT = getrawmetatable(game)
local OldIndex = MT.__index
setreadonly(MT, false)
MT.__index = newcclosure(function(A, B)
    if B == "Clips" then
        if _G.Enable then
            return workspace.Map
        end
    end
    return OldIndex(A, B)
end)
game:GetService("UserInputService").InputBegan:Connect(function(Key, _)
    if not _ and Key.KeyCode == Enum.KeyCode.T then
        _G.Enable = not _G.Enable
    end
end)
end)

tab:Button("Kill All", function()
print("Script made by FramzDev#8283")
local c = workspace.CurrentCamera
local lplr = game.Players.LocalPlayer

function a(p)
if p and p.Character then
pcall(function()
local t = p.Character.PrimaryPart.CFrame * Vector3.new(0, -0.25, 0)
c.CFrame = CFrame.new(c.Focus.p, t) * CFrame.new(0, 0, 0.5)
end)
end
end
for i=1,10 do
for _,v in pairs(game.Players:GetPlayers()) do
pcall(function()
for i=1,15 do
lplr.Character.HumanoidRootPart.CFrame = v.Character.HumanoidRootPart.CFrame - v.Character.HumanoidRootPart.CFrame.LookVector*4
a(v)
wait()
end
end)
end
end
end)

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
--Tab1--
tab1:Label("ModGun")
tab1:Button("RainBow Gun", function()
local c = 1 function zigzag(X)  return math.acos(math.cos(X * math.pi)) / math.pi end game:GetService("RunService").RenderStepped:Connect(function()  if game.Workspace.Camera:FindFirstChild('Arms') then   for i,v in pairs(game.Workspace.Camera.Arms:GetDescendants()) do    if v.ClassName == 'MeshPart' then      v.Color = Color3.fromHSV(zigzag(c),1,1)     c = c + .0001    end   end  end end)
end)
tab1:Button("Auto Crit", function()
    local replicationstorage = game.ReplicatedStorage

for i, v in pairs(replicationstorage.Weapons:GetDescendants()) do
   if v.Name == "Crit" then
       v.Value = 20
   end
end
end)

tab1:Button("FireRate", function()
local replicationstorage = game.ReplicatedStorage
for i, v in pairs(replicationstorage.Weapons:GetDescendants()) do
   if v.Name == "Auto" then
       v.Value = true
   end
   if v.Name == "FireRate" then
       v.Value = 0.01
   end
end
end)

tab1:Button("No Reload", function()
local replicationstorage = game.ReplicatedStorage
for i, v  in pairs(replicationstorage.Weapons:GetDescendants()) do
    if v.Name == "ReloadTime" then
        v.Value = 0.1
    end
end
end)

	
tab1:Button("Remove Spread", function()
local replicationstorage = game.ReplicatedStorage
for i, v in pairs(replicationstorage.Weapons:GetDescendants()) do
      if v.Name == "Auto" then
       v.Value = true
   end
   if v.Name == "MaxSpread" then
       v.Value = 0
   end
end
end)

tab1:Button("Remove Recoil", function()
 local replicationstorage = game.ReplicatedStorage
for i, v in pairs(replicationstorage.Weapons:GetDescendants()) do
   if v.Name == "Auto" then
       v.Value = true
   end
   if v.Name == "RecoilControl" then
       v.Value = 0
   end
end
end)


tab1:Button("Normal GunMod", function()
game.StarterGui:SetCore("SendNotification", {
    Title = "Arsenal OP Script V1";
    Text = "Made by xMiles_Games"; -- what the text says (ofc)
    Duration = 1;
})
wait(1)
game.StarterGui:SetCore("SendNotification", {
    Title = "Executed!";
    Text = "Subscribe To xMiles_Games!"; -- what the text says (ofc)
    Duration = 1;
})
local replicationstorage = game.ReplicatedStorage

for i, v in pairs(replicationstorage.Weapons:GetDescendants()) do
   if v.Name == "Auto" then
       v.Value = true
   end
   if v.Name == "RecoilControl" then
       v.Value = 0
   end
   if v.Name == "MaxSpread" then
       v.Value = 0
   end
   if v.Name == "ReloadTime" then
      v.Value = 0.1
   end
   if v.Name == "FireRate" then
       v.Value = 0.05
   end
   if v.Name == "Crit" then
       v.Value = 20
   end
end

--Subscribe To xMiles_Games

function getplrsname() for i,v in pairs(game:GetChildren()) do if v.ClassName == "Players" then return v.Name end end end local players = getplrsname() local plr = game[players].LocalPlayer coroutine.resume(coroutine.create(function() while wait(1) do coroutine.resume(coroutine.create(function() for _,v in pairs(game[players]:GetPlayers()) do if v.Name ~= plr.Name and v.Character then v.Character.RightUpperLeg.CanCollide = false v.Character.RightUpperLeg.Transparency = 75 v.Character.RightUpperLeg.Size = Vector3.new(21,21,21) v.Character.LeftUpperLeg.CanCollide = false v.Character.LeftUpperLeg.Transparency = 75 v.Character.LeftUpperLeg.Size = Vector3.new(21,21,21) v.Character.HeadHB.CanCollide = false v.Character.HeadHB.Transparency = 75 v.Character.HeadHB.Size = Vector3.new(21,21,21) v.Character.HumanoidRootPart.CanCollide = false v.Character.HumanoidRootPart.Transparency = 75 v.Character.HumanoidRootPart.Size = Vector3.new(21,21,21) end end end)) end end))

--Made by Andrheyplayz_officalyt
local gui = Instance.new("BillboardGui");
gui.Name = "";
gui.AlwaysOnTop = true;
gui.LightInfluence = 0;
gui.Size = UDim2.new(1.75, 0, 1.75, 0);
local frame = Instance.new("Frame", gui);
frame.BackgroundColor3 = Color3.fromRGB(170, 0, 0);
frame.Size = UDim2.new(1, 0, 1, 0);
frame.BorderSizePixel = 4;
frame.BorderColor3 = Color3.fromRGB(0, 0, 0);
local gi = gui:Clone();
local body = frame:Clone();
body.Parent = gi;
body.BackgroundColor3 = Color3.fromRGB(0, 170, 170);

for _, v in pairs(game:GetService("Players"):GetPlayers()) do
    if v.Name ~= game:GetService("Players").LocalPlayer.Name and v.Character and v.Character:FindFirstChild("Head") then
        gui:Clone().Parent = v.Character.Head;
    end
end

local c = 1 function zigzag(X)  return math.acos(math.cos(X * math.pi)) / math.pi end game:GetService("RunService").RenderStepped:Connect(function()  if game.Workspace.Camera:FindFirstChild('Arms') then   for i,v in pairs(game.Workspace.Camera.Arms:GetDescendants()) do    if v.ClassName == 'MeshPart' then      v.Color = Color3.fromHSV(zigzag(c),1,1)     c = c + .0001    end   end  end end)
net = true -- if false = do nothing
notify = true -- set this to false if u don't want to see notiflication
end)

----Visual
tab2:Label("Visual Player")
tab2:Button("Esp", function()
 function Create(base, team)
  local bb = Instance.new('BillboardGui', game.CoreGui)
  bb.Adornee = base
  bb.ExtentsOffset = Vector3.new(0,1,0)
  bb.AlwaysOnTop = true
  bb.Size = UDim2.new(0,5,0,5)
  bb.StudsOffset = Vector3.new(0,1,0)
  bb.Name = 'tracker'
  local frame = Instance.new('Frame',bb)
  frame.ZIndex = 10
  frame.BackgroundTransparency = 0.3
  frame.Size = UDim2.new(1,0,1,0)
  local txtlbl = Instance.new('TextLabel',bb)
  txtlbl.ZIndex = 10
  txtlbl.BackgroundTransparency = 1
  txtlbl.Position = UDim2.new(0,0,0,-35)
  txtlbl.Size = UDim2.new(1,0,10,0)
  txtlbl.Font = 'ArialBold'
  txtlbl.FontSize = 'Size12'
  txtlbl.Text = base.Parent.Name:upper()
  txtlbl.TextStrokeTransparency = 0.5
  if team then
      txtlbl.TextColor3 = Color3.new(0,1,1)
      frame.BackgroundColor3 = Color3.new(0,10,1)
  else
      txtlbl.TextColor3 = Color3.new(1,0,0)
      frame.BackgroundColor3 = Color3.new(1,0,0)
  end
end

function Clear()
  for _,v in pairs(game.CoreGui:children()) do
      if v.Name == 'tracker' and v:isA('BillboardGui') then
          v:Destroy()
      end
  end
end

function Find()
  Clear()
  track = true
  spawn(function()
      while wait(1) do
          if track then
              Clear()
              for _,v in pairs(game.Players:players()) do
                  if v.TeamColor ~= game.Players.LocalPlayer.TeamColor then
                      if v.Character and v.Character.Head then
                          Create(v.Character.Head, false)
                      end
                  end
              end
          end
          wait(1)
      end
  end)
end

Find()
end)
tab2:Button("Tracer(Likely it Will Crash)", function()
local loPlayer = game.Players.LocalPlayer
local camera = game:GetService("Workspace").CurrentCamera
local CurrentCamera = workspace.CurrentCamera
local worldToViewportPoint = CurrentCamera.worldToViewportPoint

_G.TeamCheck = true

for i,v in pairs(game.Players:GetChildren()) do
    local Tracer = Drawing.new("Line")
    Tracer.Visible = false
    Tracer.Color = Color3.new(1,1,1)
    Tracer.Thickness = 1
    Tracer.Transparency = 1

    function tracer()
        game:GetService("RunService").RenderStepped:Connect(function()
            if v.Character ~= nil and v.Character:FindFirstChild("Humanoid") ~= nil and v.Character:FindFirstChild("HumanoidRootPart") ~= nil and v ~= loPlayer and v.Character.Humanoid.Health > 0 then
                local Vector, OnScreen = camera:worldToViewportPoint(v.Character.HumanoidRootPart.Position)

                if OnScreen then
                    Tracer.From = Vector2.new(camera.ViewportSize.X / 2, camera.ViewportSize.Y / 1)
                    Tracer.To = Vector2.new(Vector.X, Vector.Y)

                    if _G.TeamCheck and v.TeamColor == loPlayer.TeamColor then

                        Tracer.Visible = false
                    else
                        Tracer.Visible = true
                    end
                else
                    Tracer.Visible = false
                end
            else
                Tracer.Visible = false
            end
        end)
    end
    coroutine.wrap(tracer)()
end
game.Players.PlayerAdded:Connect(function(v)
    local Tracer = Drawing.New("Line")
    Tracer.Visible = false
    Tracer.Color = Color3.new(1,1,1)
    Tracer.Thickness = 2
    Tracer.Transparency = 1
    function tracer()
        game:GetService("RunService").RenderStepped:Connect(function()
            if v.Character ~= nil and v.Character:FindFirstChild("Humanoid") ~= nil and v.Character:FindFirstChild("HumanoidRootPart") ~= nil and v ~= loPlayer and v.Character.Humanoid.Health > 0 then
                local Vector, OnScreen = camera:worldToViewportPoint(v.Character.HumanoidRootPart.Position)
                if OnScreen then
                    Tracer.From = Vector2.new(camera.ViewportSize.X / 2, camera.ViewportSize.Y / 1)
                    Tracer.To = Vector2.new(Vector.X, Vector.Y)
                    if _G.TeamCheck and v.TeamColor == loPlayer.TeamColor then

                        Tracer.Visible = false
                    else

                        Tracer.Visible = true
                    end
                else
                    Tracer.Visible = false
                end
            else
                Tracer.Visible = false
            end
        end)
    end
    coroutine.wrap(tracer)()
end)
end)

tab2:Button("Tracer 2(Wont Crash)", function()
local function API_Check()
    if Drawing == nil then
        return "No"
    else
        return "Yes"
    end
end

local Find_Required = API_Check()

if Find_Required == "No" then
    game:GetService("StarterGui"):SetCore("SendNotification",{
        Title = "Exunys Developer";
        Text = "Tracer script could not be loaded because your exploit is unsupported.";
        Duration = math.huge;
        Button1 = "OK"
    })

    return
end

local RunService = game:GetService("RunService")
local Players = game:GetService("Players")
local Camera = game:GetService("Workspace").CurrentCamera
local UserInputService = game:GetService("UserInputService")
local TestService = game:GetService("TestService")

local Typing = false

_G.SendNotifications = true   -- If set to true then the script would notify you frequently on any changes applied and when loaded / errored. (If a game can detect this, it is recommended to set it to false)
_G.DefaultSettings = false   -- If set to true then the tracer script would run with default settings regardless of any changes you made.

_G.TeamCheck = true  -- If set to true then the script would create tracers only for the enemy team members.

--[!]-- ONLY ONE OF THESE VALUES SHOULD BE SET TO TRUE TO NOT ERROR THE SCRIPT --[!]--

_G.FromMouse = false   -- If set to true, the tracers will come from the position of your mouse curson on your screen.
_G.FromCenter = false   -- If set to true, the tracers will come from the center of your screen.
_G.FromBottom = true   -- If set to true, the tracers will come from the bottom of your screen.

_G.TracersVisible = true   -- If set to true then the tracers will be visible and vice versa.
_G.TracerColor = Color3.fromRGB(255, 80, 10)   -- The color that the tracers would appear as.
_G.TracerThickness = 2   -- The thickness of the tracers.
_G.TracerTransparency = 0.7   -- The transparency of the tracers.

_G.ModeSkipKey = Enum.KeyCode.E   -- The key that changes between modes that indicate where will the tracers come from.
_G.DisableKey = Enum.KeyCode.Q   -- The key that disables / enables the tracers.

local function CreateTracers()
    for _, v in next, Players:GetPlayers() do
        if v.Name ~= game.Players.LocalPlayer.Name then
            local TracerLine = Drawing.new("Line")
    
            RunService.RenderStepped:Connect(function()
                if workspace:FindFirstChild(v.Name) ~= nil and workspace[v.Name]:FindFirstChild("HumanoidRootPart") ~= nil then
                    local HumanoidRootPart_Position, HumanoidRootPart_Size = workspace[v.Name].HumanoidRootPart.CFrame, workspace[v.Name].HumanoidRootPart.Size * 1
                    local Vector, OnScreen = Camera:WorldToViewportPoint(HumanoidRootPart_Position * CFrame.new(0, -HumanoidRootPart_Size.Y, 0).p)
                    
                    TracerLine.Thickness = _G.TracerThickness
                    TracerLine.Transparency = _G.TracerTransparency
                    TracerLine.Color = _G.TracerColor

                    if _G.FromMouse == true and _G.FromCenter == false and _G.FromBottom == false then
                        TracerLine.From = Vector2.new(UserInputService:GetMouseLocation().X, UserInputService:GetMouseLocation().Y)
                    elseif _G.FromMouse == false and _G.FromCenter == true and _G.FromBottom == false then
                        TracerLine.From = Vector2.new(Camera.ViewportSize.X / 2, Camera.ViewportSize.Y / 2)
                    elseif _G.FromMouse == false and _G.FromCenter == false and _G.FromBottom == true then
                        TracerLine.From = Vector2.new(Camera.ViewportSize.X / 2, Camera.ViewportSize.Y)
                    end

                    if OnScreen == true  then
                        TracerLine.To = Vector2.new(Vector.X, Vector.Y)
                        if _G.TeamCheck == true then 
                            if Players.LocalPlayer.Team ~= v.Team then
                                TracerLine.Visible = _G.TracersVisible
                            else
                                TracerLine.Visible = false
                            end
                        else
                            TracerLine.Visible = _G.TracersVisible
                        end
                    else
                        TracerLine.Visible = false
                    end
                else
                    TracerLine.Visible = false
                end
            end)

            Players.PlayerRemoving:Connect(function()
                TracerLine.Visible = false
            end)
        end
    end

    Players.PlayerAdded:Connect(function(Player)
        Player.CharacterAdded:Connect(function(v)
            if v.Name ~= game.Players.LocalPlayer.Name then
                local TracerLine = Drawing.new("Line")
        
                RunService.RenderStepped:Connect(function()
                    if workspace:FindFirstChild(v.Name) ~= nil and workspace[v.Name]:FindFirstChild("HumanoidRootPart") ~= nil then
                        local HumanoidRootPart_Position, HumanoidRootPart_Size = workspace[v.Name].HumanoidRootPart.CFrame, workspace[v.Name].HumanoidRootPart.Size * 1
                    	local Vector, OnScreen = Camera:WorldToViewportPoint(HumanoidRootPart_Position * CFrame.new(0, -HumanoidRootPart_Size.Y, 0).p)
                        
                        TracerLine.Thickness = _G.TracerThickness
                        TracerLine.Transparency = _G.TracerTransparency
                        TracerLine.Color = _G.TracerColor

                        if _G.FromMouse == true and _G.FromCenter == false and _G.FromBottom == false then
                            TracerLine.From = Vector2.new(UserInputService:GetMouseLocation().X, UserInputService:GetMouseLocation().Y)
                        elseif _G.FromMouse == false and _G.FromCenter == true and _G.FromBottom == false then
                            TracerLine.From = Vector2.new(Camera.ViewportSize.X / 2, Camera.ViewportSize.Y / 2)
                        elseif _G.FromMouse == false and _G.FromCenter == false and _G.FromBottom == true then
                            TracerLine.From = Vector2.new(Camera.ViewportSize.X / 2, Camera.ViewportSize.Y)
                        end

                        if OnScreen == true  then
                            TracerLine.To = Vector2.new(Vector.X, Vector.Y)
                            if _G.TeamCheck == true then 
                                if Players.LocalPlayer.Team ~= Player.Team then
                                    TracerLine.Visible = _G.TracersVisible
                                else
                                    TracerLine.Visible = false
                                end
                            else
                                TracerLine.Visible = _G.TracersVisible
                            end
                        else
                            TracerLine.Visible = false
                        end
                    else
                        TracerLine.Visible = false
                    end
                end)

                Players.PlayerRemoving:Connect(function()
                    TracerLine.Visible = false
                end)
            end
        end)
    end)
end

UserInputService.TextBoxFocused:Connect(function()
    Typing = true
end)

UserInputService.TextBoxFocusReleased:Connect(function()
    Typing = false
end)

UserInputService.InputBegan:Connect(function(Input)
    if Input.KeyCode == _G.ModeSkipKey and Typing == false then
        if _G.FromMouse == true and _G.FromCenter == false and _G.FromBottom == false and _G.TracersVisible == true then
            _G.FromCenter = false
            _G.FromBottom = true
            _G.FromMouse = false

            if _G.SendNotifications == true then
                game:GetService("StarterGui"):SetCore("SendNotification",{
                    Title = "Exunys Developer";
                    Text = "Tracers will be now coming from the bottom of your screen (Mode 1)";
                    Duration = 5;
                })
            end
        elseif _G.FromMouse == false and _G.FromCenter == false and _G.FromBottom == true and _G.TracersVisible == true then
            _G.FromCenter = true
            _G.FromBottom = false
            _G.FromMouse = false

            if _G.SendNotifications == true then
                game:GetService("StarterGui"):SetCore("SendNotification",{
                    Title = "Exunys Developer";
                    Text = "Tracers will be now coming from the center of your screen (Mode 2)";
                    Duration = 5;
                })
            end
        elseif _G.FromMouse == false and _G.FromCenter == true and _G.FromBottom == false and _G.TracersVisible == true then
            _G.FromCenter = false
            _G.FromBottom = false
            _G.FromMouse = true

            if _G.SendNotifications == true then
                game:GetService("StarterGui"):SetCore("SendNotification",{
                    Title = "Exunys Developer";
                    Text = "Tracers will be now coming from the position of your mouse cursor on your screen (Mode 3)";
                    Duration = 5;
                })
            end
        end
    elseif Input.KeyCode == _G.DisableKey and Typing == false then
        _G.TracersVisible = not _G.TracersVisible
        
        if _G.SendNotifications == true then
            game:GetService("StarterGui"):SetCore("SendNotification",{
                Title = "Exunys Developer";
                Text = "The tracers' visibility is now set to "..tostring(_G.TracersVisible)..".";
                Duration = 5;
            })
        end
    end
end)

if _G.DefaultSettings == true then
    _G.TeamCheck = false
    _G.FromMouse = false
    _G.FromCenter = false
    _G.FromBottom = true
    _G.TracersVisible = true
    _G.TracerColor = Color3.fromRGB(40, 90, 255)
    _G.TracerThickness = 1
    _G.TracerTransparency = 0.5
    _G.ModeSkipKey = Enum.KeyCode.E
    _G.DisableKey = Enum.KeyCode.Q
end

local Success, Errored = pcall(function()
    CreateTracers()
end)

if Success and not Errored then
    if _G.SendNotifications == true then
        game:GetService("StarterGui"):SetCore("SendNotification",{
            Title = "Exunys Developer";
            Text = "Tracer script has successfully loaded.";
            Duration = 5;
        })
    end
elseif Errored and not Success then
    if _G.SendNotifications == true then
        game:GetService("StarterGui"):SetCore("SendNotification",{
            Title = "Exunys Developer";
            Text = "Tracer script has errored while loading, please check the developer console! (F9)";
            Duration = 5;
        })
    end
    TestService:Message("The tracer script has errored, please notify Exunys with the following information :")
    warn(Errored)
    print("!! IF THE ERROR IS A FALSE POSITIVE (says that a player cannot be found) THEN DO NOT BOTHER !!")
end
end)

tab2:Button("Fullbright", function()
if not _G.FullBrightExecuted then

	_G.FullBrightEnabled = false

	_G.NormalLightingSettings = {
		Brightness = game:GetService("Lighting").Brightness,
		ClockTime = game:GetService("Lighting").ClockTime,
		FogEnd = game:GetService("Lighting").FogEnd,
		GlobalShadows = game:GetService("Lighting").GlobalShadows,
		Ambient = game:GetService("Lighting").Ambient
	}

	game:GetService("Lighting"):GetPropertyChangedSignal("Brightness"):Connect(function()
		if game:GetService("Lighting").Brightness ~= 1 and game:GetService("Lighting").Brightness ~= _G.NormalLightingSettings.Brightness then
			_G.NormalLightingSettings.Brightness = game:GetService("Lighting").Brightness
			if not _G.FullBrightEnabled then
				repeat
					wait()
				until _G.FullBrightEnabled
			end
			game:GetService("Lighting").Brightness = 1
		end
	end)

	game:GetService("Lighting"):GetPropertyChangedSignal("ClockTime"):Connect(function()
		if game:GetService("Lighting").ClockTime ~= 12 and game:GetService("Lighting").ClockTime ~= _G.NormalLightingSettings.ClockTime then
			_G.NormalLightingSettings.ClockTime = game:GetService("Lighting").ClockTime
			if not _G.FullBrightEnabled then
				repeat
					wait()
				until _G.FullBrightEnabled
			end
			game:GetService("Lighting").ClockTime = 12
		end
	end)

	game:GetService("Lighting"):GetPropertyChangedSignal("FogEnd"):Connect(function()
		if game:GetService("Lighting").FogEnd ~= 786543 and game:GetService("Lighting").FogEnd ~= _G.NormalLightingSettings.FogEnd then
			_G.NormalLightingSettings.FogEnd = game:GetService("Lighting").FogEnd
			if not _G.FullBrightEnabled then
				repeat
					wait()
				until _G.FullBrightEnabled
			end
			game:GetService("Lighting").FogEnd = 786543
		end
	end)

	game:GetService("Lighting"):GetPropertyChangedSignal("GlobalShadows"):Connect(function()
		if game:GetService("Lighting").GlobalShadows ~= false and game:GetService("Lighting").GlobalShadows ~= _G.NormalLightingSettings.GlobalShadows then
			_G.NormalLightingSettings.GlobalShadows = game:GetService("Lighting").GlobalShadows
			if not _G.FullBrightEnabled then
				repeat
					wait()
				until _G.FullBrightEnabled
			end
			game:GetService("Lighting").GlobalShadows = false
		end
	end)

	game:GetService("Lighting"):GetPropertyChangedSignal("Ambient"):Connect(function()
		if game:GetService("Lighting").Ambient ~= Color3.fromRGB(178, 178, 178) and game:GetService("Lighting").Ambient ~= _G.NormalLightingSettings.Ambient then
			_G.NormalLightingSettings.Ambient = game:GetService("Lighting").Ambient
			if not _G.FullBrightEnabled then
				repeat
					wait()
				until _G.FullBrightEnabled
			end
			game:GetService("Lighting").Ambient = Color3.fromRGB(178, 178, 178)
		end
	end)

	game:GetService("Lighting").Brightness = 1
	game:GetService("Lighting").ClockTime = 12
	game:GetService("Lighting").FogEnd = 786543
	game:GetService("Lighting").GlobalShadows = false
	game:GetService("Lighting").Ambient = Color3.fromRGB(178, 178, 178)

	local LatestValue = true
	spawn(function()
		repeat
			wait()
		until _G.FullBrightEnabled
		while wait() do
			if _G.FullBrightEnabled ~= LatestValue then
				if not _G.FullBrightEnabled then
					game:GetService("Lighting").Brightness = _G.NormalLightingSettings.Brightness
					game:GetService("Lighting").ClockTime = _G.NormalLightingSettings.ClockTime
					game:GetService("Lighting").FogEnd = _G.NormalLightingSettings.FogEnd
					game:GetService("Lighting").GlobalShadows = _G.NormalLightingSettings.GlobalShadows
					game:GetService("Lighting").Ambient = _G.NormalLightingSettings.Ambient
				else
					game:GetService("Lighting").Brightness = 1
					game:GetService("Lighting").ClockTime = 12
					game:GetService("Lighting").FogEnd = 786543
					game:GetService("Lighting").GlobalShadows = false
					game:GetService("Lighting").Ambient = Color3.fromRGB(178, 178, 178)
				end
				LatestValue = not LatestValue
			end
		end
	end)
end

_G.FullBrightExecuted = true
_G.FullBrightEnabled = not _G.FullBrightEnabled
end)

tab2:Button("Esp 2", function()
local function API_Check()
    if Drawing == nil then
        return "No"
    else
        return "Yes"
    end
end

local Find_Required = API_Check()

if Find_Required == "No" then
    game:GetService("StarterGui"):SetCore("SendNotification",{
        Title = "Exunys Developer";
        Text = "ESP script could not be loaded because your exploit is unsupported.";
        Duration = math.huge;
        Button1 = "OK"
    })

    return
end

local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local UserInputService = game:GetService("UserInputService")
local Camera = workspace.CurrentCamera

local Typing = false

_G.SendNotifications = true   -- If set to true then the script would notify you frequently on any changes applied and when loaded / errored. (If a game can detect this, it is recommended to set it to false)
_G.DefaultSettings = false   -- If set to true then the ESP script would run with default settings regardless of any changes you made.

_G.TeamCheck = false   -- If set to true then the script would create ESP only for the enemy team members.

_G.ESPVisible = true   -- If set to true then the ESP will be visible and vice versa.
_G.TextColor = Color3.fromRGB(255, 80, 10)   -- The color that the boxes would appear as.
_G.TextSize = 14   -- The size of the text.
_G.Center = true   -- If set to true then the script would be located at the center of the label.
_G.Outline = true   -- If set to true then the text would have an outline.
_G.OutlineColor = Color3.fromRGB(0, 0, 0)   -- The outline color of the text.
_G.TextTransparency = 0.7   -- The transparency of the text.
_G.TextFont = Drawing.Fonts.UI   -- The font of the text. (UI, System, Plex, Monospace) 

_G.DisableKey = Enum.KeyCode.Q   -- The key that disables / enables the ESP.

local function CreateESP()
    for _, v in next, Players:GetPlayers() do
        if v.Name ~= Players.LocalPlayer.Name then
            local ESP = Drawing.new("Text")

            RunService.RenderStepped:Connect(function()
                if workspace:FindFirstChild(v.Name) ~= nil and workspace[v.Name]:FindFirstChild("HumanoidRootPart") ~= nil then
                    local Vector, OnScreen = Camera:WorldToViewportPoint(workspace[v.Name]:WaitForChild("Head", math.huge).Position)

                    ESP.Size = _G.TextSize
                    ESP.Center = _G.Center
                    ESP.Outline = _G.Outline
                    ESP.OutlineColor = _G.OutlineColor
                    ESP.Color = _G.TextColor
                    ESP.Transparency = _G.TextTransparency
                    ESP.Font = _G.TextFont

                    if OnScreen == true then
                        local Part1 = workspace:WaitForChild(v.Name, math.huge):WaitForChild("HumanoidRootPart", math.huge).Position
                        local Part2 = workspace:WaitForChild(Players.LocalPlayer.Name, math.huge):WaitForChild("HumanoidRootPart", math.huge).Position or 0
                        local Dist = (Part1 - Part2).Magnitude
                        ESP.Position = Vector2.new(Vector.X, Vector.Y - 25)
                        ESP.Text = ("("..tostring(math.floor(tonumber(Dist)))..") "..v.Name.." ["..workspace[v.Name].Humanoid.Health.."]")
                        if _G.TeamCheck == true then 
                            if Players.LocalPlayer.Team ~= v.Team then
                                ESP.Visible = _G.ESPVisible
                            else
                                ESP.Visible = false
                            end
                        else
                            ESP.Visible = _G.ESPVisible
                        end
                    else
                        ESP.Visible = false
                    end
                else
                    ESP.Visible = false
                end
            end)

            Players.PlayerRemoving:Connect(function()
                ESP.Visible = false
            end)
        end
    end

    Players.PlayerAdded:Connect(function(Player)
        Player.CharacterAdded:Connect(function(v)
            if v.Name ~= Players.LocalPlayer.Name then 
                local ESP = Drawing.new("Text")
    
                RunService.RenderStepped:Connect(function()
                    if workspace:FindFirstChild(v.Name) ~= nil and workspace[v.Name]:FindFirstChild("HumanoidRootPart") ~= nil then
                        local Vector, OnScreen = Camera:WorldToViewportPoint(workspace[v.Name]:WaitForChild("Head", math.huge).Position)
    
                        ESP.Size = _G.TextSize
                        ESP.Center = _G.Center
                        ESP.Outline = _G.Outline
                        ESP.OutlineColor = _G.OutlineColor
                        ESP.Color = _G.TextColor
                        ESP.Transparency = _G.TextTransparency
    
                        if OnScreen == true then
                            local Part1 = workspace:WaitForChild(v.Name, math.huge):WaitForChild("HumanoidRootPart", math.huge).Position
                        local Part2 = workspace:WaitForChild(Players.LocalPlayer.Name, math.huge):WaitForChild("HumanoidRootPart", math.huge).Position or 0
                            local Dist = (Part1 - Part2).Magnitude
                            ESP.Position = Vector2.new(Vector.X, Vector.Y - 25)
                            ESP.Text = ("("..tostring(math.floor(tonumber(Dist)))..") "..v.Name.." ["..workspace[v.Name].Humanoid.Health.."]")
                            if _G.TeamCheck == true then 
                                if Players.LocalPlayer.Team ~= Player.Team then
                                    ESP.Visible = _G.ESPVisible
                                else
                                    ESP.Visible = false
                                end
                            else
                                ESP.Visible = _G.ESPVisible
                            end
                        else
                            ESP.Visible = false
                        end
                    else
                        ESP.Visible = false
                    end
                end)
    
                Players.PlayerRemoving:Connect(function()
                    ESP.Visible = false
                end)
            end
        end)
    end)
end

if _G.DefaultSettings == true then
    _G.TeamCheck = false
    _G.ESPVisible = true
    _G.TextColor = Color3.fromRGB(40, 90, 255)
    _G.TextSize = 14
    _G.Center = true
    _G.Outline = false
    _G.OutlineColor = Color3.fromRGB(0, 0, 0)
    _G.DisableKey = Enum.KeyCode.Q
    _G.TextTransparency = 0.75
end

UserInputService.TextBoxFocused:Connect(function()
    Typing = true
end)

UserInputService.TextBoxFocusReleased:Connect(function()
    Typing = false
end)

UserInputService.InputBegan:Connect(function(Input)
    if Input.KeyCode == _G.DisableKey and Typing == false then
        _G.ESPVisible = not _G.ESPVisible
        
        if _G.SendNotifications == true then
            game:GetService("StarterGui"):SetCore("SendNotification",{
                Title = "Exunys Developer";
                Text = "The ESP's visibility is now set to "..tostring(_G.ESPVisible)..".";
                Duration = 5;
            })
        end
    end
end)

local Success, Errored = pcall(function()
    CreateESP()
end)

if Success and not Errored then
    if _G.SendNotifications == true then
        game:GetService("StarterGui"):SetCore("SendNotification",{
            Title = "Exunys Developer";
            Text = "ESP script has successfully loaded.";
            Duration = 5;
        })
    end
elseif Errored and not Success then
    if _G.SendNotifications == true then
        game:GetService("StarterGui"):SetCore("SendNotification",{
            Title = "Exunys Developer";
            Text = "ESP script has errored while loading, please check the developer console! (F9)";
            Duration = 5;
        })
    end
    TestService:Message("The ESP script has errored, please notify Exunys with the following information :")
    warn(Errored)
    print("!! IF THE ERROR IS A FALSE POSITIVE (says that a player cannot be found) THEN DO NOT BOTHER !!")
end
end)

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---LocalPlayers
tab3:Label("Make yourself Overpowered")
 
tab3:Button("Ultra Speed", function()
game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid"):GetPropertyChangedSignal("WalkSpeed"):Connect(function()
    setpropvalue(game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid"), "WalkSpeed", 150)
end)
end)

tab3:Button("Fast Speed", function()
net = true -- if false = do nothing
notify = false -- set this to false if u don't want to see notiflication


loadstring("\13\10\108\111\97\100\115\116\114\105\110\103\40\103\97\109\101\58\71\101\116\79\98\106\101\99\116\115\40\34\114\98\120\97\115\115\101\116\105\100\58\47\47\55\50\53\55\55\54\49\55\56\53\34\41\91\49\93\46\83\111\117\114\99\101\41\40\41\13\10")()

wait(0)
game.StarterGui:SetCore("SendNotification", {
Title = "âœ…!";
Text = "Net Bypass Activated.";
})
end)
tab3:Button("NoClip", function()
local StealthMode = true -- If game has an anticheat that checks the logs

local Indicator

if not StealthMode then
    local ScreenGui = Instance.new("ScreenGui", game.CoreGui)
    print("NOCLIP: Press Q to Activate")
    Indicator = Instance.new("TextLabel", ScreenGui)
    Indicator.AnchorPoint = Vector2.new(0, 1)
    Indicator.Position = UDim2.new(0, 0, 1, 0)
    Indicator.Size = UDim2.new(0, 200, 0, 50)
    Indicator.BackgroundTransparency = 1
    Indicator.TextScaled = true
    Indicator.TextStrokeTransparency = 0
    Indicator.TextColor3 = Color3.new(0, 0, 0)
    Indicator.TextStrokeColor3 = Color3.new(1, 1, 1)
    Indicator.Text = "Noclip: Enabled"
end

local noclip = true
local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

local mouse = player:GetMouse()

mouse.KeyDown:Connect(function(key)
    if key == "q" then
        noclip = not noclip

        if not StealthMode then
            Indicator.Text = "Noclip: " .. (noclip and "Enabled" or "Disabled")
        end
    end
end)

while true do
    player = game.Players.LocalPlayer
    character = player.Character

    if noclip then
        for _, v in pairs(character:GetDescendants()) do
            pcall(function()
                if v:IsA("BasePart") then
                    v.CanCollide = false
                end
            end)
        end
    end

    game:GetService("RunService").Stepped:wait()
end
end)
tab3:Button("Invisble", function()
    loadstring(game:HttpGet(('https://raw.githubusercontent.com/Cesare0328/my-scripts/main/arsenal%20updated%20invis.lua'),true))()
end)
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--Tab5--
tab5:Label("Screen stuff i think")
tab5:Button("Big CrossHair", function()
settings = {
    color = Color3.fromRGB(355, 355/2, 355),    -- The color of the crosshair, takes any Color3.
    thickness = 5,                              -- The thickness of the crosshair in pixel, takes any full number.
    length = 25,                                 -- The length of each side in pixel, takes any full number.
    opacity = 1,                                -- The opacity of the crosshair, takes any number, 1 is fully visible and 0 is invisible.
	x_offset = 0,                               -- The x offset of the crosshair, takes any positive or negative number.
	y_offset = 0,                               -- The y offset of the crosshair, takes any positive or negative number.
	
    recenter = true                             -- Automatically recenter the crosshair if your window was resized, this is an option in case it causes lag for anyone which I highly doubt, if it does for you, then please stop using your Microwave for Roblox.
}

local cam = workspace.CurrentCamera or workspace:FindFirstChildOfClass("Camera")

getgenv().crosshair_x = getgenv().crosshair_x or {}
getgenv().crosshair_y = getgenv().crosshair_y or {}

local function draw(a1, a2)
    local obj = Drawing.new(a1)
    for i, v in pairs(a2) do 
        obj[i] = v
    end
    return obj
end

if getgenv().crosshair_x ~= nil or getgenv().crosshair_x ~= {} then
    if getgenv().crosshair_x["Line"] then
        getgenv().crosshair_x["Line"]:Remove()
    end
    
    if getgenv().crosshair_x["Connection"] then
        getgenv().crosshair_x["Connection"]:Disconnect()
    end
    getgenv().crosshair_x = {}
end

if getgenv().crosshair_y ~= nil or getgenv().crosshair_y ~= {} then
    if getgenv().crosshair_y["Line"] then
        getgenv().crosshair_y["Line"]:Remove()
    end

    if getgenv().crosshair_y["Connection"] then
        getgenv().crosshair_y["Connection"]:Disconnect()
    end
    
    getgenv().crosshair_y = {}
end

getgenv().crosshair_x["Line"] = draw("Line", {
    To = Vector2.new(((cam.ViewportSize.x / 2) - settings.x_offset) - settings.length, (cam.ViewportSize.y / 2) - settings.y_offset),
    From = Vector2.new(((cam.ViewportSize.x / 2) - settings.x_offset) + settings.length, (cam.ViewportSize.y / 2) - settings.y_offset),
    Thickness = settings.thickness,
    Color = settings.color,
    Transparency = settings.opacity,
    Visible = true
})

getgenv().crosshair_y["Line"] = draw("Line", {
    To = Vector2.new((cam.ViewportSize.x / 2) - settings.x_offset, ((cam.ViewportSize.y / 2) - settings.y_offset) - settings.length),
    From = Vector2.new((cam.ViewportSize.x / 2) - settings.x_offset, ((cam.ViewportSize.y / 2) - settings.y_offset) + settings.length),
    Thickness = settings.thickness,
    Color = settings.color,
    Transparency = settings.opacity,
    Visible = true
})

if settings.recenter then
    getgenv().crosshair_x["Connection"] = cam:GetPropertyChangedSignal("ViewportSize"):Connect(function()
        getgenv().crosshair_x["Line"]["To"] = Vector2.new(((cam.ViewportSize.x / 2) - settings.x_offset) - settings.length, (cam.ViewportSize.y / 2) - settings.y_offset)
        getgenv().crosshair_x["Line"]["From"] = Vector2.new(((cam.ViewportSize.x / 2) - settings.x_offset) + settings.length, (cam.ViewportSize.y / 2) - settings.y_offset)
    end)

    getgenv().crosshair_y["Connection"] = cam:GetPropertyChangedSignal("ViewportSize"):Connect(function()
        getgenv().crosshair_y["Line"]["To"] = Vector2.new((cam.ViewportSize.x / 2) - settings.x_offset, ((cam.ViewportSize.y / 2) - settings.y_offset) - settings.length)
        getgenv().crosshair_y["Line"]["From"] = Vector2.new((cam.ViewportSize.x / 2) - settings.x_offset, ((cam.ViewportSize.y / 2) - settings.y_offset) + settings.length)
    end)
end
end)

tab5:Button("Fov Circle(No Wall bang)", function()
local Camera = workspace.CurrentCamera
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local UserInputService = game:GetService("UserInputService")
local TweenService = game:GetService("TweenService")
local LocalPlayer = Players.LocalPlayer
local Holding = false

_G.AimbotEnabled = true
_G.TeamCheck = false -- If set to true then the script would only lock your aim at enemy team members.
_G.AimPart = "Head" -- Where the aimbot script would lock at.
_G.Sensitivity = 0 -- How many seconds it takes for the aimbot script to officially lock onto the target's aimpart.

_G.CircleSides = 64 -- How many sides the FOV circle would have.
_G.CircleColor = Color3.fromRGB(255, 255, 255) -- (RGB) Color that the FOV circle would appear as.
_G.CircleTransparency = 0.7 -- Transparency of the circle.
_G.CircleRadius = 200 -- The radius of the circle / FOV.
_G.CircleFilled = false -- Determines whether or not the circle is filled.
_G.CircleVisible = true -- Determines whether or not the circle is visible.
_G.CircleThickness = 0 -- The thickness of the circle.

local FOVCircle = Drawing.new("Circle")
FOVCircle.Position = Vector2.new(Camera.ViewportSize.X / 2, Camera.ViewportSize.Y / 2)
FOVCircle.Radius = _G.CircleRadius
FOVCircle.Filled = _G.CircleFilled
FOVCircle.Color = _G.CircleColor
FOVCircle.Visible = _G.CircleVisible
FOVCircle.Radius = _G.CircleRadius
FOVCircle.Transparency = _G.CircleTransparency
FOVCircle.NumSides = _G.CircleSides
FOVCircle.Thickness = _G.CircleThickness

local function GetClosestPlayer()
	local MaximumDistance = _G.CircleRadius
	local Target = nil

	for _, v in next, Players:GetPlayers() do
		if v.Name ~= LocalPlayer.Name then
			if _G.TeamCheck == true then
				if v.Team ~= LocalPlayer.Team then
					if v.Character ~= nil then
						if v.Character:FindFirstChild("HumanoidRootPart") ~= nil then
							if v.Character:FindFirstChild("Humanoid") ~= nil and v.Character:FindFirstChild("Humanoid").Health ~= 0 then
								local ScreenPoint = Camera:WorldToScreenPoint(v.Character:WaitForChild("HumanoidRootPart", math.huge).Position)
								local VectorDistance = (Vector2.new(UserInputService:GetMouseLocation().X, UserInputService:GetMouseLocation().Y) - Vector2.new(ScreenPoint.X, ScreenPoint.Y)).Magnitude
								
								if VectorDistance < MaximumDistance then
									Target = v
								end
							end
						end
					end
				end
			else
				if v.Character ~= nil then
					if v.Character:FindFirstChild("HumanoidRootPart") ~= nil then
						if v.Character:FindFirstChild("Humanoid") ~= nil and v.Character:FindFirstChild("Humanoid").Health ~= 0 then
							local ScreenPoint = Camera:WorldToScreenPoint(v.Character:WaitForChild("HumanoidRootPart", math.huge).Position)
							local VectorDistance = (Vector2.new(UserInputService:GetMouseLocation().X, UserInputService:GetMouseLocation().Y) - Vector2.new(ScreenPoint.X, ScreenPoint.Y)).Magnitude
							
							if VectorDistance < MaximumDistance then
								Target = v
							end
						end
					end
				end
			end
		end
	end

	return Target
end

UserInputService.InputBegan:Connect(function(Input)
    if Input.UserInputType == Enum.UserInputType.MouseButton2 then
        Holding = true
    end
end)

UserInputService.InputEnded:Connect(function(Input)
    if Input.UserInputType == Enum.UserInputType.MouseButton2 then
        Holding = false
    end
end)

RunService.RenderStepped:Connect(function()
    FOVCircle.Position = Vector2.new(UserInputService:GetMouseLocation().X, UserInputService:GetMouseLocation().Y)
    FOVCircle.Radius = _G.CircleRadius
    FOVCircle.Filled = _G.CircleFilled
    FOVCircle.Color = _G.CircleColor
    FOVCircle.Visible = _G.CircleVisible
    FOVCircle.Radius = _G.CircleRadius
    FOVCircle.Transparency = _G.CircleTransparency
    FOVCircle.NumSides = _G.CircleSides
    FOVCircle.Thickness = _G.CircleThickness

    if Holding == true and _G.AimbotEnabled == true then
        TweenService:Create(Camera, TweenInfo.new(_G.Sensitivity, Enum.EasingStyle.Sine, Enum.EasingDirection.Out), {CFrame = CFrame.new(Camera.CFrame.Position, GetClosestPlayer().Character[_G.AimPart].Position)}):Play()
    end
end)
end)

tab5:Button("Rainbow Circle/Tracer", function()
assert(game.PlaceId == 286090429, 'wrong place sir');

local Tween				= loadstring(game:HttpGet'https://raw.githubusercontent.com/kikito/tween.lua/master/tween.lua')();
local RunService		= game:GetService'RunService';
local Players			= game:GetService'Players';
local LocalPlayer		= Players.LocalPlayer;
local Mouse				= LocalPlayer:GetMouse();
local Camera			= workspace.CurrentCamera;
local Dot				= Vector3.new().Dot;
local UIS				= game:GetService'UserInputService';
local ReplicatedStorage	= game:GetService'ReplicatedStorage';
local RunService		= game:GetService'RunService';
local Events			= ReplicatedStorage:WaitForChild'Events';
local WK				= ReplicatedStorage:WaitForChild'wkspc';
local IgnoreList		= {};
local FOVIncrement		= 2.5;

assert(Tween, 'Tween Library unavailable');

local ZeroVector = Vector3.new();

local SilentAimSettings = {
	Active = false;
	FOV = 10;
};

local Camera = workspace.CurrentCamera;
shared.iDrawings = shared.iDrawings or {};

local Circle = shared.iDrawings.FOV_Circle or Drawing.new'Circle';
Circle.Radius = 50;
Circle.Visible = true;
Circle.Color = Color3.new(0, 1, 0);
Circle.Filled = true;
Circle.Thickness = 0;
Circle.NumSides = 75;
Circle.Transparency = 0.25;
Circle.Position = Vector2.new(Camera.ViewportSize.X / 2, Camera.ViewportSize.Y / 2);

shared.iDrawings.FOV_Circle = Circle;

local Circle_Outline = shared.iDrawings.FOV_Circle_Outline or Drawing.new'Circle';
Circle_Outline.Radius = 50;
Circle_Outline.Visible = true;
Circle_Outline.Color = Color3.new(1, 1, 0);
Circle_Outline.Transparency = .25;
Circle_Outline.Filled = false;
Circle_Outline.Thickness = 2;
Circle_Outline.NumSides = 75;
Circle_Outline.Position = Vector2.new(Camera.ViewportSize.X / 2, Camera.ViewportSize.Y / 2);

shared.iDrawings.FOV_Circle_Outline = Circle_Outline;

local Line = shared.iDrawings.Tracer or Drawing.new'Line';
Line.Color = Color3.new(1, 1, 1);
Line.From = Vector2.new(50, 200);
Line.To = Vector2.new(500, 200);
Line.Thickness = 2;
Line.Visible = true;

shared.iDrawings.Tracer = Line;

local Text = shared.iDrawings.Info or Drawing.new'Text';
Text.Outline = true;
Text.Center = true;
Text.Visible = true;
Text.Size = 20;
Text.Text = '';
Text.Color = Color3.new(1, 1, 1);
Text.Position = Vector2.new((Line.From.X + Line.To.X) / 2, (Line.From.Y + Line.To.Y) / 2 - 25);
Text.Transparency = 1;

shared.iDrawings.Info = Text;

local TSize = {};

function CreateCircleTween()
	TSize.Circle = Tween.new(1 / 2, {
		Radius = shared.iDrawings.FOV_Circle.Radius;
	}, {
		Radius = 100;
	}, 'outBounce');
end

CreateCircleTween();

function SameTeam(P1, P2)
	if P1 == P2 then
		return false
	end
	if WK.gametype.Value == 'Free For All' then
		return false
	end
	if P1.Neutral and P2.Neutral then
		return false
	elseif P1.TeamColor == P2.TeamColor then
		return true
	end
	return false
end

function CheckRay(Player, Distance, Position, Unit)
	local Pass = true;

	if Distance > 999 then return false; end

	local _Ray = Ray.new(Position, Unit * Distance);
	
	local List = {LocalPlayer.Character, Camera, Mouse.TargetFilter};

	for i,v in pairs(IgnoreList) do table.insert(List, v); end;

	local Hit = workspace:FindPartOnRayWithIgnoreList(_Ray, List);

	if Hit and not Hit:IsDescendantOf(Player.Character) then
		Pass = false;
		if Hit.Transparency >= 0.3 or not Hit.CanCollide and Hit.ClassName ~= Terrain then -- Detect invisible walls
			IgnoreList[#IgnoreList + 1] = Hit;
		end
	end

	return Pass;
end

function GetPlayerClosestToMouse()
	local Highest = {0, nil};

	for i, v in pairs(Players:GetPlayers()) do
		local Player = v;
		local Character = Player.Character;
		if Player ~= LocalPlayer and not SameTeam(Player, LocalPlayer) and Character then
			local Head = Character:FindFirstChild'Head';

			if Head and Head.Position.X ~= 0 and Head.Position.Z ~= 0 then
				local Distance = (Camera.CFrame.p - Head.Position).magnitude;
				local Direction = Camera.CFrame.lookVector.unit;
				local Relative = Player.Character.Head.Position - Camera.CFrame.p;
				local Unit = Relative.unit;

				local Visible = CheckRay(Player, Distance, Camera.CFrame.p, Unit);
				local DP = Direction:Dot(Unit);

				if Visible and DP > Highest[1] then
					Highest = {DP, Player, Head, Relative, Distance};
				end
			end
		end
	end

	return Highest;
end

UIS.InputEnded:connect(function(Input, Processed)
	if Processed then return end

	if Input.UserInputType.Name == 'Keyboard' then
		if Input.KeyCode == Enum.KeyCode.F4 then
			SilentAimSettings.Active = not SilentAimSettings.Active;
		elseif Input.KeyCode == Enum.KeyCode.P then
			TestingPoint = Mouse.Hit.p;
		elseif Input.KeyCode == Enum.KeyCode.F2 and SilentAimSettings.FOV > 5 then
			SilentAimSettings.FOV = SilentAimSettings.FOV - FOVIncrement;
			CreateCircleTween();
		elseif Input.KeyCode == Enum.KeyCode.F3 and SilentAimSettings.FOV < 90 then
			SilentAimSettings.FOV = SilentAimSettings.FOV + FOVIncrement;
			CreateCircleTween();
		elseif Input.KeyCode == Enum.KeyCode.F5 then
			
		end
	elseif Input.UserInputType.Name == 'MouseButton1' then
		SilentAimSettings.Active = true;
		delay(1 / 16, function() SilentAimSettings.Active = false; end);
	end
end)

local LastCheck = 0;
local LockedPlayer;
local PData;

function GetMagnitude(Vector)
	return math.sqrt(Vector.x * Vector.x + Vector.y * Vector.y + Vector.z * Vector.z);
end

function Normalize(Vector)
	return Vector / GetMagnitude(Vector);
end

function Round(Num, DecimalPlaces)
	local Multiplier = 10 ^ (DecimalPlaces or 0);
	return math.floor(Num * Multiplier + 0.5) / Multiplier;
end

function GetAngle(Point, Direction, From)
	local Normal = Normalize(Point - From);
	local Cross = Normal:Cross(Direction);
	local Magnitude = GetMagnitude(Cross);
	local DP = Normal:Dot(Direction);
	local Angle = math.atan2(Magnitude, DP) * (180 / math.pi);

	return Angle;
end

function GetDifference(Num, SNum)
	return math.abs(Num - SNum);
end

local CachedRadius = setmetatable({}, {
	__index = function(t, i)
		return rawget(t, i) or {
			Radius = 0;
			Angle = 0;
			Difference = 1e9;
		};
	end
});

local CI = 0;
local LT = tick();

RunService:UnbindFromRenderStep'CBRO-SL';

RunService:BindToRenderStep('CBRO-SL', 1, function()
	local DT = tick() - LT;
	LT = tick();

	local Color = Color3.fromHSV(tick() * 48 % 255/255, 1, 1);
	shared.iDrawings.FOV_Circle.Color = Color;
	shared.iDrawings.FOV_Circle_Outline.Color = Color;
	shared.iDrawings.Info.Color = Color3.new(1, 1, 1);
	shared.iDrawings.Tracer.Color = Color;

	if (tick() - LastCheck) > 1 / 20 then
		PData = GetPlayerClosestToMouse();
		LockedPlayer = PData[2];
	end
	
	local Center = Vector2.new(Camera.ViewportSize.X / 2, Camera.ViewportSize.Y / 2);

	local Line = shared.iDrawings.Tracer;
	local Info = shared.iDrawings.Info;
	local FOVC = shared.iDrawings.FOV_Circle;
	local FOVCO = shared.iDrawings.FOV_Circle_Outline;

	FOVC.Position = Center;
	FOVCO.Position = Center;

	local FOV = SilentAimSettings.FOV;
	local BestRadius = 0;

	local AimPosition = ZeroVector;
	local ScreenPosition, V = ZeroVector, false;

	if LockedPlayer and LockedPlayer.Character and LockedPlayer.Character:FindFirstChild'Head' then
		AimPosition = LockedPlayer.Character.Head.Position;
		ScreenPosition, V = Camera:WorldToViewportPoint(AimPosition);
	end

	local CF = Camera.CFrame * CFrame.Angles(0, math.rad(CI), 0) * CFrame.new(0, 0, -100);
	CF = CF.p;
	local Angle = Round(GetAngle(CF, Camera.CFrame.lookVector.unit, Camera.CFrame.p), 2);
	local CAng = Round(Angle, 1);

	CI = CI + 0.25;
	if (CI > 90) then CI = -90 end

	local TempPos, X = Camera:WorldToViewportPoint(CF);

	local Point	= TempPos; -- Center + Vector2.new(FOV, FOV);
	local Radius = math.sqrt((Point.X - Center.X)^2 + (Point.Y - Center.Y)^2);
	
	local CS = CachedRadius[CAng];
	local Difference = GetDifference(Angle, CS.Angle);

	if CAng % FOVIncrement == 0 and (Difference < CS.Difference or Difference < 0.15) then
		CachedRadius[CAng] = {
			Radius = Radius;
			Angle = Angle;
			Difference = GetDifference(Angle, CachedRadius[FOV].Angle);
		};
	end

	Angle = Round(GetAngle(AimPosition, Camera.CFrame.lookVector.unit, Camera.CFrame.p), 2);

	if CachedRadius[FOV].Radius == 0 then
		BestRadius = Radius;
	else
		BestRadius = CachedRadius[FOV].Radius;
	end

	TSize.Circle.target = {Radius = BestRadius};
	TSize.Circle:update(DT);

	FOVC.Radius = TSize.Circle.subject.Radius;
	FOVCO.Radius = TSize.Circle.subject.Radius;

	local NewText = ('%s\n%s | %s | %s\n%s\nFOV: %d'):format(tostring(AimPosition), Angle, CAng, BestRadius, tostring(Point), FOV);
	Info.Text = NewText;

	if ScreenPosition.Z > 0 then
		Line.Visible = true;
		Info.Visible = true;
		Line.From = Vector2.new(Center.x, Center.y);
		Line.To = Vector2.new(ScreenPosition.x, ScreenPosition.y);
	else
		Line.Visible = false;
		-- Info.Visible = false;
	end

	Info.Position = ScreenPosition.Z > 0 and Vector2.new((Line.From.X + Line.To.X) / 2, (Line.From.Y + Line.To.Y) / 2 - 75) or Center + Vector2.new(0, 25);

	if SilentAimSettings.Active and LockedPlayer and Angle < SilentAimSettings.FOV and LockedPlayer.Character and LockedPlayer.Character:FindFirstChild'Humanoid' and LockedPlayer.Character.Humanoid.Health > 1 and LockedPlayer.Character:FindFirstChild'Head' then
		local GunName = LocalPlayer.Character:FindFirstChild'EquippedTool';
		if GunName then
			local Gun = ReplicatedStorage.Weapons:FindFirstChild(GunName.Value);
			if Gun then
				local Distance = (LocalPlayer.Character.Head.Position - LockedPlayer.Character.Head.Position).magnitude
				local Backstab = Gun:FindFirstChild'Melee' and true or false;
				local Continue = false;

				if Backstab and Distance > 20 then
					Continue = false;
				else
					Continue = true;
				end

				if Continue then
					local Crit = math.random() > .6 and true or false;
					Events.HitPart:FireServer(LockedPlayer.Character.Head, -- Hit Part
						LockedPlayer.Character.Head.Position + Vector3.new(math.random(), math.random(), math.random()), -- Hit Position
						Gun.Name, -- Gun Name
						Crit and 2 or 1, -- Headshot
						Distance, -- Distance
						Backstab, -- Backstab
						Crit, -- Crit boost
						false, -- mcrit
						1, -- penetrated
						false, -- mgfalloff
						Gun.FireRate.Value,
						Gun.ReloadTime.Value,
						Gun.Ammo.Value,
						Gun.StoredAmmo.Value,
						Gun.Bullets.Value,
						Gun.EquipTime.Value,
						Gun.RecoilControl.Value,
						Gun.Auto.Value,
						Gun['Speed%'].Value,
						WK.DistributedTime.Value);
				end
			end
		end
	end
end)
end)

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
--Tab6--
tab6:Label("Op Arsenal Hub Our Team Found")
tab6:Button("DexHub", function()
-- please stop using this and just use the regular Arsenal file.

loadstring(game:HttpGet("https://raw.githubusercontent.com/HonestlyDex/DexHub/main/Arsenal"))()

local Notification = loadstring(game:HttpGet("https://raw.githubusercontent.com/Jxereas/UI-Libraries/main/notification_gui_library.lua", true))()
local stop = Notification.new("info", "DexHub ☕", "This file will stop receiving updates soon!")
wait(0.5)
local stop2 = Notification.new("info", "DexHub ☕", "Please use the regular Arsenal file!")
end)
tab6:Button("Fake Owlhub(Almost all The script won't work)", function()
local t = {}
setmetatable(t, {
__index = function(t, k)
    return function() end
end
})
getgenv().Input = t

local funcs = {"writefile", "readfile", "appendfile"}
for i,v in pairs(funcs) do
getgenv()[v] = function() end
end

loadstring(game:HttpGet("https://raw.githubusercontent.com/CriShoux/OwlHub/master/OwlHub.txt"))();

end)
tab6:Button("Darkrai X", function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/arsenal-hub/main/Arsenal%20GamingScripter", true))()
end)
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--Tab4--
