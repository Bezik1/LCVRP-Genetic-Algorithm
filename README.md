# 🧬 LCVRP Genetic Algorithm

## 💡 Overview

This project goal was to find the best soultion for the
`Limited Capacitated Vehicle Routing Problem (LcVRP)`. To
achieve it we had to used `Genetic Algorithm (GA)` written
in lower level `C++`, with the code optimized down to the last
detail.

## ⚙️ Commands

Note:
In case of path error, modify the `ProblemLoader::BASE_PATH`,
`ProblemLoader::BASE_EXTENSION`, folderName or instanceName parameters.

```bash
# Initialize build directory
cmake -S . -B build

# Builds project
cmake --build build --target main

# Run project
./build/main
```

## Parameters

```C++
int populationSize;     // Controls the size of the population
double mutProb;         // Controls probability for mutation occurances
double crossoverProb;   // It's the probability for solution crossing, when it did not occur we simply copy indivduals
int numTurns;           // Number of turns, at which tournament selection will be looking for mate
int numEpochs;          // How many times Optimizer::runIteration will be invoked
int numGroups;          // Number of groups of trucks to optimize
```

## 📚 Documentation

Generate Documentation Template

```bash
# Generates documentation
doxygen -g

# Updates documentation
doxygen

# Run documentation
./docs/html/index.html
```

Custom Operators: Overloads < and > to facilitate integration with the HeapSort algorithm.

<p align="center">
    <a href="https://skillicons.dev">
        <img src="https://skillicons.dev/icons?i=cpp,vscode,github,git" />
    </a>
</p>
