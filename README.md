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
