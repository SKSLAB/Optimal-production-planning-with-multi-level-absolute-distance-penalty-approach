# Optimal production planning with multi-level (absolute distance penalty approach) 
##### An optimization test suite involving 108 continuous variables

This submission can be used to evaluate the performance of optimization techniques on problems with continuous variables. This optimization problem arises for maximization of profit in production planning. However these files can be used as black-box optimization problems.

There are eight minimization optimization problems in this suite (case1.p, case2.p, case3.p, case4.p, case5.p, case6.p, case7.p and cas8.p). All the cases (Case 1 to Case 8) have a problem dimension of 108 continuous variables.

Each of them has the following format
```
[ F ] = case1(X);
```
Input: population (or solution, denoted by X) and its <br>
Output: objective function (F) values of the population members.

The file ProblemDetails.p can be used to determine the lower and upper bounds along with the function handle for each of the cases.

The format is `[lb, ub, fobj] = ProblemDetails(n);`

Input: n is an integer from 1 to 8. <br>
Output: (i) the lower bound (lb), <br>
(ii) the upper bound (ub), and <br>
(iii) function handle (fobj).

The file Script.m shows how to use these files along with an optimization algorithm (SanitizedTLBO).


**Note:**<br>
  1. The absolute distance penalty comes in while handling domain hole constraint, which is the minimum between absolute of X<sub>j</sub> and (X<sub>j</sub>-l<sub>j</sub>). Here X<sub>j</sub> refers to the jth dimension of solution and l<sub>j</sub> refers to minimum non-zero production level.

  2. Case 1 - 4 have the same problem structure but employ different data; Case 5 - 8 has same set of data as compared to Case 1 - 4, but do not employ a certain feature (flexible) of the problem.

  3. The objective function files are capable of determining the objective function values of multiple solutions (i.e., if required, the entire population can be sent to the objective function file).


**Reference:** Chauhan, S., S., and P. Kotecha (2019), Performance Evaluation of Grey Wolf Optimizer and Symbiotic Organisms Search for Multi-level Production Planning with Adaptive Penalty, Springer, DOI 10.1007/978-981-10-8968-8