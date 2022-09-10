# SDCND : Scan Matching Localization
This project is for the third course in the  [Udacity Self-Driving Car Engineer Nanodegree Program](https://www.udacity.com/course/c-plus-plus-nanodegree--nd213) : Localization. 

Steps taken to complete the project are as follows:
- Step 1) Filter scan using voxel filter;
- Step 2) Find pose transform by using ICP or NDT matching;
- Step 3) Transform the scan so it aligns with ego's actual pose and render that scan.

Project requirements are as follows:
 1) drive the vehicle at least 170 meters without the pose error rising above 1.2 meters, at an at least medium speed (three up arrow taps in the workspace); 
 2) the transformed point cloud should be appropriately rendered.
 
All codes are implemened in `c3-main.cpp`. The code is written in a way that user can select which algorithm (ICP or NDT) to run for localization. Multiple parameters (e.g., iteration, transformation epsilon, resolution, etc.) were tried to achieve the above requirements. 

### ICP Algorithm

To run ICP algorithm, we enter the code below after running `carla simulator`: 
```
./cloud_loc ICP
```

Parameters used for ICP algorithm are as follows:
- iteration= 60
- transformation epsilon = 0.001

Obatined results are shown below for 3 instances:

![ICP_1](https://user-images.githubusercontent.com/109758200/189467053-cf1642fc-8601-452f-95c0-2877f2e7e5d2.PNG)
![ICP_3](https://user-images.githubusercontent.com/109758200/189467057-ce0de459-217b-4f76-aba6-9581afe38b6a.PNG)
![ICP_final](https://user-images.githubusercontent.com/109758200/189467060-87dae090-af3c-4a4a-a44e-de1ac08799e5.PNG)


### NDT Algorithm

To run NDT algorithm, we enter the code below after running `carla simulator`: 
```
./cloud_loc NDT
```

Parameters used for NDT algorithm are as follows:
- iteration= 100
- transformation epsilon = 0.001
- grid resolution= 5

Obtained results are shown below for 3 instances:
![NDT_1](https://user-images.githubusercontent.com/109758200/189467044-7ddbb881-73e1-45a0-ab34-fdc073484764.PNG)
![NDT_3](https://user-images.githubusercontent.com/109758200/189467047-57586846-3a5a-4591-a486-6711a46d40cb.PNG)
![NDT_Final](https://user-images.githubusercontent.com/109758200/189467049-2b4fc184-ed69-4da4-ab58-33cfe79c5e74.PNG)
