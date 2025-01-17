This app works best with JavaScript enabled.

# Think Like a Programmer:

## Chapter One

### Strategies for Problem Solving

#### 2018-11-26

**Problem solving** - writing an original program that performs a particular set of tasks and meets all stated constraints

**Analogy** - an exploitable simularity between a solved problem and an unsolved problem

### Rules for Problem Solving

#### 1. Always have a plan

Your plan may need to be changed or you may have to abandon it and come up with another, but you should never start blindly coding. Planning allows you to set intermediate goals and achieve them.

Without a plan, you only have one goal - solving the entire problem. This leads you to feeling like you haven't accomplished anything until a solution has been reached, which leads to frustration.

If you instead create a plan with a series of minor goals, even if you haven't solved the main problem, you will make measureable progress toward a solution and feel as though you have spent your time usefully.

#### 2. Restate the Problem

This may provide insights into the problem not obvious to you initially. This can be part of your plan for solving the problem, which counts as progress toward your end goal. Restating the problem also allows you to ask clarification from whomever you received the problem from if your assessment of the problem is accurate.

#### 3. Divide the Problem

This can often lower the difficulty of solving a problem by an order of magnitude.

#### 4. Start With What You Know

At every point in your career, there will be some skills you have nailed down, others you can use with effort, and still others that you don't yet possess. Any given problem may be entirely solveable with the skills you already have, or it might not. Either way, you should investigate the problem with the tools already at your disposal before looking elsewhere

#### 5. Reduce the Problem

Example: You're given a series of coordinates in three-dimensionsal space and need to find the coordinates that are closest to each other. If you don't immediately know how to solve that, you can reduce the problem to seek a solution.

- What if the coordinates were in two-dimensional space instead of three? What if the coordinates were along a line and the coordinates were individual numbers? Then the question becomes find the two numbers with the minimum absolute difference.

- What if instead of having a series of coordinates, you had three? Then you could compare A to B, B to C, and A to C.

Reduction allows us to work on a simpler problem even when we can't find a way to divide the problem into smaller parts. This also allows you to pinpoint what areas of the problem you might be struggling with.

#### 6. Look for Analogies

Don't just look for code similar to the code you need to solve the problem and then try to modify that code to suit your purpose - it's difficult to modify code you don't fully understand. Even more than that, if you don't complete a solution yourself, you won't internalize it, which is a missed analogy for the future.

#### 7. Experiment

This is not the same as guessing. Experimenting is done in a more controlled fashion and involves making hypotheses and then testing whether or not your assumptions about the outcome were correct.

#### 8. Don't Get Frustrated

Realize that you can own your own emotional reaction to things and take a break if you need to.

### Exercises:

1.  Try a medium-difficulty Sudoku puzzle.

2.  Consider a sliding tile puzzle variant where the tiles are covered with a picture instead of numbers. How does this increase the difficulty and why?

3.  Find a strategy for sliding tile puzzles different from mine.

4.  Search for old-fashioned puzzles of the fox, goose, and corn variety and try to solve them. Sam Loyd popularized them, so search his name. Once you uncover (or give up and read) the solution, think of how you could make an easier version of the puzzle. What would you have to change? The constraints or just the wording?

5.  Try to write explicit strategies for traditional pencil and paper games like crosswords or "Jumble"

---

## Problem: How to Cross the River

A farmer with a fox, a goose, and a sack of corn needs to cross a river. The farmer has a rowboat, but there is room for only the farmer and one of his three items. Unfortunately, both the fox and the goose are hungry. The fox cannot be left alone with the goose, or the fox will eat the goose. Likewise, the goose cannot be left alone with the sack of corn or the goose will eat the sack of corn. How does the farmer get everything across the river?

## Solution Sketching

        **Point A**
    Items on shore

\*\*Toward origin\*\*

\*\*Boat\*\*

\*\*Across River\*\*

\*\*Point B\*\*  
Items on shore

corn, fox, goose

corn, fox

goose

=&gt;

corn, fox

&lt;=

goose

fox

corn

=&gt;

goose

fox

&lt;=

goose

corn

goose

fox

=&gt;

corn

goose

&lt;=

corn, fox

goose

=&gt;

corn, fox

corn, fox, goose

#### By restating a problem in more formal terms, we can often uncover so9ltuions that would have otherwise eluded us

## Boat Cross - State Constraints

1 - The farmer can only take one item at a time on the boat  
2 - The fox and goose cannot be left alone on the same shore  
3 - The goose and corn cannot be left alone on the same shore

## List Operations

### Option 1: List actions needing to be taken:

1.  Operation: Carry the fox across the river
2.  Operation: Carry the goose across the river
3.  Operation: Carry the corn across the river

