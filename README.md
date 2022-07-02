# GeneCluster

A library for using genetic algorithm for auto clustering failures and reliability incidents.

The idea is to run multiple ETL functions, each generating a score from 0.0-1.0. Gathering this in a vector like a gene. Then compare the affinity of that gene with previously known failures.

I used this before in testing highly concurrent C++ application that used to have a lot of crashes reducing the analysis time to only few minutes!

I can't use the old implementation so this project is to recreate this library in multiple languages.

Help appreciated :-)
