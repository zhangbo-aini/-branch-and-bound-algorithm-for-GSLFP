# -branch-and-bound-algorithm-for-GSLFP
MATLAB codes for branch and bound algorithms for a class of generalized linear fraction sum problems
Warning:  When running this code, a version of MATLAB (2020b) or higher needs to be installed。
 
After unpacking the compressed package, the code package with the file name "Codes_for__GSLFP" is our general code, and its main program is "SOCPRBBRA_GLSFP.m" When solving a  generalized sum-of-linear-fractions programming (GSLFP) problem, the command "[Solution,Opt_val,Iter,CPU] = SOCPRBBRA_GLSFP(A, b,  c, d,e,f,r1,r2,rp,lenri,lenre)" needs to be called. The relevant explanations are as follows:

  Ax<=b
  A: Linear constraint matrix (m×n)
  b: m×1 Constant  vector on the right side of a linear constraints: Ax<=b
 c: In the objective function of problem GLSFP, a n×p matrix composed of real vectors on the numerators of all linear fractions.
  d: In the objective function of problem GLSFP, a p×1 vector composed of real numbers on the numerators of all linear fractions.
  e: In the objective function of problem GLSFP, a n×p matrix composed of real vectors on the denominators of all linear fractions.
  f: In the objective function of problem GLSFP, a p×1 vector composed of real numbers on the denominators of all linear fractions.
  r1: Without losing generality, for convenience,  let the exponents of the first lenri linear fraction functions be 1
  r2: Without losing generality, for convenience,  let the exponents of the last lenre linear fraction functions be 1
  rp: the exponent of the last fractional function  in the original p fractional functions (either 1 or 2) 
  lenri:represents the number of fractional functions with exponent 1 in the first p-1 fractional functions
  lenre:represents the number of fractional functions with exponent 2 in the first p-1 fractional functions 
  Solution: A global eps-optimal solution
  Opt_val: A global eps-optimal value
  Iter: The number of iterations of the algorithm at termination
  CPU: The total CPU time used by the algorithm at termination
  The code package with the file name "Codes_for_SLR" is an important subclass of the GSLFP problem (i.e., the sum of linear ratios (SLR) problem), and its main program is "SOCPRBBRA_SLR.m" When solving a general GSLFP problem, the command "[Solution,Opt_val,Iter,CPU] = SOCPRBBRA_SLR(A, b,  c, d,e,f,r1)" needs to be called.

In addition, for the codes in other files, they are numerical experimental settings from our upcoming SCI paper, which correspond to several tables in the paper. We mainly compared the algorithms in five existing papers to demonstrate the efficiency and practical applicability of our algorithm.
