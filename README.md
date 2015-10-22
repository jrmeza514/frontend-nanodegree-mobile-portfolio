#Run This Application
Simply open the index.html file located in the root directory
for the mobile porfolio.

Or.. Open the pizza.html file located in the views directory
for the pizza site.

##Optimizations
60FPS
=====
To Make sure the site ran at a smooth 60fps, I had to make some small changes to the
views/js/main.js file handled moving the background pizzas.

* The Most Significant change was computing the phase values before the for loop
and not inside of it