### Option 2: Make operations generic or parametized

1.  Operation: Row the boat from one side of the river to the other
2.  Operation: If the boat is empty, load an item from the shore
3.  Operation: If the boat is not empty, unload an item to the shore

---

## Problem: Sudoku

A 9x9 grid is partially filled with single digits (from 1-9) and the player must fill in the empty squares while meeting certain constraints. In each row and column, each digit must appear exactly once, and further, in each marked 3x3 area, each digit must appear exactly once

## Step 1: Restate Problem Constraints

1.  The numbers 1-9 must appear exactly once per row
2.  The numbers 1-9 must appear exactly once per column
3.  The numbers 1-9 must appear exactly once per 3x3 grid

## Operations

1.  Fill in grid based on information already provided
2.  Start with area of grid most filled in and less uncertain

## Board

<table><thead><tr class="header"><th></th><th>Col 0</th><th>Col 1</th><th>Col 2</th><th>Col 3</th><th>Col 4</th><th>Col 5</th><th>Col 6</th><th>Col 7</th><th>Col 8</th></tr></thead><tbody><tr class="odd"><td>Row 0</td><td></td><td>9</td><td>1</td><td></td><td>6</td><td></td><td>7</td><td></td><td></td></tr><tr class="even"><td>Row 1</td><td></td><td></td><td></td><td></td><td>8</td><td>2</td><td></td><td>3</td><td>9</td></tr><tr class="odd"><td>Row 2</td><td>5</td><td></td><td>3</td><td></td><td></td><td></td><td>2</td><td></td><td></td></tr><tr class="even"><td>Row 3</td><td></td><td></td><td></td><td>9</td><td>1</td><td>3</td><td></td><td>6</td><td>2</td></tr><tr class="odd"><td>Row 4</td><td></td><td></td><td>2</td><td>4</td><td></td><td>6</td><td>8</td><td></td><td></td></tr><tr class="even"><td>Row 5</td><td>1</td><td>4</td><td></td><td>8</td><td>2</td><td>5</td><td></td><td></td><td></td></tr><tr class="odd"><td>Row 6</td><td></td><td></td><td>9</td><td></td><td></td><td></td><td>5</td><td></td><td>7</td></tr><tr class="even"><td>Row 7</td><td>6</td><td>7</td><td></td><td>1</td><td>5</td><td></td><td></td><td></td><td></td></tr><tr class="odd"><td>Row 8</td><td></td><td></td><td>5</td><td></td><td>4</td><td></td><td>6</td><td>9</td><td></td></tr></tbody></table>

## Steps

1.  Assess if any unambiguous solution for a square

2.  \[4, 4\] is the obvious starting point as the other squares in the 3x3 grid it belongs to are already filled out, leaving the only solution for that square to be 7

3.  Col 4 now only has two open slots, on Row 2 and Row 6. As there are only two slots left in the row, we can rule out all the numbers that are already present in the row (1, 2, 4, 5, 6, 7, 9\], leaving the only two options 3 and 9. There is already a 3 on Row 2 and there is already a 9 on Row 6, so we know that \[2, 4\] must be 9 and \[6, 4\] must be 3.

4.  \[3, 6\] is a good next target. It can't be 1, 2, 3, 6, or 9 because those are already found in Row 3. Col 6 eliminates 5, 7, and 8. That leaves 4.

5.  \[7, 6\] is a good next target. 1, 5, 6, 7 are eliminated because they are present in Row 7. 2, 4, and 8 are additionally eliminated by Col 6. The 3x3 grid eliminates 9. That leaves 3.

6.  \[5, 6\] is a good target. 1, 2, 4, 5 are eliminated by Row 5. 3, 6, 7, 8 are eliminated by Col 6. That leaves 9.

7.  \[1, 6\] now can only be 1 because 1 is the only number missing in Col 6.

8.  \[5, 7\] is a good target. 1, 2, 4, 5, 8, 9 are elinated by Row 5. 3 and 6 are eliminated by Col 7. That leaves 7.

9.  \[5, 8\] is a good target. 1, 2, 4, 5, 7, 8, 9 are eliminated by Row 7. 6 is eliminated by the 3x3 grid. Leaving 3.

10. \[5, 2\] has to be 6 because that's the only number missing in Row 5.

11. \[0, 5\] is a good target. 1, 6, 7, 9 are eliminated by Row 0. 2, 3, 5 are eliminated by Col 5. 8, 9 are eliminated by the 3x3 grid. Leaving 4.

12. \[2, 5\] is a non-obvious next target - there is not a 1 found in the 3x3 grid and the only other open slots in the grid are in Col 3, which already has a 1, which leaves \[2, 5\] having to be 1.

