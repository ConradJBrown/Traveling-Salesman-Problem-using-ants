# Traveling-Salesman-Problem-using-ants
This is a program for optimizing an ant colony for the traveling salesman problem.

## Description
write code that allows an ant algorithm to find optimal paths for TSP.

Your specific task is to write the code that selects which node an ant will visit next.  This is the core of an ant algorithm, and the trickiest part to get right!

After you've completed this assignment you'll find a class called AntDriver.java in the RESOURCES module that will allow you to run a full simulation of ACO for TSP, using your code. **Code and assignment given by Dr. Mark Hatcher of Memorial University of Newfoundland**

**For this assignment you will need to write methods to perform these 6 sub-tasks:**

- determine a list of nodes not yet visited by an ant
- determine the lengths of the edges to those nodes from the current node
- determine the pheromone levels on those edges 
- determine the probability of selecting an edge based on the standard ACO Edge Selection formula
- determine the cumulative probabilities based on the above
- choose the next node to visit using roulette wheel selection

Three classes have been provided for this task: Ant.java, AntSim.java and AntTester.java.

You should keep all three of these classes in the same folder when compiling and running your work.

*Ant.java*

This class contains the six methods that you need to complete.  **This is what they need to do:**

- ***getNotVisited()***
  - return an array list of nodes not yet visited by this ant
  - each node is represented by an integer
  - the input parameter is a boolean array visited[]
    - where visited[i] == true if node i has been visited by this ant
- ***getLengths()***
    - return the lengths of the edges leading to nodes not yet visited by this ant
- ***getLevels()***
  - return the pheromone levels of the edges leading to nodes not yet visited by this ant
- ***getProbabilities()***
  - calculates and returns the probabilities of choosing each edge that leads a node not yet visited
  - must use the standard ACO Edge Selection formula, as provided in the class slides:
    - p(choose edge i) = (τi^⍺ . ηi^β) / Σn(τi^⍺ . ηi^β) :
      - τi = level of pheromone on edge i
      - ηi = 1/(length of edge i)
- ***getCumulativeProbabilities()***
  - return list of cumulative probabilities of choosing edges based on the list of probabilities above
- ***chooseNextNode()***
  - choose the next node to visit using roulette wheel selection
  - will return an integer in range [0,n-1], where n = cumulative.size()
  
## How to run
  - To run this coude you just need to run the antdriver.java file, this is a file given to me for the assingment to test the code i have written.
