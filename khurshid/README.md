![BeyondAI Banner for Research Projects](../BeyondAI_Banner_Research_Projects_2024.png)

# Comparative Analysis of ODE Solvers: Accuracy and Performance Evaluation

Provide a description of your project including 

# 1. Motivation
Solving Ordinary Differential Equations (ODEs) is crucial for modeling dynamic systems in fields like physics, biology, and machine learning. This research evaluates and compares the accuracy of three NODE integrators: RK4, Euler’s method, and an adaptive step-size solver Dormand-Prince 5 utilizing PyTorch’s torchdiffeq. By testing these solvers, we analyze their strengths, limitations, and suitability for tasks requiring precision and efficiency, providing insights for applications like Neural ODEs.

# 2. Research question
How do different ODE solvers influence the accuracy and computational performance of Neural Ordinary Differential Equations (NODEs)?

# 3.  Method and implementation
This research analyzed various ODE solvers within Neural Ordinary Differential Equations (NODEs): Euler’s method, RK4, and the adaptive step-size solver ODEINT from ‘torchdiffeq’. RK4 and ODEINT were compared in terms of computational time and training loss over 400 epochs.
The adjoint sensitivity method was used for memory-efficient backpropagation. The study highlights trade-offs between fixed-step solvers (e.g., RK4) and adaptive solvers (ODEINT - Dopri 5) in optimizing NODE performance.

# 4. Briefly mention and discuss your results
Two Neural ODE fixed time step numerical solvers: Euler’s method RK4 method were implemented, and compared against each other in terms of error. Because Euler’s integrator is the simplest way to solve NODEs, I decided to compare one of the famous fixed step size ODE solver - RK4 against proposed custom made ODE solver(Dopri5) from the original paper and torchdiffeq library created by author. I utilized spirial dataset of 2000 points and trained them using 4 hundred iterations.

# 5. Draw your conclusions
The objective of this research was to identify the most accurate and efficient Neural ODE (NODE) integrator. By comparing the loss and processing time, it was observed that the adaptive step-size solver Dopri5 demonstrated superior accuracy, with a lower loss compared to the RK4 integrator. However, achieving comparable accuracy with RK4 required reducing the time steps, which significantly increased the computational time. Consequently, Dopri5 proved to be more effective, balancing both accuracy and computational efficiency, making it a preferable choice over RK4 in this context.

> The research poster for this project can be found in the [BeyondAI Proceedings 2024](https://thinkingbeyond.education/beyondai_proceedings_2024/).
