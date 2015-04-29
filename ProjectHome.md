Oritaka is a BWAPI bot for Terran. Its main design concept is rule-base. Used units are SCV, Marine, Command Center, Supply Depot, and Barracks. Oritaka's SCV can collect resource such as minerals and gas, build structures, and scout the enemy bases. Barracks generates Marines. When Marines are built up a certain number, they attack the enemy bases at once.

Oritaka.cpp consists of onStart and onFrame. A function onStart is called at first. It does terrain analysis with BWTA and initialize parameters. A function onFrame is called every frame. It consists of drawing debug information, preprocessing, allocation of instruction, execution of instruction.

As debug information, the number of units of their own at each type, the number of enemy units that are in sight, frame count, elapsed time of the game, map name, the place of mineral and oil field, appropriate place to build a resource depot, and name, id, order at each units are displayed.

At preprocessing, the information used in the conditional expression at assignment instruction are calculated.

At allocation of instruction, my units are classified by their type and allocated order with rule-base. When some worker are allocated building order, mineral\_reserve that is necessary to ensure resources will be defined.

At execution of instruction, my units are classified into tasks: task\_train\_scv, task\_train\_marine, task\_set\_rally\_point, task\_scout, task\_attack, task\_escape, task\_build\_command\_center, task\_refinary, task\_build\_supply\_depot, task\_build\_barracks.

| <a href='http://www.youtube.com/watch?feature=player_embedded&v=HOQdLQrkn8w' target='_blank'><img src='http://img.youtube.com/vi/HOQdLQrkn8w/0.jpg' width='425' height=344 /></a> | <a href='http://www.youtube.com/watch?feature=player_embedded&v=MJDS8ZF_2nM' target='_blank'><img src='http://img.youtube.com/vi/MJDS8ZF_2nM/0.jpg' width='425' height=344 /></a> |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|