# Gene Inheritance Simulation

This project simulates the inheritance of blood type alleles across generations in a family tree. Built in C, the simulation models how a child's blood type is determined based on their parents' alleles, tracing inheritance through multiple generations.

## Overview

Each person in the simulation has:
- **Two alleles** (A, B, or O)
- **Two parents** (unless they are in the oldest generation)

Inheritance follows simple Mendelian rules:
- Each parent randomly passes one of their two alleles to the child.
- The oldest generation receives randomly assigned alleles.

##  How It Works

- The program builds a family tree using recursion.
- The oldest generation (e.g., grandparents) are assigned random alleles.
- Each generation inherits one allele from each parent.
- The `create_family(int generations)` function constructs the tree and returns a pointer to the youngest person.
- Each person is dynamically allocated using `malloc`.

##  Running the Program

###  Compile:

```bash
gcc -o inheritance inheritance.c
```
### Run:
```bash
./inheritance
```

## Example Output

```bash
Child (Generation 0): blood type OO
    Parent (Generation 1): blood type AO
        Grandparent (Generation 2): blood type OA
        Grandparent (Generation 2): blood type BO
    Parent (Generation 1): blood type OB
        Grandparent (Generation 2): blood type AO
        Grandparent (Generation 2): blood type BO


```
