# Constraint Satisfaction Problem Algorithm and Solver

The class for defining a constraint satisfaction problem (CSP) is quite general, and can be used with many problems. The solver is
based on min conflicts with weighted assignments (0 or 1 by default, >1 gives preference to that node assignment) used to break the tie between two equally good non-conflicting solutions. 


Example
---
We want the 4 cedges of a square to be given names. Possibilities for male are: Billy, Morris, Edward; for female are: Mary, Bridget, Sue. Adjacent edges must have different genders. We prefer that the first letters of names of adjacent edges are different.

    Billy ---- Mary
     |          |
     |          |                                                    
    Bridget -- Morris

Is obviously a solution using the traditional min conflicts algorithm. But

    Edward ---- Sue
     |          |                             
     |          |
    Bridget --- Morris

Is a preferred choice using this version of min conflicts. Bear in min the preferred solution only has a higher chance of being chosen.
