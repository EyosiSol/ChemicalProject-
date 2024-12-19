# Chemical Reaction Simulation Using Moore's Diagram

This repository contains the project documentation, design, and implementation files for simulating a chemical reaction process using Moore's Diagram. The simulation involves designing and analyzing a circuit using Altium Designer to model the behavior of chemical reactions and their resulting properties.

## Project Overview

This project models the interaction of an unknown chemical `A` with another chemical `B` (which can be either strong or weak). The chemical interactions lead to distinct color and smell characteristics, determined by specific rules:

1. **Initial Mixture of A with B:**

   - Strong `B`: Blue color, bad smell.
   - Weak `B`: Red color, bad smell.

2. **Reactions with Further Additions:**
   - Blue compound + Strong `B` → Red, bad smell.
   - Blue compound + Weak `B` → Brown, bad smell.
   - Red compound + Strong `B` → Brown, good smell.
   - Red compound + Weak `B` → Green, good smell.
   - Green compound + Weak `B` → White, bad smell.
   - Green compound + Strong `B` → Original state, good smell.
   - Brown compound + Strong `B` → White, bad smell.
   - Brown compound + Weak `B` → Grey, good smell.
   - Grey compound + Strong `B` → Original state, good smell.
   - Grey compound + Weak `B` → White, bad smell.
   - White compound + Strong `B` → White, bad smell.
   - White compound + Weak `B` → Green, good smell.

## Project Components

### 1. **Circuit Design**

The chemical interaction logic is implemented as a circuit designed in **Altium Designer**. The circuit simulates the state transitions based on the type of chemical added.

### 2. **Simulation**

Simulation graphs demonstrate the reaction process. Steps include:

- Annotating and validating the circuit schematic.
- Running transient analysis to visualize state transitions.
- Observing weak and strong paths through the color and smell states.

### 3. **PCB Design**

A PCB is designed to implement the circuit:

- Manufactured parts were used to ensure accurate representation.
- Automatic routing and validation were performed for the final design.

### 4. **Moore's Diagram**

The circuit follows the principles of Moore's state machine to represent the transitions between states based on the input conditions.

## Usage

1. Open the project in **Altium Designer**.
2. Follow the annotated circuit to understand the logic implementation.
3. Run the simulation:
   - Set simulation parameters: `FROM TO ~ 0 and 25` with step `0.1`.
   - Observe the plotted graph for state transitions.
4. Use the PCB design files to visualize or fabricate the circuit.

## Files

- `ChemicalProject.pdsprj`: Altium project file containing the circuit schematic and PCB layout.
- Simulation graphs: Included in the project to illustrate state transitions.
- Moore's Diagram documentation.

## License

This project is released under the MIT License. See `LICENSE` for details.
