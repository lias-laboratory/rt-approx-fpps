# An FTPAS for Response Time Analysis of Fixed Priority Real-Time Tasks with Resource Agmentation

The project page provides all MATLAB source codes of the algorithms and simulation environments defined in the paper _"An FTPAS for Response Time Analysis of Fixed Priority Real-Time Tasks with Resource Augmentation"_, Thi Huyen Chau Nguyen, Pascal Richard, Emmanuel Grolleau,  +IEEE Transactions on Computers+, 2014, accepted for publication.<http://dx.doi.org/10.1109/TC.2014.2346178>

The paper presents a best possible Fully Polynomial Time Approximation Scheme under resource augmentation for computing worst-case response time upper bounds of fixed-priority tasks with arbitrary deadlines to be executed upon a uniprocessor platform. 

## Download

Download both files (Approx.zip and Graphs_of_all_Experiments.zip) at https://github.com/lias-laboratory/RT-Approx-FPPS/releases

## Installation instructions

All MATLAB code files must be extracted in the same folder for execution.

## File descriptions

* Approx.zip - MATLAB source codes by categories: 
> * FTPAS   - MATLAB codes of the Fully Polynimial Time Approximation Scheme
> > * Approx.m - main function of FTPAS algorithm (Algorithm 3 in the paper)
> > * ApproxFirstStage.m - FirstStage algorithm (Algorithm 1 in the paper)
> > * ApproxSecondStage.m - SecondStage algorithm (Algorithm 2 in the paper)
> > * ApproxSchedPoints.m - list of scheduling points considered in the first stage (Equation 13 in the paper)
> > * Approx_wil.m - cumulative approximate workload (Equation 8 in the paper)
> > * jobindex.m - Index of the most recently released job of tau_i (Equation 16 in the paper)
> > * intersection.m - intersection of approximate workload and processor capacity (see Fig. 2 in the paper)
> * Exact Response Time Analysis - MATLAB codes (Lehoczky's algorithm)
> > * ResponseTime.m - main function of exact RTA
> > * JobResponseTime.m - worst-case response time of Job l of Task i in the level-i busy period
> * Linear Response Time Upper Bound (LRTUB) - MATLAB codes (Bini, Nguyen, Richard, Baruah Algorithm, 2009)
> > * UpperBoundBB.m - function computing LRTUB (Equation 6 in the paper)
> * Taskset Generator - MATLAB codes for generating tasksets for experiments
> > * GenTasks.m - main function for generating taskset under various parameters (see Section 6.1 in the paper)
> > * UUniFast.m - Bini's UUniFast function for generating unbiased utilization factors
> > * rm.m - Sort task according to Rate Monotonic scheduling algorithm (implicit deadline tasks)
> > * dm.m - Sort task according to Rate Monotonic scheduling algorithm (constrained-deadline tasks)
> > * Audsley.m - - Sort task according to Audsley's scheduling algorithm (arbitrary deadline tasks)
> * Experiment 1 - MATLAB codes for monitoring the average accuracy parameter of the FPTAS for beating LRTUB (graph generator in Section 6.2 in the paper)
> > * PlotMinK.m - main file for generating graphs under various parameter of controls 
> > * ComputeMinK.m - Compute minimum FPTAS accuracy parameter to beat LRTUB 
> * Experiment 2 - MATLAB codes for monitoring the average speedup factor of FTPAS and LRTUB (graph generator in Section 6.3 in the paper)
> > * PlotSdf.m - main file for generating graphs under various parameter of controls
> > * ComputeSdf.m - replication of experiments that call the following to functions
> > * SlowdownFactor.m - resource augmentation for FTPAS to achieve performance of exact RTA
> > * SlowdownFactor_bb.m - resource augmentation for LRTUB to achieve performance of exact RTA
> * Experiment 3 - MATLAB codes for monitoring the average acceptance ratio of FTPAS, LRTUB, Liu and Layland's utilization bound against exact RTA (graph generator in Section 6.4 in the paper).
> > * PlotAccept.m - main file for generating graphs under various parameter of controls 
> > * ComputeAccept.m - Compute average schedulable tasksets according to  FPTAS and LRTUB 
> * Experiment 4 - MATLAB codes for monitoring the average error (UB - Exact)/Exact for the FPTAS and LRTUB (graph generator in Section 6.5 in the paper)
> > * PlotError.m - main file for generating graphs under various parameter of controls 
> > * ComputeError.m - Compute the average error for the FPTAS against Exact RTA
> > * ComputeErrorBB.m - Compute the average error for the LRTUB against Exact RTA

* Graphs.zip - MATLAB figure files (.fig) generated during the experiments (only some of them are presented in the paper). These files can be directly opened using MATLAB. 

## Historic Contributors

* [Pascal RICHARD](https://www.lias-lab.fr/fr/members/pascalrichard/)

## Code Analysis

* Programming Languages: MATLAB