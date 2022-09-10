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

1. **ICP Algorithm**


2. **NDT Algorithm**