13. \[2, 3\] is a good next target. 1, 2, 3, 5 are eliminated by Row 2. 4, 8, 9 are eliminated by Col 3. 6 is eliminated by the 3x3. That leaves 7

14. \[0, 3\] is a good target. In the 3x3, only 5 and 3 are still missing and the open slots are \[0, 3\] and \[1, 3\]. However, Row 1 already has a 3, so \[0, 3\] must be the 3 in the 3x3.

15. That leaves \[1, 3\] being the 5.

16. \[6, 5\] is a good target. 3, 5, 7, 9 are eliminated by Row 6. 1, 2, 4, 6 are eliminated by Col 5. That leaves 8

17. \[7, 5\] is a good target. 1, 3, 5, 6, 7 are eliminated by Row 7. 2, 4, 8 are eliminated by Col 5. That leaves 9.

18. That leaves \[8, 5\] being 7 as it's the only number not accounted for in Col 5.

19. \[8, 3\] is a good target. 4, 5, 6, 7, 9 are eliminated by Row 8. 1, 3, 8 are eliminated by Col 3. That leaves 2.

20. \[6, 3\] has to be 6 as it's the only unaccounted number in the 3x3 and in Col 3.

21. \[1, 1\] is a good target. 1, 2, 3, 5, 8, 9 are eliminated by Row 1. 4, 7 are eliminated by Col 1. That leaves 6.

22. \[2, 1\] is a good target. 1, 2, 3, 5, 7, 9 are eliminated by Row 2. 4, 6 are eliminated by Col 1. That leaves 8.

23. \[2, 7\] is a good target. 1, 2, 3, 5, 7, 8, 9 are eliminated by Row 2. 6 is eliminated by Col 7. That leaves 4.

24. \[2, 8\] has to be 6 because it's the only number unaccounted for in Row 2.

25. \[0, 0\] is a good target. 1, 3, 4, 6, 7, 9 are eliminated by Row 0. 5 is eliminated by Col 0. 8 is eliminated by 3x3. That leaves 2.

26. \[3, 1\] is a good target. 1, 2, 3, 4, 6, 9 are eliminated by Row 3. 7, 8 are eliminated by Col 1. That leaves 5.

27. \[6, 0\] is a good target. 3, 5, 6, 7, 8, 9 are eliminated by Row 6. 1, 2 are eliminated by Col 0. That leaves 4.

28. This means \[1, 2\] must be 4 as Col 0 and Col 1 already have a 4, as do Rows 0 and 2.

29. This means \[1, 0\] has to be 7 as it is the only number missing in the 3x3 grid and in Row 1.

30. \[3, 0\] is a good target. 1, 2, 3, 4, 5, 6, 9 are eliminated by Row 3. 7 is eliminated by Col 0. That leaves 8.

31. This means \[3, 2\] has to be 7 as it's the only number missing from Row 3.

32. \[4, 1\] is a good target. 2, 4, 6, 7, 8 are eliminated by Row 4. 5, 9 are eliminated by Col 1. 1 is eliminated by the 3x3 grid. That leaves 3.

33. That means \[4, 0\] must be 9 as it's the only number missing from the 3x3.

34. That means \[8, 0\] has to be 3 as it's the only number missing from Col 0

35. \[7, 2\] has to be 8 as it's the only number missing from Col 2.

36. \[6, 1\] is a good target. 3, 4, 5, 6, 7, 8, 9 are eliminated by Row 6. While that leaves 1 and 2 as options, the only other empty slot in the 3x3 is \[8, 1\] and Row 8 already has a 2, leaving \[6, 1\] having to be 2.

37. That leaves \[8, 1\] having to be 1.

38. That leaves \[8, 8\] having to be 8 as it's the only missing number in Row 8.

39. \[7, 7\] is a good target. 1, 3, 5, 6, 7, 8, 9 are eliminated by Row 7. 4 is eliminated by Col 7. That leaves 2.

40. That leaves \[6, 7\] having to be 1 as it's the only missing number in Row 6.

41. That leaves \[7, 8\] having to be 4 as it's the only missing number in the 3x3 and in Row 7.

42. \[4, 8\] is a good target. In the 3x3, the only two numbers missing are 1 and 5. The other empty slot is \[4, 7\] and Col 7 already has a 1, so \[4, 7\] must be 1.

43. That means \[4, 7\] must be 5.

44. \[0, 7\] has to be 8 because that's the only number missing from Col 7

45. \[0, 8\] has to be 5 because that's the only number missing from Col 8

