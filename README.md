#Run This Application
Simply open the index.html file located in the root directory
for the mobile porfolio.

Or.. Open the pizza.html file located in the views directory
for the pizza site.

60FPS
=====
To Make sure the site ran at a smooth 60fps, I had to make some small changes to the
views/js/main.js file handled moving the background pizzas.

* The Most Significant change was computing the phase values before the for loop
and not inside of it to prevent recalculationg the values every single time. Since there would
only be five different values for each call to the updatePositions function, I calculated those values and stored the in an array and later referenced those values from within the loop.

* I also made sure I was using efficient selectors such as document.getElemntById and document.getElementsByClassName to make better use of time.

Resizing Pizzas
===============
* The Biggest Problem with this portion of the application was calculating the exact same value inside a while loop. Since the values would not change, moving the outside of the loop massively increased efficiency. This flaw was found in the changePizzaSizes method with dx and newwidth being the repeated calculations.

* I also noticed that the functions determineDx , changePizzaSizes, changeSliderLabel, and sizeSwitcher were being defined every time there was a call to the resizePizzas. This is unecessary since the definitions don't change, so moving them to he global scope results
in less work.
