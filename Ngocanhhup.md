
local egg = script.Parent
local owner = nil

egg.Touched:Connect(function(hit)
    local player = game.Players:GetPlayerFromCharacter(hit.Parent)
    if player and owner ~= player then
        owner = player
        egg.BrickColor = player.TeamColor
        print(player.Name .. " đã lấy trứng!")
    end
end)