<table><thead><tr class="header"><th></th><th>Col 0</th><th>Col 1</th><th>Col 2</th><th>Col 3</th><th>Col 4</th><th>Col 5</th><th>Col 6</th><th>Col 7</th><th>Col 8</th></tr></thead><tbody><tr class="odd"><td>Row 0</td><td>2</td><td>9</td><td>1</td><td>3</td><td>6</td><td>4</td><td>7</td><td>8</td><td>5</td></tr><tr class="even"><td>Row 1</td><td>7</td><td>6</td><td>4</td><td>5</td><td>8</td><td>2</td><td>1</td><td>3</td><td>9</td></tr><tr class="odd"><td>Row 2</td><td>5</td><td>8</td><td>3</td><td>7</td><td>9</td><td>1</td><td>2</td><td>4</td><td>6</td></tr><tr class="even"><td>Row 3</td><td>8</td><td>5</td><td>7</td><td>9</td><td>1</td><td>3</td><td>4</td><td>6</td><td>2</td></tr><tr class="odd"><td>Row 4</td><td>9</td><td>3</td><td>2</td><td>4</td><td>7</td><td>6</td><td>8</td><td>5</td><td>1</td></tr><tr class="even"><td>Row 5</td><td>1</td><td>4</td><td>6</td><td>8</td><td>2</td><td>5</td><td>9</td><td>7</td><td>3</td></tr><tr class="odd"><td>Row 6</td><td>4</td><td>2</td><td>9</td><td>6</td><td>3</td><td>8</td><td>5</td><td>1</td><td>7</td></tr><tr class="even"><td>Row 7</td><td>6</td><td>7</td><td>8</td><td>1</td><td>5</td><td>9</td><td>3</td><td>2</td><td>4</td></tr><tr class="odd"><td>Row 8</td><td>3</td><td>1</td><td>5</td><td>2</td><td>4</td><td>7</td><td>6</td><td>9</td><td>8</td></tr></tbody></table>

## Lessons Learned

Look for most constrained part of the problem.

In AI: In a problem where you are trying to assign different values to different variables to meet constraints, you should start with the variable with the most constraints/the variable with the lowest number of possible options.

---

## Problem: The Sliding Eight

A 3x3 grid is filled with 8 tiles, numbered 1 through 8, and one empty space. A tile can be slid into an adjacently empty space, leaving the tile's previous location empty. The goal is to slide the tiles to place the grid in an ordered configuration from 1 in the upper left

## Step 1 - Restate the problem constraints

1.  A tile can be slid into an adjacently empty space
2.  If a tile is moved to an empty space, previous location becomes the empty space
3.  The 1 tile must end up in the upper left
4.  The grid must end up ordered

## Step 2 - Operations

1.  Look at the position of the tiles in the grid
2.  Move a numbered tile to an empty space
3.  Repeat until ordered

## Solution should look like:

<table><thead><tr class="header"><th>1</th><th>2</th><th>3</th></tr></thead><tbody><tr class="odd"><td>4</td><td>5</td><td>6</td></tr><tr class="even"><td>7</td><td>8</td><td></td></tr></tbody></table>

## A starting position:

<table><thead><tr class="header"><th>4</th><th>7</th><th>2</th></tr></thead><tbody><tr class="odd"><td>8</td><td>6</td><td>1</td></tr><tr class="even"><td>3</td><td>5</td><td></td></tr></tbody></table>

## Solution

Form a train of consecutive numbers to maintain order. Solve for a row or column in order to break up problem into smaller problems

Left:⇦

Right:⇨

Up:⇧

Down:⇩

**Step 1**

<table><thead><tr class="header"><th>4</th><th>7</th><th>2</th></tr></thead><tbody><tr class="odd"><td>8</td><td>6</td><td>1</td></tr><tr class="even"><td>3</td><td>5</td><td>⇩</td></tr></tbody></table>

**Step 2**

<table><thead><tr class="header"><th>4</th><th>7</th><th>2</th></tr></thead><tbody><tr class="odd"><td>8</td><td>6</td><td>⇩</td></tr><tr class="even"><td>3</td><td>5</td><td>1</td></tr></tbody></table>

**Step 3**

<table><thead><tr class="header"><th>4</th><th>7</th><th>⇨</th></tr></thead><tbody><tr class="odd"><td>8</td><td>6</td><td>2</td></tr><tr class="even"><td>3</td><td>5</td><td>1</td></tr></tbody></table>

**Step 4**

<table><thead><tr class="header"><th>4</th><th>⇧</th><th>7</th></tr></thead><tbody><tr class="odd"><td>8</td><td>6</td><td>2</td></tr><tr class="even"><td>3</td><td>5</td><td>1</td></tr></tbody></table>

**Step 5**

