# 8queens-evolutionary

A solution to the 8 queen problem using the evolutionary algorithm approach.



# Evolutionary algorithms

Evolutionary algorithms are based on the Darwinian concept of evolution. It usually follows the following steps:

1. Initialize the population randomly

2. Calculate the fitness of each individual

3. Select individuals to reproduce based on some rule influenced by the fitness

4. Recombine the selected parents to generate new sons.

   - Crossover

   - Mutation  



The main difficulty in the evolution process is to find a good balance between exploration of the problem space and exploitation of local minima. Increases in crossover and mutation probability usually lead to an increase in exploration. On the other hand, a small recombination probability leads to sons being more similar to their parents, which causes an increase in exploitation. Other means of increasing exploitation involve:



- Elitist parent selection

- Crossover rules biased towards preservation of parent genotype

- Mutation probability set to low  



However, if the algorithm is too biased toward exploitation this may lead to early convergence, which may not offer the desired solution.



# 8 Queens 

The 8 queens problem is to find a chessboard configuration where 8 queens so that no two queens threaten each other. This problem is NP-complete which makes large boards unfeasible to solve algorithmically. Many approaches have been proposed to offer a solution to the problem, they are usually based on a given heuristic.



# Our Approach

We developed a standard evolutionary algorithm to solve the 8 queens problem.

- Fitness function: The sum of all conflicts on a given board 

- Parent selection: Two parents were randomly picked out of the 5 best individuals in the population

- Recombination

    - Crossover:

      - Standart crossover

      - Crossover at the edges of the array

    - Mutation:

      - Standart mutation

    - Dynamic tuning of crossover and mutation probability



# Evaluation Metrics

The following metrics were used to evaluate the performance of a given architecture:

- Num of epochs to reach convergence

  - Average num of epochs

  - Mean num of epochs

- Best individual fitness

- Standard fitness deviation

- Average fitness

