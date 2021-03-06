# Challenge 1: Rocket Fuel
You are on a spacecraft and you're waiting for launch.

The team at mission control are going through the pre-launch checks.

As the team are running through the Go/No-Go checks, everything is going smoothly until the "Fuel Counter-Upper" person! He hasn't done his job and determined the amount of fuel required yet.

Fuel required to launch a given module is based on its mass. Specifically, **to find the fuel required for a module, take its mass, divide by three, round down, and subtract 2**.

For example:

- For a mass of 12, divide by 3 and round down to get 4, then subtract 2 to get 2.
- For a mass of 14, dividing by 3 and rounding down still yields 4, so the fuel required is also 2.
- For a mass of 1969, the fuel required is 654.
- For a mass of 100756, the fuel required is 33583.

The Fuel Counter-Upper needs to know the total fuel requirement. To find it, individually calculate the fuel needed for the mass of each module (your puzzle input), then add together all the fuel values.

What is the sum of the fuel requirements for all of the modules on your spacecraft?

The module masses can be found [here](https://github.com/pixelrunner/Meraki-ISE-Python-Challenges/blob/master/Challenge_1/Module_masses.txt).

Upload your script(s)to github, and send your answer to John on teams (don't put it in the team chat)! Then move on to part 2.

-----

# Part 2
OK, so you've worked out the amount of fuel you need and that has been added to your ship.

The Go/No-Go checks can continue, the person in charge of the "Rocket Equation Double-Checker" stops the launch sequence. Apparently, you forgot to include additional fuel for the fuel you just added.

Fuel itself requires fuel just like a module - take its mass, divide by three, round down, and subtract 2. However, **that fuel also requires fuel, and that fuel requires fuel, and so on**. Any mass that would require negative fuel should instead be treated as if it requires zero fuel; the remaining mass, if any, is outside the scope of this calculation.

**So, for each module mass, calculate its fuel and add it to the total. Then, treat the fuel amount you just calculated as the input mass and repeat the process, continuing until a fuel requirement is zero or negative.**

For example:

- A module of mass 14 requires 2 fuel. This fuel requires no further fuel (2 divided by 3 and rounded down is 0, which would call for a negative fuel), so the total fuel required is still just 2.
- At first, a module of mass 1969 requires 654 fuel. Then, this fuel requires 216 more fuel (654 / 3 - 2). 216 then requires 70 more fuel, which requires 21 fuel, which requires 5 fuel, which requires no further fuel. So, the total fuel required for a module of mass 1969 is 654 + 216 + 70 + 21 + 5 = 966.
- The fuel required by a module of mass 100756 and its fuel is: 33583 + 11192 + 3728 + 1240 + 411 + 135 + 43 + 12 + 2 = 50346.

What is the sum of the fuel requirements for all of the modules on your spacecraft when also taking into account the mass of the added fuel? (Calculate the fuel requirements for each module separately, then add them all up at the end.)

Upload your script(s)to github (don't worry if it's part of the "part 1" script), and relax; safe in the knowledge you now have enough fuel to take off.
