# 8queens-evolutionary
A solution to the 8 queen problem using the evolutionary algorithm approach.

# Evolutionary algorithms
Evolutionary algorithms are based on the darwinian concept of evolution. It usualy follows the following steps:
1. Initialize population randomly
2. Calculate fitness of each individual
3. Select individuals to reproduce based on some rule influenced by the fitness
4. Recombine the selected parents to generate new sons.
   - Crossover
   - Mutation  
The main difficulty on the evolution process is to find a good balance between exploration of the problem space and exploitation of local minima. Increases on crossover and mutation probability usualy lead to an increase of exploration. On the other hand, a small recombination probability leads to sons being more similar to their parents, which causes an increase of exploitation. Other means of increasing exploitation involve:

- Elistis parent selection
- Crossover rules biased towards preservation of parent genotype
- Mutation probability set to low  

However, if the algorithm is too biased toward exploitation this may led to early convergence, which may not offer a desired solution.

# 8 Queens 
The 8 queens problem is to find a chessboard configuration where 8 queens so that no two queens threaten each other. This problem is NP complete wich makes large boards unfeasible to solve algorithmically. Many approaches have been proposed to offer a solution to the problem, they are usually based on a give heuristic.

# Our Approach
We developed a standart evolutionary algorithm to solve the 8 queens problem.
- Fitness function: The sum of all conflicts on a given board 
- Parent selection: Two parents randomly picker out of the 5 best individuals of the population
- Recombination
    - Crossover:
      - Standart crossover
      - Crossover at the edges of the array
    - Mutation:
      - Standart mutation
    - Dynamic tuning of crossover and mutation probability

# Evaluation Metrics
The following metrics were used to evaluate performance of a given architecture:
- Num of epochs to reach convergence
  - Average num of epochs
  - Mean num of epochs
- Best invidual fitness
- Standart fitness deviation
- Average fitnes
