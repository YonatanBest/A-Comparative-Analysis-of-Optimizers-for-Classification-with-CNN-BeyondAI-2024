![BeyondAI Banner for Research Projects](../BeyondAI_Banner_Research_Projects_2024.png)

# Geometric Clifford Algebra Networks in Robotics

Conventional methods for modeling the dynamics of robots often depend on intricate kinematic and dynamic equations. Geometric Clifford Algebra Networks (GCANs) have the potential to provide a more intuitive and efficient approach due to their ability to capture geometric transformations and relationships. This research aims to outline the problem, focusing on the creation and assessment of GCAN models for predicting the motion and forces exerted by robotic arms across various scenarios. While we have some additional insights, the complexity and lack of research for this topic combined with the short timeframe was quite a challenge for us to tackle. Thus, for the research stage, we focused on:

1. Implementing a basic GCA-MLP in Python using clifford, cliffordlayers, etc. as per the structure described in the GCAN paper by Ruhe et al.
2. Testing the GCA-MLP's performance on simple datasets such as MNIST and Iris, as well as on the World Geometries Dataset and implementing it in robot dynamics
3. Comparing its performance to an MLP and a CNN, including accuracy, loss over epochs, and time for convergence.

Generally, the GCA-MLP showed decent accuracy during testing (85%-90%), and low loss by the last epoch (0.5 by the 50th epoch in the robot dynamics experiment). However, the GCA-MLP consumes a considerable amount of time to converge. As addressed in the GCAN paper, the problem of higher computational density can be addressed by using hardware accelerators like GPUs. In scenarios which require a faster time for convergence such as robotic motion, we suspect that the model will require some form of modification. The Geometric Algebra Transformers (GATr) paper by Brehmer et al. appears to be a promising route for future research on geometric algebra in robotics.

> The research poster for this project can be found in the [BeyondAI Proceedings 2024](https://thinkingbeyond.education/beyondai_proceedings_2024/).
