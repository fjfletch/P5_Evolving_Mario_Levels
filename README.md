## P5: Evolving Mario Levels Writeup

**Individual_Grid**
- We used one-point crossover in our generate_children function, so that the first half of a level (based on length) is sometimes joined with the second half of the other genome, depending on a probability calculated with the other genome's fitness. This produces one child that is then possibly mutated before being returned.
- For our mutation, we gave each cell in the grid a very low chance (less than 1%) to mutate. When the chance is given, the operator could do nothing, add, or remove blocks depending on if there are any other adjacent blocks. Additionally, we implemented a 0.2% chance of a random floor block to be removed.

**Individual_DE**
- The design element crossover uses one-point crossover at a point randomly picked along the length for both genomes. It then creates two children with the four sections created by splitting the genomes at that point by pairing them with a section from the alternate genome. 
- The mutation function of the design element encoding has a 10% chance of randomly selecting an element to change and another varying chance of applying a type-specific mutation to one of the following: its attributes, position, or dimensions. 

**Generated Level**
- We chose this level, which required 10 generations and a little over 59 seconds to produce, because it seemed like a great balance of not to hard but not to easy. There are a decent amount of enemies and randomly placed holes that make it so you have to think properly about where you are jumping and when you will keep moving forward, but not so many that it becomes overwhelming.