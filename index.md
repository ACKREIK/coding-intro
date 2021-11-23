
## Introduction

Code is built with a lot of different things, variables, functions, loops, and data streams. Variables are especially important and have many distinct types. The most important of the bunch are Booleans which store true & false, int values that carry numbers, and string values. Inside of normal machine code you can use other scripts functions and components by referencing them.


Math is very closely related to coding, specifically coefficients, constants, and a lot of variables. In code you will be using math a lot, want to check if one value is bigger? You use math, coefficients are the first numbers in an equation, for example:
```lua
local val = 10
local HWID = syn.hw:GetHWID()
print((10 * val) + HWID)
```
The 10 is a coefficient, and the `val` is a variable, while the HWID is a constant.

![](https://www.math.net/img/a/algebra/variables/constant/eq.svg)

The four operations you can reference in code are `+`, `-`, `/`, and `*`.





# Functions, Variables, Loops, And DStreams. 
This is how to do each of the common types
```lua
-- you can do '--' to add comments.
--Functions
function crossdivide(div, divisor, cross)
-- code
end
-- running functions
crossdivide(1, 12, '*')



-- Variables
local string = "String"
local int = 4
local bool = true



-- Loops
local v = true
while wait() do -- only repeats something during wait()
--[[ 
using wait() is a good practice, it allows you to do while true loops
without using wait().

to make a loop that is while value thingy do then add an if inside of this,
its a better practice

]]
if v then
print('pog')
end
end

local pro = false

repeat -- prints hamburger once.
print("hamburger")
until not pro

```

## Breaks and Returns.
Now for a very important thing, returns and loop breaks.
Returns will stop the function in a script and are pretty strange to work with but after a while you will get used to it.

The ONLY time you should use a break is during a loop:
```lua
local V = 0
while wait(1) do
		if V < 100 then
		V = V + 1 -- add one every second
		else
		V = 100
		break -- break the loop when passed
		end
end

V = 100
repeat
wait(1)
V = V - 1
if V = 50 then
	print("reached half")
	break -- stops loop
end
until V < 1
```
Returns are going to be used a ton.
```lua
function getMag(hit, part)
	local mag = (hit.Position - part.Position).Magnitude
	return(mag)
end

local plr = game.Players.LocalPlayer
local mouse = plr:GetMouse()
local uis = game:GetService("UserInputService")

uis.InputBegan:Connect(function(hit, pro)
	if pro then
		return(pro)
	end

	if hit.UserInputType == Enum.UserInputType.MouseButton1 then
		local hit = mouse.Hit
		local part = plr.Character.HumanoidRootPart
		if getMag(hit, part) > 100 then
			print("Out Of Range!")
		else
			part.Position = hit.Position
		end
	end
end)
```
What that script does it teleport you to your mouse if it is less than 100 studs away.

You have now finished the tutorial! Move onto the
[Simple Autofill Script](https://ackreik.github.io/coding-intro/pages/simpleautofillscript)




#### Main Pages  
[Main Page](https://ackreik.github.io/coding-intro/)   
[Page List](https://ackreik.github.io/coding-intro/pages/main)  