<table><thead><tr class="header"><th>4</th><th>6</th><th>7</th></tr></thead><tbody><tr class="odd"><td>8</td><td>⇧</td><td>2</td></tr><tr class="even"><td>3</td><td>5</td><td>1</td></tr></tbody></table>

**Step 6**

<table><thead><tr class="header"><th>4</th><th>6</th><th>7</th></tr></thead><tbody><tr class="odd"><td>8</td><td>5</td><td>2</td></tr><tr class="even"><td>3</td><td>⇦</td><td>1</td></tr></tbody></table>

**Step 7**

<table><thead><tr class="header"><th>4</th><th>6</th><th>7</th></tr></thead><tbody><tr class="odd"><td>8</td><td>5</td><td>2</td></tr><tr class="even"><td>3</td><td>1</td><td>⇩</td></tr></tbody></table>

**Step 8**

<table><thead><tr class="header"><th>4</th><th>6</th><th>7</th></tr></thead><tbody><tr class="odd"><td>8</td><td>5</td><td>⇩</td></tr><tr class="even"><td>3</td><td>1</td><td>2</td></tr></tbody></table>

**Step 9**

<table><thead><tr class="header"><th>4</th><th>6</th><th>⇨</th></tr></thead><tbody><tr class="odd"><td>8</td><td>5</td><td>7</td></tr><tr class="even"><td>3</td><td>1</td><td>2</td></tr></tbody></table>

**Step 10**

<table><thead><tr class="header"><th>4</th><th>⇧</th><th>6</th></tr></thead><tbody><tr class="odd"><td>8</td><td>5</td><td>7</td></tr><tr class="even"><td>3</td><td>1</td><td>2</td></tr></tbody></table>

**Step 11**

<table><thead><tr class="header"><th>4</th><th>5</th><th>6</th></tr></thead><tbody><tr class="odd"><td>8</td><td>⇧</td><td>7</td></tr><tr class="even"><td>3</td><td>1</td><td>2</td></tr></tbody></table>

**Step 12**

<table><thead><tr class="header"><th>4</th><th>5</th><th>6</th></tr></thead><tbody><tr class="odd"><td>8</td><td>1</td><td>7</td></tr><tr class="even"><td>3</td><td>⇦</td><td>2</td></tr></tbody></table>

**Step 13**

<table><thead><tr class="header"><th>4</th><th>5</th><th>6</th></tr></thead><tbody><tr class="odd"><td>8</td><td>1</td><td>7</td></tr><tr class="even"><td>3</td><td>2</td><td>⇩</td></tr></tbody></table>

**Step 14**

<table><thead><tr class="header"><th>4</th><th>5</th><th>6</th></tr></thead><tbody><tr class="odd"><td>8</td><td>1</td><td>⇨</td></tr><tr class="even"><td>3</td><td>2</td><td>7</td></tr></tbody></table>

**Step 15**

<table><thead><tr class="header"><th>4</th><th>5</th><th>6</th></tr></thead><tbody><tr class="odd"><td>8</td><td>⇧</td><td>1</td></tr><tr class="even"><td>3</td><td>2</td><td>7</td></tr></tbody></table>

**Step 16**

<table><thead><tr class="header"><th>4</th><th>5</th><th>6</th></tr></thead><tbody><tr class="odd"><td>8</td><td>2</td><td>1</td></tr><tr class="even"><td>3</td><td>⇨</td><td>7</td></tr></tbody></table>

**Step 17**

<table><thead><tr class="header"><th>4</th><th>5</th><th>6</th></tr></thead><tbody><tr class="odd"><td>8</td><td>2</td><td>1</td></tr><tr class="even"><td>⇩</td><td>3</td><td>7</td></tr></tbody></table>

**Step 18**

<table><thead><tr class="header"><th>4</th><th>5</th><th>6</th></tr></thead><tbody><tr class="odd"><td>⇩</td><td>2</td><td>1</td></tr><tr class="even"><td>8</td><td>3</td><td>7</td></tr></tbody></table>

**Step 19**

<table><thead><tr class="header"><th>⇦</th><th>5</th><th>6</th></tr></thead><tbody><tr class="odd"><td>4</td><td>2</td><td>1</td></tr><tr class="even"><td>8</td><td>3</td><td>7</td></tr></tbody></table>

**Step 20**

<table><thead><tr class="header"><th>5</th><th>⇦</th><th>6</th></tr></thead><tbody><tr class="odd"><td>4</td><td>2</td><td>1</td></tr><tr class="even"><td>8</td><td>3</td><td>7</td></tr></tbody></table>

**Step 21**

