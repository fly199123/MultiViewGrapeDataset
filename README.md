# MultiViewGrapeDataset
The target of the grape harvesting view planning task is to adjust the continuous camera viewpoints to ultimately help the robot locate the grape stem. 
This is a multi-view grape dataset designed for training a deep reinforcement learning policy network for this task.The dataset contains a total of 6 
groups of data. Each group includes RGB images, depth images captured from 147 sampled viewpoints, and a CSV file. 

![项目Logo](image/Fig1.png)

As shown in Figure 1, during data collection, the camera viewpoints are constrained to lie on a spherical surface centered at the grape cluster centroid 
$GC$ with a radius $R$. The camera position is represented as $p = [R, θ, φ]$. The center point of each region $R_{i}$ on the sphere is selected as a sampling 
point, and the robotic arm is controlled to move the camera to these points for data acquisition. The policy network outputs actions $A=\\{ +\Delta\theta, -\Delta\theta, +\Delta\phi, +\Delta\phi \\}$. 
By setting the size of each region $R_{i}$, the policy network ensures that each action results in the camera moving to an adjacent grid region.
The CSV file contains the following information:

