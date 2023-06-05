# Social Distancing Simulator Prolog

This Prolog program aims to find a path through a park while adhering to social distancing rules. It divides the park into a grid and calculates distances using the Pythagorean theorem to ensure a safe distance from other park-goers.

## Usage

To run the program and find a path, follow these steps:

1. Ensure you have a Prolog interpreter installed on your system.
2. Clone or download this repository to your local machine.
3. Open the Prolog interpreter and load the program file.
4. Use the `solve` predicate to find a path by providing the necessary arguments:
   - Starting position on the south edge of the park.
   - Ending Y-coordinate (typically on the north edge of the park).
   - Size of the grid.
   - Locations of other park-goers.
   - The resulting path.
5. Run the program and observe the output path.

Here's an example of how to use the user-facing `solve` predicate with the provided sample values:

```prolog
solve([13,0], 24, [25,25], [[20,4],[13,7],[4,19]], Path).
```
The program will return the variable Path, which contains the resulting path as a list of coordinates representing the positions to follow to reach the goal while maintaining a safe distance from other park-goers.
```
P = [[13, 0], [13, 1], [12, 1], [11, 1], [10, 1], [9, 1], [9, 2], [8, 2], [8, 3], [7, 3], [7, 4], [7, 5], [7, 6], [7, 7], [7, 8], [7, 9], [7, 10], [7, 11], [7, 12], [7, 13], [8, 13], [8, 14], [9, 14], [9, 15], [10, 15], [10, 16], [10, 17], [10, 18], [10, 19], [10, 20], [10, 21], [10, 22], [10, 23], [10, 24]] 
```
Example 

<img width="500" alt="GUI picture" src="https://github.com/umangptl/Programming-Languages-Social-Distancing-Simulator/blob/main/distance.png">

