# Data-Visualization
This respository showcases a data visualization I coded using information from an existing JSON file, which included data on indviduals currently in space (at the time the data was collected). 
What I made: an animation of the two spacecrafts hovering in space, with the astronauts represented by little dots, all labeled at the bottom of the sketch. 

Check out the code here! 
https://editor.p5js.org/Kmorrissey1/full/ARX_q6wz2

# creative goals: 

This project was intended to increase comfort in working with data structures, arrays, and loops. I chose a small data set, uploaded the JSON into the editor of p5.js, and created a representative sketch. I wanted to build off of skills I have been learning in previous sketches. Namely, I wanted an excuse to create a gradient of colors, which I attempted and failed when using the lerpColor function. in my previous design, I learned that you can use map() to convert a data value to a range between 0 and 1, and then use that mapped value in lerpColor() to get a color that smoothly transitions between two colors. I also practiced using arrays in a few different ways! I created stars by using a for loop which allowed me to set 500 possible vectors for stars to appear. The astronauts array is populated by mapping over the astronautsData.people array. Each astronaut's name, craft, and an empty position array are stored in a new object. This uses JavaScript's map() function to transform the data into a new structure.

I also use a for loop to run through each astronaut aboard the ISS, which calculates a position for each astronaut around the ISS, using trigonometric functions (cos() and sin()) to position them in a circular pattern. This directly builds on my trig experiments in my previous sketch, Peace. The map() function maps the astronaut index (i) to an angle between 0 and TWO_PI (a full circle), which is used to calculate the offsets for x and y. I also used the filter() function to create two separate arrays of astronauts—one for those aboard the ISS and another for those aboard Tiangong. Each astronaut is then drawn within their respective spacecraft with a loop. Finally, I used loops to display the names of astronauts aboard the ISS and Tiangong by iterating through the issAstronauts and tiangongAstronauts arrays. Each astronaut's name is drawn in the respective colored text box, with vertical spacing based on the loop index (i). This project gave me a chance to explore animations using trigonometric functions, practice calling info from data structures, and playing with for loops and arrays for creative effect. 

# Challenges:

I could not load the JSON data from a link; I had to upload a copy of it directly into the editor. Granted, the link to the JSON I used was not secure, so I chose to avoid issues. I still don't know why it did not work.

I do not know why I failed to make lerpColor happen before; I knew that map could be used with it to create smooth color transitions, but it was impossible for me to make it work with a moving object despite watching and following a few tutorials. I avoided that issue in this sketch by making the gradient the background, but I would like to make something more interactive with this function combination. 

Not all of the names appear from the ISS. I thought maybe it had to do with the text boxes, but even when I created two boxes, three names did not appear. I don't know why my code does not go through the whole list of names in the JSON. This could probably be solved by more debugging. 

JSON: http://api.open-notify.org/astros.json
