The figure above provides a graphical representation of a plant in which 2 Rovers (yellow and blue circles) on a remote planet move on specific area that can be though of as being represented as a (4×6) grid.

The rover can move up, down, left, right within the boundaries of the grid.

The coordinate (x,y)=(1,1) is related to left-bottom corner.

Initially, the yellow rover is in position (3,4), whereas the blue rover is in position (4,1). If the rover sits on a red tile, then the possible movements are uncontrollable (i.e., the rover cannot decide which way to go). Otherwise, the possible movements are controllable.

Each rover is also provided with a battery that when fully charged has a capacity of 8 units of energy. Initially, the battery is fully charged. Whenever a Rover makes a move the battery level decreases by 1 unit of energy. Each rover can keep on moving provided it is not out of energy. 

Some of the tiles provide charging stations, depicted as blue power plugs. In this example, we have two charging stations: one in tile (4,1) and another in tile (3,4). If a Rover sits on any of these tiles, then it can get a full charge.

In the plant, some tiles contain samples that the rover can collect (assume that the amount of samples available is infinite). Specifically:

minerals (magenta diamond symbol)
liquid (blue waves symbol)
flora (green leaf symbol)
fossil (spiral symbol)
The rover can collect and carry maximum 3 samples for each type of sample described above. Clearly, any sample can be collected if and only if the rover sits on the right tile. Once one (or more) sample has been collected, then the rover can also empty its containers.

Finally, on tile (1,6) there is a lab for analyzing samples and a transmission center to transmit data back to earth. When the rover unloads the collected samples (if any) on this tile, the lab becomes BUSY. The lab can process if it is BUSY. The lab can transmit the data back to earth if it is not BUSY and a processing of samples has been actually done. After transmission, the processed data is forgotten.

Tasks:

 - Design a suitable SVG graphical representation of the plant.
 - Design the plant modules and describe the marking.
 - Design the following invariant requirements
    R1:  no rover runs out of battery on tiles that are not charging station.
    R2: The current energy level of each rover is always ≥2 units;
    R3: The maximum number of samples that each rover can carry (no matter the combination of samples) is always ≤10 samples;
    R4: Each rover can unload the collected samples only if (i) a sample has been collected, (ii) the rover is at the lab, and (iii) the lab has completed the previous processing;
    R5: Each rover can charge only if its current level of energy is <8 units
    R6: Rovers do not collide
    
Write a tooldef script to synthesize a supervisor enforcing all requirements
Write a PDF report justifying all of your design choices.
(Bonus): Can you design (or modify) the plant such that the supervisory synthesis algorithm run on it (without any requirements) computes a supervisor that already satisfies R1? Hint: exploit the marking.