<table><thead><tr class="header"><th>5</th><th>6</th><th>⇧</th></tr></thead><tbody><tr class="odd"><td>4</td><td>2</td><td>1</td></tr><tr class="even"><td>8</td><td>3</td><td>7</td></tr></tbody></table>

**Step 22**

<table><thead><tr class="header"><th>5</th><th>6</th><th>1</th></tr></thead><tbody><tr class="odd"><td>4</td><td>2</td><td>⇨</td></tr><tr class="even"><td>8</td><td>3</td><td>7</td></tr></tbody></table>

**Step 23**

<table><thead><tr class="header"><th>5</th><th>6</th><th>1</th></tr></thead><tbody><tr class="odd"><td>4</td><td>⇧</td><td>2</td></tr><tr class="even"><td>8</td><td>3</td><td>7</td></tr></tbody></table>

**Step 24**

<table><thead><tr class="header"><th>5</th><th>6</th><th>1</th></tr></thead><tbody><tr class="odd"><td>4</td><td>3</td><td>2</td></tr><tr class="even"><td>8</td><td>⇨</td><td>7</td></tr></tbody></table>

**Step 25**

<table><thead><tr class="header"><th>5</th><th>6</th><th>1</th></tr></thead><tbody><tr class="odd"><td>4</td><td>3</td><td>2</td></tr><tr class="even"><td>⇩</td><td>8</td><td>7</td></tr></tbody></table>

**Step 26**

<table><thead><tr class="header"><th>5</th><th>6</th><th>1</th></tr></thead><tbody><tr class="odd"><td>⇩</td><td>3</td><td>2</td></tr><tr class="even"><td>4</td><td>8</td><td>7</td></tr></tbody></table>

**Step 27**

<table><thead><tr class="header"><th>⇦</th><th>6</th><th>1</th></tr></thead><tbody><tr class="odd"><td>5</td><td>3</td><td>2</td></tr><tr class="even"><td>4</td><td>8</td><td>7</td></tr></tbody></table>

**Step 28**

<table><thead><tr class="header"><th>6</th><th>⇦</th><th>1</th></tr></thead><tbody><tr class="odd"><td>5</td><td>3</td><td>2</td></tr><tr class="even"><td>4</td><td>8</td><td>7</td></tr></tbody></table>

**Step 29**

<table><thead><tr class="header"><th>6</th><th>1</th><th>⇧</th></tr></thead><tbody><tr class="odd"><td>5</td><td>3</td><td>2</td></tr><tr class="even"><td>4</td><td>8</td><td>7</td></tr></tbody></table>

**Step 30**

<table><thead><tr class="header"><th>6</th><th>1</th><th>2</th></tr></thead><tbody><tr class="odd"><td>5</td><td>3</td><td>⇨</td></tr><tr class="even"><td>4</td><td>8</td><td>7</td></tr></tbody></table>

**Step 31**

<table><thead><tr class="header"><th>6</th><th>1</th><th>2</th></tr></thead><tbody><tr class="odd"><td>5</td><td>⇧</td><td>3</td></tr><tr class="even"><td>4</td><td>8</td><td>7</td></tr></tbody></table>

**Step 32**

<table><thead><tr class="header"><th>6</th><th>1</th><th>2</th></tr></thead><tbody><tr class="odd"><td>5</td><td>8</td><td>3</td></tr><tr class="even"><td>4</td><td>⇨</td><td>7</td></tr></tbody></table>

**Step 33**

<table><thead><tr class="header"><th>6</th><th>1</th><th>2</th></tr></thead><tbody><tr class="odd"><td>5</td><td>8</td><td>3</td></tr><tr class="even"><td>⇩</td><td>4</td><td>7</td></tr></tbody></table>

**Step 34**

<table><thead><tr class="header"><th>6</th><th>1</th><th>2</th></tr></thead><tbody><tr class="odd"><td>⇩</td><td>8</td><td>3</td></tr><tr class="even"><td>5</td><td>4</td><td>7</td></tr></tbody></table>

**Step 35**

<table><thead><tr class="header"><th>⇦</th><th>1</th><th>2</th></tr></thead><tbody><tr class="odd"><td>6</td><td>8</td><td>3</td></tr><tr class="even"><td>5</td><td>4</td><td>7</td></tr></tbody></table>

**Step 36**

<table><thead><tr class="header"><th>1</th><th>⇦</th><th>2</th></tr></thead><tbody><tr class="odd"><td>6</td><td>8</td><td>3</td></tr><tr class="even"><td>5</td><td>4</td><td>7</td></tr></tbody></table>

**Step 37**

<table><thead><tr class="header"><th>1</th><th>2</th><th>⇧</th></tr></thead><tbody><tr class="odd"><td>6</td><td>8</td><td>3</td></tr><tr class="even"><td>5</td><td>4</td><td>7</td></tr></tbody></table>

