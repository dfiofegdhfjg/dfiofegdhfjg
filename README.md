local Library = local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("CUSTOM GUI", "Ocean")

--TABS
local Main = Window:NewTab("Main")
local MainSection = Main:NewSection("Main")


MainSection:NewButton("Flips!", "FLIP OVER ANYONE!!!", function()
    loadstring(game:HttpGet("https://pastebin.com/raw/7wDcPtLk"))()
end)

MainSection:NewToggle("Super-Human", "Makes You Fast With Speed and JumpPower", function(state)
    if state then
        game.Players.LocalPlayer.Character.Humanoid.walkspeed = 120
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = 120
    else
        game.Players.LocalPlayer.Character.Humanoid.walkspeed = 16
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = 50
    end
end)

MainSection:NewButton("Inf yield", "cmds ig.", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyeld/master/source",true))()
end)

--Local Player.
local Player = Window:NewTab("Local Player.")
local PlayerSection = Tab:NewSection("Player")

PlayerSection:NewSlider("Speed", "max is 500", 500, 16, function(s) -- 500 (MaxValue) | 0 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)
