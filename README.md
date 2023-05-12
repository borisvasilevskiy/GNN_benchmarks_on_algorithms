# GNN benchmarks on algorithms
Benchmarking existing GNN approaches on algorithmically solvable tasks

## Motivation

Evaluating GNN approach on a dataset that can be solved algorithmically might be a nice way to understand pros and cons of each approach.

One can select degree of locality needed to solve the task. E.g. if the task is to calculate # of neighbors - 1 GNN layer should be sufficient to tackle the problem. If the task is to calculate the shortest path to the given node then it's clear that no limited-layer GNN will have 100% accuracy.

## Benchmarking tasks

1. For each node, calculate the number of neighbors.
2. Determine if the graph is planar. This task is linearly-solvable (https://en.wikipedia.org/wiki/Planarity_testing#:~:text=In%20graph%20theory%2C%20the%20planarity,the%20plane%20without%20edge%20intersections). The theorem says the graph shouldn't contain K_5 and K_{3,3} subgraphs. It implies that all sufficient information should be possible to collect from 2-step neighbourhood of each node (therefore, 2-layer GNN might already solve the problem).

## Approaches

1. Node2vec
2. DeepWalk
