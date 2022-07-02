# GeneCluster

A library for using genetic algorithm for auto clustering failures and reliability incidents.

The idea is to run multiple ETL functions, each generating a score from 0.0-1.0. Gathering this in a vector like a gene. Then compare the affinity of that gene with previously known failures.

I used this before in testing highly concurrent C++ application that used to have a lot of crashes reducing the analysis time to only few minutes!

I can't use the old implementation so this project is to recreate this library in multiple languages.

## Concepts borrowed from Genetic Algorithms

* A failure signature is similar to a chromosome in genetic algorithm.
* Each feature (gene) was extracted independently. Some are simple like run metadata. some are more involved like thrown exceptions, or failing stack.
* An analysis profile is a collection of weights that are applied to guide the analysis when we look for matches
* Signature with too few information is dropped as being to generic (black holes)

![image](https://user-images.githubusercontent.com/3342359/177013476-4f84c1ca-3ff6-4217-a654-78c8f9285e9e.png)

* No fancy Self Organizing Map (SOM):
  * provide a compare function for each feature
  * We measure the Cartesian distance

![image](https://user-images.githubusercontent.com/3342359/177013452-996c663a-05bf-4647-af6b-ebbe19651d3e.png)



Help appreciated :-)
