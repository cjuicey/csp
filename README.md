# csp
# Constraint Satisfaction Problem Algorithm and Solver

The class for defining a constraint satisfaction problem (CSP) is quite general, and can be used with many problems. The solver is
based on min conflicts with weighted assignments (0 or 1 by default, >1 gives preference to that node assignment) used to break the
tie between two non-conflicting solutions. A good idea would be to have a higher weight for assignments satisfying soft constraints 
to attract optimal results.


Example
---
We want the 4 cedges of a square to be given names. Possibilities are Billy, Bob, Edward, Mary, Margaret, Sue. Adjacent edges must 
have different genders. We prefer that the first letters of names of adjacent edges are different.

Billy ---- Mary
 |          |
 |          |                                                    
Bob  ----- Margaret

Is obviously a solution using the traditional min conflicts algorithm. But

Edward ---- Sue
 |          |                             
 |          |
Bob  ----- Margaret

Is a preferred choice using this version of min conflicts.