**Step 38**

<table><thead><tr class="header"><th>1</th><th>2</th><th>3</th></tr></thead><tbody><tr class="odd"><td>6</td><td>8</td><td>⇨</td></tr><tr class="even"><td>5</td><td>4</td><td>7</td></tr></tbody></table>

**Step 39**

<table><thead><tr class="header"><th>1</th><th>2</th><th>3</th></tr></thead><tbody><tr class="odd"><td>6</td><td>⇨</td><td>8</td></tr><tr class="even"><td>5</td><td>4</td><td>7</td></tr></tbody></table>

**Step 40**

<table><thead><tr class="header"><th>1</th><th>2</th><th>3</th></tr></thead><tbody><tr class="odd"><td>⇧</td><td>6</td><td>8</td></tr><tr class="even"><td>5</td><td>4</td><td>7</td></tr></tbody></table>

**Step 41**

<table><thead><tr class="header"><th>1</th><th>2</th><th>3</th></tr></thead><tbody><tr class="odd"><td>5</td><td>6</td><td>8</td></tr><tr class="even"><td>⇦</td><td>4</td><td>7</td></tr></tbody></table>

**Step 42**

<table><thead><tr class="header"><th>1</th><th>2</th><th>3</th></tr></thead><tbody><tr class="odd"><td>5</td><td>6</td><td>8</td></tr><tr class="even"><td>4</td><td>⇦</td><td>7</td></tr></tbody></table>

**Step 43**

<table><thead><tr class="header"><th>1</th><th>2</th><th>3</th></tr></thead><tbody><tr class="odd"><td>5</td><td>6</td><td>8</td></tr><tr class="even"><td>4</td><td>7</td><td>⇩</td></tr></tbody></table>

**Step 44**

<table><thead><tr class="header"><th>1</th><th>2</th><th>3</th></tr></thead><tbody><tr class="odd"><td>5</td><td>6</td><td>⇨</td></tr><tr class="even"><td>4</td><td>7</td><td>8</td></tr></tbody></table>

**Step 45**

<table><thead><tr class="header"><th>1</th><th>2</th><th>3</th></tr></thead><tbody><tr class="odd"><td>5</td><td>⇨</td><td>6</td></tr><tr class="even"><td>4</td><td>7</td><td>8</td></tr></tbody></table>

**Step 46**

<table><thead><tr class="header"><th>1</th><th>2</th><th>3</th></tr></thead><tbody><tr class="odd"><td>⇧</td><td>5</td><td>6</td></tr><tr class="even"><td>4</td><td>7</td><td>8</td></tr></tbody></table>

**Step 47**

<table><thead><tr class="header"><th>1</th><th>2</th><th>3</th></tr></thead><tbody><tr class="odd"><td>4</td><td>5</td><td>6</td></tr><tr class="even"><td>⇦</td><td>7</td><td>8</td></tr></tbody></table>

**Step 48**

<table><thead><tr class="header"><th>1</th><th>2</th><th>3</th></tr></thead><tbody><tr class="odd"><td>4</td><td>5</td><td>6</td></tr><tr class="even"><td>7</td><td>⇦</td><td>8</td></tr></tbody></table>

**Step 49**

<table><thead><tr class="header"><th>1</th><th>2</th><th>3</th></tr></thead><tbody><tr class="odd"><td>4</td><td>5</td><td>6</td></tr><tr class="even"><td>7</td><td>8</td><td></td></tr></tbody></table>

\*Note: This was much easier to document on paper.

## Lessons Learned:

1.  In solving problems, you are sometimes faced with situations where you wont' see a clear path to code a solution. You must never use that as an excuse to forgo planning and systematic approaches.

2.  Sometimes problems are divisible in ways that aren't immediately obvious. Looking for a way to divide a problem is usually time well spent.

3.  Even if you are unable to find a clean division, you may learn something about the problem that helps you solve it.

"When solving problems, working with a specific goal in mind is always better than random effort, whether you achieve that specific goal or not."

---

## Problem: The Quarrasi Lock

A hostile alien race, the Quarrasi, has landed on Earth, and you've been captured. You've managed to overpower your guards, even though they are enormous and tentacled, but to escape the (still grounded) spaceship, you have to open the massive door. The instructions for opening the door are, oddly enough, written in English but it's still no piece of cake. To open the door, you have to slide the three bar-shaped Kratzz along tracks that lead from the right receptor to the left receptor, which lies at the end of the door, 10 feet away.

