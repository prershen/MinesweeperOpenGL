# MinesweeperOpenGL

## Objective of the project

The main objective of this project is to use OpenGL functions to implement a single player puzzle game - Minesweeper. 

## Gameplay

Minesweeper mines are scattered throughout a board, which is divided into cells. Cells have three states: 
* Uncovered (exposed)
* Covered (blank and clickable)
* Flagged ( marked by the player to indicate a potential mine location)

A player left-clicks a cell to uncover it. If a player uncovers a mined cell, the game ends, as there is only 1 life per game. Otherwise, the uncovered cells display either a number, indicating the quantity of mines adjacent to it, or a blank tile (or "0"), and all adjacent non-mined cells will automatically be uncovered. Right-clicking on a cell will flag it, causing a flag to appear on it. Flagged cells are still considered covered, and a player can click on them to uncover them, although typically they must first be unflagged with an additional right-click.

To win the game, players must uncover all non-mine cells, at which point, the timer is stopped. 



## Methodology 

It initiates the board using simple graphics and opengl function

Input is given using the mouse and the click decides which cell the user wants to uncover

Cell structure is used to store the status of each cell and its content can have any of - 0 (blank),1-8 (adjacent mines),-1 (mine) and the content is updated after initiation

Game_stats variable is used to store the state of the game and the result of the actions

Mine cells are decided randomly at initiation and upon clicking this, it ends the game and the user loses

Uncovering a non mine cell leads to a recursion call to uncovering all neighbouring cells that are safe

When the uncovered cells in the end are the same as the number of mines, the game ends and the user wins.


## Scope

It will help users to gain the cognitive asset of making inferences out of visual based system. 
It helps users in enhancing their hypothetical thinking.
It is also being developed on a 3D platform for more interactiveness.

## Software Requirements 

Operating System- Windows 10/MacOS

Tool - Visual Studio

Language- C++ 

Library- OpenGL (glut 3.7.6) 

## System Design and Implementation 

## Data Flow Diagram

![Minesweeper_Dataflow](https://github.com/user-attachments/assets/a7a52d0d-4ab3-4938-9ec4-998dbb7e8961)


## Modular Description
Minesweeper Board - Contains the information of the whole board, its status and the count of covered and uncovered cells. If the number of covered cells is equal to mines, ends the game with status as “Win”.
Uncover cell - It checks the condition of itself and uncovers if it is safe to uncover and recursively finds adjacent safe cells to uncover.
Calculate Adjacent Mines -  It calculates the number of adjacent mines and displays them on uncovered cells.
Mine detection - detects mins and if pressed, ends the game with status as “Lose”.
Display - Displays the game board and its details using OpenGL.



## Results and Snapshots

![Minesweeper_res1](https://github.com/user-attachments/assets/df8f4b12-8e1a-473d-a8b7-9606af487fbe)

![Minesweeper_res2](https://github.com/user-attachments/assets/acc4bedd-708a-47e6-8617-aaea3d36a3c3)


