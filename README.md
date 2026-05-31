Simulation of albedo-effect in arctic ocean via mente-carlo steps in Python with fractal dimension method built-in.
# Arctic Albedo Effect: Monte Carlo Simulation and Fractal Dimension Analysis

## Overview
A Monte Carlo simulation modeling the Arctic albedo effect on a 1024×1024 lattice,
reproducing the increased fractal dimension of sea ice observed over recent decades
due to global warming.

## Scientific question
Melting in Arctic sea ice creates ponds in the ice during summer which controls albedo, transmittance of light, and heat and mass
balance(ice-albedo feedback). Ice melting leads to ice sheets of various shape, creating different living arctic ocean ecosystem.
The simulation attempt to predict the shape of the ice sheet to maintain the arctic ocean ecosystem.

## Methods
- Lattice size: 1024×1024 lattice that loops left to right and up and down
- Lattice initialization: Labeled with 1.0 = water and -1.0 = ice, and randomized number [-1.0,1.0] for height. The total percentage of water is given.
- Simulation type: Monte Carlo, randomly locate a grid in lattice, evaluate up,down,left,right grid's identity, modify the middle grid to identity of max quantity. If the quantity is 2 and 2, ice if height < 0, water if height > 0.
- Key library: NumPy
- Analysis: Fractal Dimension via counting area and surface perimeter that is in contact with the water.
- Result Visualization: Matplotlib

## Results
The results follow the expected trend of Arctic Ocean ice-water albedo effects. An increase in initialized water percentage results in a higher fractal dimension constant, reflecting more complex ice sheet geometries and increasingly fragmented structures that diversify the Arctic Ocean ecosystem. Fractal dimension values ranged from 1 to 2 as ice area increased, which is congruent with real-world observations.

## Assumptions
1) Only ice and water, in reality there are state of slushi etc.
2) Assuming the area of ice is 1, in reality not true

## How to run
**Requirements:** Python 3.x, NumPy, MatPlot

Install dependencies:
pip install numpy
pip install numpy matplotlib

Run the notebook:
jupyter notebook arctic_albedo_simulation.ipynb
