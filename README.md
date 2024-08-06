# Assignment-1
Assignment 1 of Formal Languages and Compilation.
Description of the code itself.  BORRAR DESPUES
Certainly! Let's go through the code step by step and explain what each part does:

1. The `minimize_dfa` function takes a list of `cases` as input. Each `case` is a dictionary containing information about a DFA (Deterministic Finite Automaton) that needs to be minimized.

2. For each `case` in the `cases` list, the function performs the following steps:

   a. Extracts the necessary information from the `case` dictionary, including the number of states (`n`), the alphabet, the final states, and the transition table.

   b. Step 2: Create equivalent state groups. Initially, the equivalent groups are set to two groups: the final states and the non-final states.

   c. Step 4: Iterate until no more state groups can be collapsed. This step is the core of the DFA minimization algorithm. It repeatedly checks for different transitions between states and splits the groups accordingly.

   d. Inside the loop, a new list `new_equivalent_groups` is created to store the updated groups after each iteration.

   e. For each group in the `equivalent_groups`, a dictionary `group_dict` is created to store the transitions of each state in the group.

   f. Step 4b: Check for different transitions. It compares the transitions of each state in the group for each symbol in the alphabet. If there are different transitions for any symbol, it splits the group into two new groups: one with states having the same transitions and the other with states having different transitions.

   g. The new groups are added to the `new_equivalent_groups` list.

   h. Once all the groups have been checked, the `new_equivalent_groups` list is compared with the `equivalent_groups` list. If they are the same, it means no more state groups can be collapsed, and the loop is exited.

   i. If the `new_equivalent_groups` list is different from the `equivalent_groups` list, it means there are still state groups that can be collapsed. The `equivalent_groups` list is updated with the `new_equivalent_groups` list, and the loop continues.

   j. Step 6: Print the final equivalent state groups. Once the loop is exited, the function prints the final equivalent state groups.

That's a high-level overview of what the code does. It implements the DFA minimization algorithm, which aims to reduce the number of states in a DFA while preserving its behavior. The algorithm works by iteratively identifying and merging equivalent states until no more merges can be made. The resulting equivalent state groups represent the minimized DFA.


BORRAR LO DE ARRIBA - NOES NECESARIO
