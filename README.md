# Desmos Solar System
A fully accurate 1:1 model of the solar system in Desmos Graphing Calculator
The link to the project is here: [https://www.desmos.com/calculator/ope5xhz8ok](url)

## Structure

Time is measured with the q variable, which utilizes the ticker function to constantly increase at a rate of 1 every second. Using this, the simulation accurately measures time, even if the browser window is not in focus by the user.

Each planet is arranged exactly as far as it is in real life, at the size it is in real life, at the speed it is in real life. They are structured internally within Desmos as circles, with their X and Y positions being set up as a sine function and a cosine function respectively, of the form:

distance from the sun * cos(year length/10.5 seconds * q); or
distance from the sun * sine(year length/10.5 seconds * q)

The reason behind the constant 10.5 seconds is that that is the time it would take for a planet to make a full rotation if the function is sin(q) or cos(q).

Moreover, the function to graphically show the planets themselves is of the form:

(x - Planet_x)^2 + (y - Planet_y)^2 = Planet_radius^2

Where Planet_x and Planet_y are the planets' x and y positions, and Planet_radius is the planet's radius.
