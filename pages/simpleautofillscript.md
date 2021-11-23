# Intro

Before we start it is required to know a few things about Roblox's luau string functions:

### Splitting
```lua
-- splitting a string into parts
 
local str = "yo/lets/go/bro"
local split = string.split(str, "/")
print(split[1], split[2], split[3], split[4])

```
the output would be

`yo lets go bro`
### Matching
```lua
-- looking for string matches

  

local str = "pro is not you cooler!"

  

if string.match(str, "cooler!") then

print("cooler detected")

end
```
output:
`cooler detected`

## Making the script

Now to create the actual script, 
Finished script for lazy people:
```lua
game.Players.PlayerAdded:Connect(function(plr)
	plr.Chatted:Connect(function(msg)
		local plrs = game.Players:GetPlayers()
		for i = 1, #plrs do plrs[i] = plrs[i].Name end
		for i,v in ipairs(plrs) do
			if string.match(v, msg) then
				print("match")
			end
		end
	end)
end)
```

First we hook to the player and their chat,
```lua
game.Players.PlayerAdded:Connect(function(plr)
	plr.Chatted:Connect(function(msg)
	end)
end)
```

Then we get the players and convert their instances into strings,
```lua
game.Players.PlayerAdded:Connect(function(plr)
	plr.Chatted:Connect(function(msg)
	local plrs = game.Players:GetPlayers()
		for i = 1, #plrs do plrs[i] = plrs[i].Name end
	end)
end)
```

finally we add a ipairs loop to loop through the whole table, 
```lua
game.Players.PlayerAdded:Connect(function(plr)
	plr.Chatted:Connect(function(msg)
		local plrs = game.Players:GetPlayers()
		for i = 1, #plrs do plrs[i] = plrs[i].Name end
		for i,v in ipairs(plrs) do
			if string.match(v, msg) then
				print("match")
			end
		end
	end)
end)
```

Now if we wanted to add a whitelist then,
```lua
local w = {
	["yournamehere"] = true;
}
game.Players.PlayerAdded:Connect(function(plr)
	plr.Chatted:Connect(function(msg)
		if not w[plr.Name] then return end
		local plrs = game.Players:GetPlayers()
		for i = 1, #plrs do plrs[i] = plrs[i].Name end
		for i,v in ipairs(plrs) do
			if string.match(v, msg) then
				print("match")
			end
		end
	end)
end)
```

Done!


#### Main Pages  
[Main Page](https://ackreik.github.io/coding-intro/)   
[Page List](https://ackreik.github.io/coding-intro/pages/main)  
