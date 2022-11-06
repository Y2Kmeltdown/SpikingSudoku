# Sudoku Solver Using spiking neural networks and Spinnaker

In this github repository I will showcase my work on making a spiking neural network solve a standard 9 by 9 sudoku with high accuracy. The system is based off another paper that used spiking neural networks to generate a complete 4x4 sudoku with no prior inputs. The network I have designed plays a standard 9x9 sudoku with the given priors for a 9x9 game and finds the exact solution that is expected.

## Requirements

### Hardware

To get started with this you will need to have access to a Spinnaker board whether it be through online access or a physical board. you can register for online access [here](https://iam.ebrains.eu/auth/realms/hbp/protocol/openid-connect/registrations?response_type=code&client_id=xwiki&redirect_uri=https://wiki.ebrains.eu).

### Dataset

For my testing I used a dataset from kaggle which contains 1 million sudoku games and solutions which can be found [here](https://www.kaggle.com/datasets/bryanpark/sudoku).

### Dependencies

For spinnaker on a local machine, you will need to have python 3.8.13 installed. I recommend setting up a conda environment for it. You can find the instructions for setting up your local spinnaker interface and how to install spynnaker8 [here](https://spinnakermanchester.github.io/spynnaker/4.0.0/PyNNOnSpinnakerInstall.html). For this example to work you will just need spynnaker8 and all of it's dependencies such as matplotlib and numpy.

## Code Overview

The notebook is set up in three sections.

The first section is data preparation where the sudoku data is loaded and the connection layers and functions for mapping to specific neurons are created.

The second section is where the spiking neural network is set up on the spinnaker hardware. This section is where the layers are defined and the projections are created.

The final section is evaluation. This is where the results of the simulation are recorded such as the number of sudoku violations overtime and the final resulting board.

## Conclusion

The code presented in this github is extremely effective at solving constrained sudoku problems with high accuracy. The next stages of this project is to develop an online game where users will be able to play against the spinnaker board to see if they can beat a computer brain.