That's easy enough, but you have to avoid setting off the alarms, which work as follows. On each Kratzz are one or more star-shaped crystal power gems known as Quinicrys. Each receptor has four sensors that light up if the number of Quinicrys in the column above is even. An alarm goes off if the number of lit sensors is ever exactly one. Note that each receptor's alarm is separate: You can't ever have exactly one sensor lit for the left receptor or for the right receptor. The good news is that each alarm is equipped with a suppressor, which keeps the alarm from sounding as long as the button is pressed. If you could press both suppressors at once, the problem would be easy, but you can't since you have short human arms rather than long Quarrasi tentacles.

Given all of this, how would you slide the Kratzz to open the door without activating either alarm?

<table><thead><tr class="header"><th>L</th><th>e</th><th>f</th><th>t</th><th></th><th></th><th></th><th>R</th><th>i</th><th>g</th><th>h</th><th>t</th></tr></thead><tbody><tr class="odd"><td>‖</td><td>‖</td><td>‖</td><td>‖</td><td></td><td></td><td></td><td></td><td>‖</td><td>‖</td><td>‖</td><td>‖</td></tr><tr class="even"><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr class="odd"><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>★</td><td></td><td>★</td><td>★</td></tr><tr class="even"><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr class="odd"><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>★</td><td>★</td><td></td><td></td></tr><tr class="even"><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr class="odd"><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td></td><td>★</td><td></td><td></td></tr><tr class="even"><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr class="odd"><td>0</td><td>0</td><td>0</td><td>0</td><td></td><td></td><td></td><td></td><td>1</td><td>1</td><td>0</td><td>0</td></tr></tbody></table>

## Restate Problem Constraints

1.  Need to slide 3 bars from right to left
2.  On each bar, there are one or more star-shaped gems
3.  Each receptor (side) has one sensor per column and will light if the number of stars in a column is even
4.  If exactly one sensor is lit on a receptor, the alarm will go off
5.  Cannot allow an alarm to go off
6.  Alarms can be suppressed, but only if you are on the same side as the alarm

## Operations

1.  Move bars from one side to another
2.  Make sure there is never just one even column on a side

### Bad combinations (will result in alarm)

1.  Top bar + middle bar
2.  Middle bar + bottom bar

## Good combination (will not result in alarm)

1.  Top bar + bottom bar

<table><thead><tr class="header"><th>Left</th><th>Left<br />
Suppressor</th><th></th><th>⇦</th><th></th><th>In Transit</th><th></th><th>⇨</th><th></th><th>Right<br />
Suppressor</th><th>Right</th></tr></thead><tbody><tr class="odd"><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td>Top,<br />
Middle,<br />
Bottom</td></tr><tr class="even"><td></td><td></td><td></td><td>⇦</td><td></td><td>Middle</td><td></td><td></td><td></td><td></td><td>Top,<br />
Bottom</td></tr><tr class="odd"><td>Middle</td><td></td><td></td><td></td><td></td><td></td><td></td><td>⇨</td><td></td><td></td><td>Top,<br />
Bottom</td></tr><tr class="even"><td>Middle</td><td></td><td></td><td>⇦</td><td></td><td>Top</td><td></td><td></td><td></td><td></td><td>Bottom</td></tr><tr class="odd"><td>Top,<br />
Middle</td><td>Yes</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td>Bottom</td></tr><tr class="even"><td>Top</td><td></td><td></td><td></td><td></td><td>Middle</td><td></td><td>⇨</td><td></td><td></td><td>Bottom</td></tr><tr class="odd"><td>Top</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td>Yes</td><td>Middle,<br />
Bottom</td></tr><tr class="even"><td>Top</td><td></td><td></td><td>⇦</td><td></td><td>Bottom</td><td></td><td></td><td></td><td></td><td>Middle</td></tr><tr class="odd"><td>Top,<br />
Bottom</td><td></td><td></td><td></td><td></td><td></td><td></td><td>⇨</td><td></td><td></td><td>Middle</td></tr><tr class="even"><td>Top,<br />
Bottom</td><td></td><td></td><td>⇦</td><td></td><td>Middle</td><td></td><td></td><td></td><td></td><td></td></tr><tr class="odd"><td>Top,<br />
Middle,<br />
Bottom</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>

## Lesson Learned

Importance of recognizing analogies. Quarrasi Lock is analogous to fox, goose, and corn problem. If we can discover that analogy early enough, we can avoid most of the work of the problem by translating our solution for the first problem.

[Problem solving](../tags/problem%20solving/index.html)[Think Like a Programmer](../tags/think%20like%20a%20programmer/index.html)

### &lt;&lt; Previous: Programming Foundations: Data Structures

### &gt;&gt; Next: Think Like a Programmer: Pure Puzzles
