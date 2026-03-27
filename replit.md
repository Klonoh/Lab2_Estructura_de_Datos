# Doubly Linked List - C Programming Exercise

## Project Overview
This is a C programming lab assignment focused on implementing a generic Doubly Linked List (TDA - Tipo de Dato Abstracto).

## Goal
Students must complete the function implementations in `list.c` by filling in the stub functions. The file contains a note at the top: **DO NOT modify `list.c` as an agent — these are student exercises.**

## Key Files
- **`list.h`** - Header file with struct definitions and function prototypes
- **`list.c`** - Implementation file (students fill in the stubs)
- **`main.c`** - Demo application using the list to store Movie (Pelicula) structs
- **`test.c`** - Unit tests for all list functions
- **`test.sh`** - Automation script: compiles tests, runs them, and optionally pushes to GitHub

## Data Structures
- `Node` - Doubly linked node with `data`, `next`, and `prev` pointers
- `List` - Contains `head`, `tail`, and `current` node pointers

## Functions to Implement (in list.c)
1. `createList()` - Allocate and initialize a List with all pointers set to NULL
2. `firstList(list)` - Return data of head node, set current to head
3. `nextList(list)` - Return data of node after current, advance current
4. `lastList(list)` - Return data of tail node, set current to tail
5. `prevList(list)` - Return data of node before current, move current back
6. `pushFront(list, data)` - Insert a new node at the beginning
7. `pushCurrent(list, data)` - Insert a new node after the current node
8. `popCurrent(list)` - Remove node at current position, return its data, advance current to next

## Pre-implemented Functions
- `createNode(data)` - Allocates and initializes a Node
- `pushBack(list, data)` - Uses pushCurrent (needs pushCurrent to work)
- `popFront(list)` / `popBack(list)` - Use popCurrent (needs popCurrent to work)
- `cleanList(list)` - Uses popFront to empty the list

## Tech Stack
- Language: C
- Compiler: GCC
- Debugger: GDB (available in nix deps)

## Workflow
- **Start application**: Compiles `test.c` (which includes `list.c`) and runs the tests to show progress
- Compilation: `gcc test.c -o a.out && ./a.out`
- Tests are scored out of 60 points total (10 per function)
