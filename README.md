# JuliaCon'21: Set Propagation with Applications

Minisymposium that took place at JuliaCon 2021.

## Title

- Set Propagation Methods in Julia: Techniques and Applications

## Roles

- Organisers:
    - Marcelo Forets ([@mforets](http://github.com/mforets)), UdelaR
    - Christian Schilling ([@schillic](http://github.com/schillic/)), Univ. Konstanz

- Moderator/Chair: 
    - David P. Sanders ([@dpsanders](http://github.com/dpsanders)), UNAM, MIT

## Abstract

This minisymposium presents modern approaches to analyze a variety of mathematical systems in Julia, via set propagation techniques: dynamical systems, cyber-physical systems, probabilistic systems, and neural networks. To deploy those systems in the real world there is an increasing demand for safe and reliable models. The speakers represent a broad cross-section of work from different fields in the directions of set-based techniques and global optimization to address  such challenges.

## Description

A new generation of algorithms is addressing the fundamental challenge of how to exhaustively explore all possible scenarios for simulation of dynamical systems under model uncertainties. Moreover, deep neural networks play an increasing role in control and safety-critical applications, although it is often not known how to guarantee that they will behave correctly and safely under all circumstances. This minisymposium will host applications of set-based techniques and global optimization in Julia that address these questions.

We have deliberately reached out to several different groups working on set propagation techniques and their application in a wide range of areas, in order to present a broad overview of the contributions that Julia is bringing to this exciting area.

More specifically, the following talks are planned:

### Introductory talk

- Speaker: Goran Frehse (Hybrid Systems Semantics group, Computer Science and System Engineering Laboratory (U2IS), ENSTA Paris; [webpage](https://sites.google.com/site/frehseg/home)).

- ~10 mins. Invited expert in the domain of the minisymposium (non-Julia-specific).

- Goran Frehse has a Diploma in Electrical Engineering and Information Technology from Karlsruhe Institute of Technology, Germany, and a PhD in Computer Science from Radboud University Nijmegen, the Netherlands. From 2006 to 2018, he was an associate professor at the University Grenoble Alpes, from which he obtained a habilitation in 2016. From 2016 to 2018, he held a research chair (Chaire Initiative Universitaire Alpes) at the Univ. Grenoble Alpes. Since 2018, he is a professor at ENSTA Paris, where he continues his research on safe cyber-physical systems. He is the architect and lead developer of two popular model checking tools for hybrid and cyber-physical systems, [PHAVer](http://www-verimag.imag.fr/~frehse/phaver_web/) and [SpaceEx](http://spaceex.imag.fr/). He is coauthor of the revew article [Set Propagation Techniques for Reachability Analysis
](https://www.annualreviews.org/doi/abs/10.1146/annurev-control-071420-081941).

### Combining Set Propagation with Finite Element Methods for Time Integration in Transient Solid Mechanics Problems

- By Jorge P??rez Zerpa ([@jorgepz](http://github.com/jorgepz)) UdelaR (speaker), Marcelo Forets ([@mforets](http://github.com/mforets)) and Daniel Freire Caporale ([@dfcaporale](http://github.com/dfcaporale)). 

- Links: [arXiv preprint](https://arxiv.org/abs/2105.05841), [Repeatability Evaluation](https://github.com/JuliaReach/RFEM_RE) package.

- The Finite Element Method (FEM) is the gold standard for numerical simulation in transient solid mechanics problems. Several time-integration algorithms have been developed in recent decades; however, it is still a challenging problem to completely describe the family of dynamically-feasible behaviors from given sets of initial states. In this talk we present a different, set-based approach, motivated by recent advances in the field of Reachability Analysis (RA): by propagating the sets given in the problem formulation, we obtain **flowpipes**, i.e. unions of sets enclosing the infinitely many solutions of the problems. We show that the full potential of RA in solid mechanics problems is yet to be explored.

### Dionysos.jl: Optimal Control of Cyber-Physical Systems.

- By Benoit Legat ([@blegat](https://github.com/blegat)), UCLouvain, Guillaume Berger ([guberger](github.com/guberger)), Julien Calbert ([JulienCalbert](github.com/JulienCalbert)) (speaker) and Rapha??l Jungers ([raphaeljungers](github.com/raphaeljungers)). 

- [Dionysos.jl](https://github.com/dionysos-dev/Dionysos.jl) is software produced by the ERC project Learning to Control (L2C). In view of the Cyber-Physical Revolution, the only sensible way of controlling these complex systems is often by discretizing the different variables, thus transforming the model into a simple combinatorial problem on a finite-state automaton, called an abstraction of this system. The goal of L2C is to transform this approach into an effective, scalable, cutting-edge technology that will address the challenges of Cyber-Physical Systems and unlock their potential. This ambitious goal will be achieved by leveraging powerful tools from Mathematical Engineering.

### Solving Optimization Problems with Embedded Dynamical Systems.

- By Matthew Wilhelm ([@mewilhel](https://github.com/mewilhel), Univ. Connecticut and Matthew Stuber ([@MatthewStuber](https://github.com/MatthewStuber)), Univ. Connecticut.

- We will discuss our recent work on the [EAGODynamicOptimizer.jl](https://github.com/PSORLab/EAGODynamicOptimizer.jl) and [DynamicBounds.jl](https://github.com/PSORLab/DynamicBounds.jl) packages. These extend our [EAGO.jl](https://github.com/PSORLab/EAGO.jl) nonconvex optimizer to address formulations containing embedded dynamical systems. We highlight a series of approaches for constructing the requisite convex and concave relaxations of differential equations in the original decision space and discuss the use of such techniques in a global optimization context. These methods may readily be composed with existing McCormick relaxation approaches, which allows for the solution of general nonlinear formulations to certified global optimality. Use cases relevant to hybrid data-driven process modeling, parameter estimation, and worst-case robust design are discussed.

### Computing with sets of probabilities in Julia

- By Ander Gray ([@AnderGray](http://github.com/AnderGray)), Univ. Liverpool.  
 
- There are many ways to mathematically define a set of probability distributions, including: intervals, possibility distributions, random sets and probability boxes (p-boxes). These structures were discovered independently from one another, but are often synonymous and can be translated. Imprecise Probability theory links all these theories into one. In this presentation, we present [ProbabilityBoundsAnalysis.jl](https://github.com/AnderGray/ProbabilityBoundsAnalysis.jl), a numerical implementation of p-box arithmetic in Julia, which gives an arithmetic of random variables where both marginal distributions and dependencies may be partially defined. We show how Probability Bounds Analysis may be used to rigorously propagate distributions and p-boxes in reachability problems using [ReachabilityAnalysis.jl](https://github.com/JuliaReach/ReachabilityAnalysis.jl).


### Methods to Soundly Verify Deep Neural Networks

- By Tomer Arnon ([@tomerarnon](https://github.com/tomerarnon)), Stanford.

- Deep neural networks are widely used for nonlinear function approximation, with applications ranging from computer vision to control. Although these networks involve the composition of simple arithmetic operations, it can be very challenging to verify whether a particular network satisfies certain input-output properties. [NeuralVerification.jl](https://github.com/sisl/NeuralVerification.jl) implements several methods that have emerged recently for soundly verifying such properties. These methods borrow insights from reachability analysis, optimization, and search. We discuss fundamental differences and connections between existing algorithms and we provide pedagogical implementations of existing methods and compare them on a set of benchmark problems.
 
