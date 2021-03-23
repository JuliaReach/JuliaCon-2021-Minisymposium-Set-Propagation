# JuliaCon'21: Set Propagation Applications

Minisymposium (proposal) for the JuliaCon 2021.

## Title

- Set Propagation Techniques with Applications in Control and Deep Learning


## Roles

- Organisers:
    - Marcelo Forets ([@mforets](http://github.com/mforets)), UdelaR
    - Christian Schilling ([@schillic](http://github.com/schillic/)), Univ. Konstanz
    - David P. Sanders ([@dpsanders](http://github.com/dpsanders)), UNAM, MIT

- Moderator/Chair: 
    - David P. Sanders ([@dpsanders](http://github.com/dpsanders)), UNAM, MIT

## Abstract (500 characters)

This minisymposium presents modern approaches to analyze a variety of mathematical systems in Julia: dynamical systems, cyber-physical systems, probabilistic systems, and neural networks. To deploy those systems in the real world there is an increasing demand of software that can ensure safety and reliability under all feasible scenarios. Set-based techniques and global optimization are being developed to address such challenge.

## Description (5000 characters)

A new generation of algorithms is addressing the fundamental challenge of how to exhaustively explore all possible scenarios for simulation of dynamical systems under model uncertainties. Moreover, deep neural networks take an increasing role in control and safety-critical applications, although it is not known how to guarantee that they will behave correctly and safely under all circumstances. This minisymposium will host applications of set-based techniques and global optimization in Julia.

More specifically, the following talks are planned:

- Introductory talk (10min) from an expert in the field of reachability analysis and cyber-physical systems. Non Julia-specific.

- Five (20min) talks from scientists and Julia package developers:

**Talk (A)** Using Set Propagation and the Finite Element Method For Time Integration in Transient Solid Mechanics Problems. By Jorge Pérez Zerpa ([@jorgepz](http://github.com/jorgepz)), UdelaR (speaker), Marcelo Forets ([@mforets](http://github.com/mforets)), UdelaR, and Daniel Freire Caporale ([@dfcaporale](http://github.com/dfcaporale)), UdelaR. The Finite Element Method (FEM) is the gold standard for the numerical simulation in transient solid mechanics problems. Several time integration algorithms have been developed in recent decades, however it is still a challenging problem to completely describe the family of dynamically feasible behaviors under given sets of initial states. In this talk we present a different, set-based approach motivated by recent advances in the field of Reachability Analysis (RA): by propagating the sets given in the problem formulation, we obtain flowpipes, unions of sets enclosing the infinitely many solutions of the problems. We show that the full potential of RA in solid mechanics problems is yet to be explored.

**Talk (B)** Dionysos.jl: Optimal Control of Cyber-Physical Systems, from Benoit Legat ([@blegat](http://github.com/blegat)), UCLouvain. Dionysos is the software of the ERC project Learning to control (L2C). In view of the Cyber-Physical Revolution, the only sensible way of controlling these complex systems is often by discretizing the different variables, thus transforming the model into a simple combinatorial problem on a finite-state automaton, called an abstraction of this system. The goal of L2C is to transform this approach into an effective, scalable, cutting-edge technology that will address the CPS challenges and unlock their potential. This ambitious goal will be achieved by leveraging powerful tools from Mathematical Engineering.

**Talk (C)** Solving Optimization Problems with Embedded Dynamical Systems, from Matthew Wilhelm (@mewilhel), Univ. Connecticut - Speaking and Matthew E. Wilhelm from , Univ. Connecticut. We review our recent work on the EAGODynamicOptimizer.jl and DynamicBounds.jl packages which extended the EAGO.jl nonconvex optimizer to address formulations containing embedded dynamical systems. We highlight a series of approaches for constructing the requisite convex and concave relaxations of differential equations in the original decision space and discuss the use of such techniques in a global optimization context. These methods may readily be composed with existing McCormick relaxations approaches which allows for the solution of general nonlinear formulations to certified global optimality. Use cases relevant to hybrid data-driven process modeling, parameter estimation, and worst-case robust design are discussed.


**Talk (D)** Computing with sets of probabilities in Julia, by Ander Gray ([@AnderGray](http://github.com/AnderGray)) (Univ Liverpool), [Project link](https://github.com/AnderGray/ProbabilityBoundsAnalysis.jl).  Ander Gray received an Msci in Physics from Queen’s University Belfast (2017). Since then he has been a PhD student at the University of Liverpool, studying Uncertainty Quantification. For his thesis work, Ander researches methods for efficiently propagating uncertainty in radiation transport simulations. He is also involved in developing methods and software for calibrating and propagating uncertainties through computational models, in the form of imprecise probabilities. There are many ways to mathematically define a set of probability distributions, including: intervals, possibility distributions, random sets and probability boxes (p-boxes). These structures were discovered independently from one another, but are often synonymous and can be translated. Imprecise Probability theory links all these theories into one. In this presentation, we present Probability Bounds Analysis, a numerical implementation of p-box arithmetic in Julia, which gives an arithmetic of random variables where both marginal distributions and dependencies may be partially defined. We show how Probability Bounds Analysis may be used to rigorously propagate distributions and p-boxes in reachability problems using ReachabilityAnalysis.jl.

**Talk (E)** Methods to Soundly Verify Deep Neural Networks by Tomer Arnon ([@tomerarnon](http://github.com/tomerarnon)), Stanford. Deep neural networks are widely used for nonlinear function approximation with applications ranging from computer vision to control. Although these networks involve the composition of simple arithmetic operations, it can be very challenging to verify whether a particular network satisfies certain input-output properties. NeuralVerification.jl implements several methods that have emerged recently for soundly verifying such properties. These methods borrow insights from reachability analysis, optimization, and search. We discuss fundamental differences and connections between existing algorithm and we provide pedagogical implementations of existing methods and compare them on a set of benchmark problems.



---


## Schedule

### Introductory Talk (10min)

...

### Set Propagation For Time Integration in Transient Solid Mechanics Problems (20min + 2min Q)

- Set Propagation For Time Integration in Transient Solid Mechanics Problems
    - Marcelo Forets ([@mforets](http://github.com/mforets)), UdelaR
    - Daniel Freire Caporale ([@dfcaporale](http://github.com/dfcaporale)), UdelaR
    - **Jorge Perez Zerpa** ([@jorgepz](http://github.com/jorgepz)), UdelaR
    - Project link (TO BE ADDED)

    - Description of talk:
    
        - The Finite Element Method (FEM) is the gold standard for the numerical simulation in transient solid mechanics problems. Several time integration algorithms have been developed in recent decades, however it is still a challenging problem to completely describe the family of dynamically feasible behaviors under given sets of initial states. In this talk we present a different, set-based approach motivated by recent advances in the field of Reachability Analysis (RA): by propagating the sets given in the problem formulation, we obtain flowpipes, unions of sets enclosing the infinitely many solutions of the problems. We show that the full potential of RA in solid mechanics problems is yet to be explored.


### Dionysos.jl: Optimal Control of Cyber-Physical Systems (20min + 2min Q)

- Dionysos.jl: Optimal Control of Cyber-Physical Systems
    - Benoit Legat ([@blegat](http://github.com/blegat)), UCLouvain
    - [Project link](https://github.com/dionysos-dev/Dionysos.jl)

- Dionysos is the software of the ERC project Learning to control (L2C). In view of the Cyber-Physical Revolution, the only sensible way of controlling these complex systems is often by discretizing the different variables, thus transforming the model into a simple combinatorial problem on a finite-state automaton, called an abstraction of this system. The goal of L2C is to transform this approach into an effective, scalable, cutting-edge technology that will address the CPS challenges and unlock their potential. This ambitious goal will be achieved by leveraging powerful tools from Mathematical Engineering.


### Solving Optimization Problems with Embedded Dynamic Systems (20min + 2min Q)

- Solving Optimization Problems with Embedded Dynamic Systems
    - Matthew Wilhelm ([@mewilhel](http://github.com/mewilhel)), Univ. Connecticut
    - Project link (TO BE ADDED)


- Solving Optimization Problems with Embedded Dynamical Systems.

    - Matthew Wilhelm (@mewilhel), Univ. Connecticut - Speaking.

        - Matthew E. Wilhelm received a B.S. in Applied Mathematics from the University of North Carolina at Greensboro, Greensboro, NC, USA (2009), and a M.S. in Chemical Engineering from Columbia University, New York, NY, USA (2011). He is currently a PhD Candidate in Chemical and Biomolecular Engineering at the  University of Connecticut where his research interests include: nonconvex optimization, dynamic simulation and optimization, mathematical biology, and engineering & STEM pedagogy.

    - Matthew Stuber (@MatthewStuber), Univ. Connecticut

        - Matthew D. Stuber received a Bachelor of Chemical Engineering degree from the University of Minnesota – Twin Cities (2007) and a PhD in Chemical Engineering from MIT (2012). He is currently an Assistant Professor of Chemical and Biomolecular Engineering at the University of Connecticut his research interests include: process systems engineering, design under uncertainty, renewable energy and process integration, desalination and water treatment.

    - Description of Talk:

        - We review our recent work on the EAGODynamicOptimizer.jl and DynamicBounds.jl packages which extended the EAGO.jl nonconvex optimizer to address formulations containing embedded dynamical systems. We highlight a series of approaches for constructing the requisite convex and concave relaxations of differential equations in the original decision space and discuss the use of such techniques in a global optimization context. These methods may readily be composed with existing McCormick relaxations approaches which allows for the solution of general nonlinear formulations to certified global optimality. Use cases relevant to hybrid data-driven process modeling, parameter estimation, and worst-case robust design are discussed.


### Probability Bounds Analysis in Julia (20min + 2min Q)

- Probability Bounds Analysis in Julia
    - Ander Gray ([@AnderGray](http://github.com/AnderGray)) (Univ Liverpool)
    - [Project link](https://github.com/AnderGray/ProbabilityBoundsAnalysis.jl)

- Probability bounds analysis in Julia, a package for performing arithmetic between uncertain numbers. ProbabilityBoundsAnalysis.jl computes guaranteed bounds on functions of random variables, given only partial information about their marginals and dependence. Considered to be a form of rigorous computing with random variables.


### Methods to Soundly Verify Deep Neural Networks (20min + 2min Q)

- Methods to Soundly Verify Deep Neural Networks
    - Tomer Arnon ([@tomerarnon](http://github.com/tomerarnon)), Stanford
    - [Project link](https://github.com/sisl/NeuralVerification.jl)

- Deep neural networks are widely used for nonlinear function approximation with applications ranging from computer vision to control. Although these networks involve the composition of simple arithmetic operations, it can be very challenging to verify whether a particular network satisfies certain input-output properties. NeuralVerification.jl implements several methods that have emerged recently for soundly verifying such properties. These methods borrow insights from reachability analysis, optimization, and search. We discuss fundamental differences and connections between existing algorithm and we provide pedagogical implementations of existing methods and compare them on a set of benchmark problems.


