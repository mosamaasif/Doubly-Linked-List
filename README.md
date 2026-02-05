# Doubly Linked List

A template-based doubly linked list implementation in C++ with forward and reverse iterators.

## About

I built this as part of a Data Structures course assignment at university. It is a fully functional doubly linked list with custom iterator classes, supporting traversal in both directions. Each node holds data along with pointers to its previous and next neighbors. The project also includes an `Item` class (specific to the assignment) that demonstrates loading tab-delimited product data from a file, but the list itself is generic and works with any type.

## Features

- Generic (template-based) doubly linked list
- Forward and reverse iterator classes with full operator overloading (`++`, `--`, `*`, `==`, `!=`)
- Insert at head, tail, or before/after a specific element
- Delete from head, tail, or by element lookup
- Find elements by value
- Swap two nodes in the list (actual node swap, not just data swap)
- Sort a sub-range of the list using insertion sort
- Load data from tab-delimited text files
- Exception-safe assignment using the copy-swap idiom throughout
- Interactive console menu for all operations

## Built With

- C++14

## Getting Started

### Prerequisites

- A C++ compiler with C++14 support (clang++, g++, MSVC, etc.)
- [git](https://git-scm.com)

### Installation

Clone the repo:

```sh
git clone https://github.com/mosamaasif/Doubly-Linked-List.git
cd Doubly-Linked-List
```

### How to Run

Compile and run using clang++ (macOS example):

```sh
clang++ -std=c++14 -stdlib=libc++ -Iincludes src/main.cpp src/item.cpp -o main
./main
```

For g++ on Linux:

```sh
g++ -std=c++14 -Iincludes src/main.cpp src/item.cpp -o main
./main
```

For other compilers or IDEs, make sure the `includes/` directory is on the include path and both `src/main.cpp` and `src/item.cpp` are compiled together.

### Input File Format

The program can load data from `.txt` files. The file must be tab-delimited with the following columns:

```
ID	Name	Price	Category	Company
```

**All fields must be separated by tabs.** See the `tests/` directory for example files.
