## P5: Evolving Mario Levels Writeup

**Individual_Grid**
- We used one-point crossover in our generate_children function, so that the first half of a level (based on length) is sometimes joined with the second half of the other genome, depending on a probability calculated with the other genome's fitness. This produces one child that is then mutated before being returned.
- For our mutation, we gave each cell in the grid a very low chance (less than 0.1%) to mutate. When the chance is given, the operator could do nothing, add, or remove blocks depending on if there are any other adjacent blocks. Additionally, we implemented a 0.002% chance of a random floor block to be removed.

**Individual_DE**
- The design element crossover uses one-point crossover at a point randomly picked along the length for both genomes. It then creates two children with the four sections created by splitting the genomes at that point by pairing them with a section from the alternate genome. 
- The mutation function of the design element encoding has a 10% chance of randomly selecting an element to change and variable chance of applying a type-specific mutation to its attributes, position, or dimensions. 