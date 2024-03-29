# NPB3.0-JAV-FORK

This is a fork of the original [NASA NAS Parallel Benchmarks](https://www.nas.nasa.gov/publications/npb.html).

Please read the following file: NPB3.0-JAV/README.md

I do not plan to make updates on this code, nor the build. Just used it for some of my tutorials.

# Author

* José Vicente Núñez Zuleta

# Original README

## The non-MPI Version of NAS Parallel Benchmarks (SER, OMP, HPF, JAV)
=======================================================================

The non-MPI version of NAS Parallel Benchmarks was based on a version
that was previously released as PBN, or "Programming Baseline for NPB".
This version consists of four sets of source codes based on the NAS 
Parallel Benchmark version 2.3:

	NPB3.0-SER - An improved sequential implementation
	NPB3.0-OMP - An OpenMP implementation based on NPB-SER
	NPB3.0-HPF - An HPF implementation based on NPB-SER
	NPB3.0-JAV - A Java implementation with Java threads

For more details on each implementation, please refer to the README file
in each sub-directory.

The rationale behind this release is as follows:

1. To provide the community with an optimized version of NPB2.3-serial

In our effort to compare compilers and tools using NPB2.3-serial as a baseline,
we encountered implementation efficiencies and code organization that greatly
limits their parallelization based on the insertion of "directives". While the 
presence of these "imperfections" reflect the ability of "average" programmers,
fixing some of these greatly reduced the noise in the results and helped our 
evaluation. For example, BT and SP were reorganized so that memory requirements
for Class A on one SGI Origin2000 (O2K) node are reduced by 9 times and 2 times 
respectively. Execution speed almost doubled in each case. An unnecessary code 
segment, only required in the MPI parallel implementation, was also removed to 
(almost) double IS's performance on one O2K node. We note further that an LU 
implementation (with loop organization favoring parallelization based on a
"hyperplane" or "wavefront") that favors data-parallelism is also included for 
the benefit of HPF. These, together with other minor fixes, have been 
introduced to NPB2.3-serial to produce the NPB3.0-SER

2. To provide standard implementations based on OpenMP and HPF directives
   and Java threads

The OpenMP and HPF directives inserted reflect a programmer's 
parallelization and data-distribution strategy, while the compiler is 
responsible for implementation and optimization. The Java implementation
serves to examine Java as a new language for CFD computation.


NPB3.0 was implemented by Henry Jin <hjin@nas.nasa.gov>, Michael Frumkin 
<frumkin@nas.nasa.gov> and Matthew Schultz.
We want to acknowledge support and comments, particularly from the original
NPB implementation team of the NAS Division at NASA Ames Research Center.  
Additionally, we want to thank Thomas Gruen <gruen@cs.uni-sb.de> and Allan 
Snavely <allans@SDSC.EDU> who pointed out the problem with IS.

For all errors/feedbacks related to NPB3.0, please contact:

      NAS Parallel Benchmarks Team
      npb@nas.nasa.gov


