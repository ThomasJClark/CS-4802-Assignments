# CS 4802 Assignment 1
Thomas Clark

## Running
To run a simulation, either press **"Play"** to advance the board each second, or click **"Step"** to manually go through one generation at a time. While the simulation is playing, you can press **"Pause"** to stop it, or wait for it to automatically stop when the board stops changing.

## Generation 0
The initial generation is generated by making all cells have a 30% probability of being alive and a 70% probability of being dead.  You can click **"Randomize"** to generate a new starting configuration with a different probability, or **"Kill All"** to generate a board with no living cells.

### Custom Configurations
To customize the initial configuration, you can click empty spots to place cells, and click living cells to kill them.  This can also be done in the middle of a simulation, but only if it's paused.  To create an entirely custom configuration, click the **"Kill All"** button, then begin placing cells.

## Rules
By default, the simulation applies the standard Conway's Game of Life rules.  However, the following game presets are also available:

* **Population Growth**, where cells always reproduce into neighboring cells
* **Population Decline**, where any cells adjacent to dead cells die
* **"Blob"**, where cells with four or more neighbors are alive, regardless of their previous state.  This tends to made cells group together blob-like shapes, giving it its name.
* **26/36**, a common variation on Conway's Game of Life where dead cells with either 3 or 6 neighbors become alive.
* **Strobe**, another made-up game where all living cells die and all dead cells come alive.  This results in every cell flashing between two states at each generation.
* **Maze**, a made-up set of rules I wrote that tends to form strobing maze-like patterns.

You can select a game preset using the **"Game Presets"** panel.  The specific rules of each game are also shown when that game is selected.

### Custom Rules

You can experiment with visualizing new cellular automatons by using the custom rule feature.
1. Choose the **"Custom"** game preset
2. Click **"Add Rule"** in the custom rules panel.
3. Select the conditions that cause the rule to affect a cell, and click **"+ Add Rule"**.
4. To remove a custom rule, click the **X** next to the rule.

Any cell that does not match any custom rule will remain in its previous state.  You can use the **Play** and **Step** features to view the results of custom rules just like any other rule preset.

## Significance
### Technical
Most of the free-form features of the simulation are technical.  It features a selection of rule presets, a flexible set of way to create randomized or manually specified boards, and a system for prototyping entirely new sets of rules.  A concise textual description for each rule is also generated.  In addition, the page uses responsive design, so it will adjust itself appropriately on smartphones.
### Biological
The custom rule feature can be used to add biological significance to simulations.  Instead of just viewing the results of a single set of arbitrary rules like Conway's Game, one can add a custom set of rules to visualize an approximation of a biological process.

## Lab 3
### Currently Supported Interactions
Interactions currently supported (prior to Lab 3) include:
* #### Playing/pausing the simulation
Playing the simulation makes it easy to see the abstract results of the current rules and the state of the board over many generations.  The ability to pause supports user understanding by providing a chance to see what an individual generation looks like.

* #### Selecting between different game presets
The user can choose one of many different game presets, such as Conway's Game of Life, which helps the user determine how simple rule changes affect the outcome.

* #### Stepping the simulation one generation at a time
The ability to step the simulation to the next generation improves user understanding by showing the specific results  of one application of the game's rules.

* #### Randomizing the board to a specified percentage of living cells
Randomizing the board doesn't do much to improve user understanding, but allowing the user to specify a custom percentage improves the effectiveness of other features that present under certain conditions, such as a very high density of cells.

* #### Creating cells, killing cells, and killing all cells
The user can click the board to create or kill individual cells, and click a button to kill all cells on the board.  Allowing predetermined initial configurations in addition to randomized ones supports user understanding.  It allows the user to test hypotheses about  patterns in the current rules, rather than just randomizing the board and looking for patterns.

* #### Adding new rules to the custom game mode
This supports user understanding by allowing the user to rapidly prototype new game designs.

### Opportunities for more interaction
* #### Show percentage of cells that are alive over time
The user could toggle on and off an alternate view to show the percentage of cells that are currently alive, as well as a time-series chart showing the historical percentage of living cells.

* #### Identify clusters of cells
The user to set parameters for detecting clusters of cells, and be able to see how these clusters form and move around over time.

* #### View history
The user could have access to a slider to go back to previous states of the board.  This would help show the results of a particular initial state better than only being able to watch it once.
##### Mockup
![](http://i.imgur.com/7pQ6v3c.png)


