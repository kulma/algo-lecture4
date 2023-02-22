# Activities

> The [modulo-calculator](#links) might be handy in these exercises.

## Task 1

- Refer to the following link. Discuss how open hashing works.
  https://www.cs.usfca.edu/~galles/visualization/OpenHash.html
> With open hashing, the hash function separates the values into different categories, inside which the values are stored as linked lists.
- Open Hashing Practice. Refer to the following link. Move each record on the left to the appropriate bin on the right.
  https://opendsa-server.cs.vt.edu/OpenDSA/Exercises/Hashing/OpenHashPRO.html
- Given the following input (`4322, 1334, 1471, 9679, 1989, 6171, 6173, 4199`) and the hash function `x mod 10`, which of the following statements are true?
- [x] `9679, 1989, 4199` hash to the same value
- [x] `1471, 6171` hash to the same value
- [] All elements hash to the same value
- [] Each element hashes to a different value

## Task 2

- Bucket Hashing Practice. Refer to the following [link](https://opendsa-server.cs.vt.edu/OpenDSA/Exercises/Hashing/HashBucketPRO.html).
- The keys `12, 18, 13, 2, 3, 23, 5 and 15` are inserted into an initially empty hash table of length `10` using open addressing with hash function `h(k) = k mod 10` and **linear probing**. What is the resultant hash table?
```
0 - 
1 - 
2 - 12
3 - 13
4 - 2
5 - 3
6 - 23
7 - 5
8 - 18
9 - 15
```
## Task 3:

- What is the [Birthday Paradox](http://en.wikipedia.org/wiki/Birthday_problem)?
> The birthday paradox refers to the fact that if one was to collect 23 random people in a room, the probability of at least 2 of them sharing a birthday would be 50+%. It's called a paradox because the number of people needed to surpass the 50% mark is counterintuitively low.
- Why is it generally discussed with hashing?
> It helps illustrate the fact that by increasing the size of the hashing table, it doesn't necessarily translate into a lot less collisions.
- In a hash table of 9658 slots, what is the smallest number of records that must be inserted for the probability of a collision to be 61% or more? Use the calculator at this [link](https://opendsa-server.cs.vt.edu/ODSA/AV/Hashing/Birthday.html)
> The probability surpasses 61% at 136 entries
- Discuss in groups how the following program works `./src/birthday.cpp`?
> The main function calls the find function, which uses the function $\sqrt{2*365*ln(\frac{1}{(1-p)})}$ to determine how many people it takes to reach the given probability of collision.
## Task 4: Individual (at home)

- Difference between `Separate Chaining` and `Open Addressing` collision handling techniques?

  https://www.geeksforgeeks.org/open-addressing-collision-handling-technique-in-hashing/

  https://www.geeksforgeeks.org/separate-chaining-collision-handling-technique-in-hashing/

- (Bonus) Run the following program and comment on the code `./src/hashtable.cpp`

## Link(s)

- [modulo-calculator](https://www.calculators.org/math/modulo.php)
- [Practice Problems on Hashing](https://www.geeksforgeeks.org/practice-problems-on-hashing/)
