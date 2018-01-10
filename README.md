# Swarmathon Methods
These methods were created with the help of the 2016 Swarmathon high school outreach modules. 

The goal of the high school Swarmathon is to command robots to collect as many "rocks" as possible using as few steps/ticks as possible. This is a representation of a swarm of rovers on the Mars surface, using a 2D, virtual, Netlogo simulation.

## Instructions
Download all files and run the ".nlogo" files on Netlogo. 

1. Setup the field by hitting "Setup".
2. If applicable, adjust parameters such as pen?, turning angle, etc. using the buttons in the interface on the left.
3. When ready, hit the "Go" button to start the simulation. Use "Halt" under "Tools" if the simulation hits a looping point (i.e., the robots are taking a long time to find the last rock)

Requirements:
* Netlogo installation

## Considerations
* In a 2D simulation, the rovers have no regard for spatial or temporal differences when roaming the planet or sending each other messages. In reality, things like battery life, weather, radio signal travel time, and approach in the same area must be taken into consideration.
* Although the bat simulation significantly reduces the number of steps taken compared to random methods, it is still a very high number of steps.
* In the end, the pheromone method (not included; can be found in original module code) most consistently takes the fewest amount of steps. However, it takes the most processing time, and can also take time in reality for the time it takes the rovers to sense or lay down their "pheromones."

## Screenshots

### Initial field setup
<img src="https://github.com/vickyjjj/SwarmathonMethods/blob/master/screenshots/setup.png?raw=true">
Setting: parking lot; blue = rock/tag to be picked up.

### Control: Random movement
<img src="https://github.com/vickyjjj/SwarmathonMethods/blob/master/screenshots/random.png?raw=true">
Random method relies entirely on random movement.

### Bat Method 1
The first bat method allows rovers to send a signal to other rovers in the vicinity when they find a large patch of rocks to be picked up; other rovers who receive this signal will then swarm towards the area for a set number of steps to eradicate the patch before returning to their regular random movement. This is similar to how bats will send echolocation signals to fellow bats in the area when they find a large patch of prey to feast on together.
<img src="https://github.com/vickyjjj/SwarmathonMethods/blob/master/screenshots/ogbatinit.png?raw=true">
Initial movement lines.
<img src="https://github.com/vickyjjj/SwarmathonMethods/blob/master/screenshots/ogbatfinal.png?raw=true">
Final movement lines.

### Bat Method 2
The second bat method works like bat method 1, but instead of random movement, it implements a deterministic square search starting from the outermose square to the innermost square, before implementing random search when it reaches the smallest square path possible. The rovers are staggered so that they have different starting points in their squares.
<img src="https://github.com/vickyjjj/SwarmathonMethods/blob/master/screenshots/bat2init.png?raw=true">
Initial movement lines.
<img src="https://github.com/vickyjjj/SwarmathonMethods/blob/master/screenshots/bat2final.png?raw=true">
Final movement lines.

### Bat Method 3
The third bat method was written to compare the pheromone method and bat method 2. While bat method 2 could occasionally outperform the pheromone method in the number of ticks it used, the pheromone method more consistently reached numbers of the upper 9,000s, while bat method 2 would often get numbers in the 10,000s rather than the 9,000s.

### Glowworm method
The glowworm method works similarly to the bat method but implements some scales accounting for distance and amount of rocks in a single patch. Its result is similar to the bat method and showed no significant improvement from the bat method, so it was ignored.
<img src="https://github.com/vickyjjj/SwarmathonMethods/blob/master/screenshots/glowinit.png?raw=true">
Initial movement lines.
<img src="https://github.com/vickyjjj/SwarmathonMethods/blob/master/screenshots/glowfinal.png?raw=true">
Final movement lines.
