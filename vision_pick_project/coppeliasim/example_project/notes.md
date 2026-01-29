# Project Notes

Informal notes documenting experiments, decisions and observations and open questions.

## Model Simple Manipulator Model 

> Notes and observations while experimenting with a CoppeliaSim example manipulator model.
> Goal: understand how motion planning and IK planning are blended for efficient manipulation.

---

### 📌 Model Information

- **Simulator**: CoppeliaSim
- **Model**: Simple Manipulator (`.ttt`)
- **Source**: CoppeliaSim example models
- **Credits**: Original model and setup by CoppeliaSim

---

### 🎯 Objective

- Learn how:
  - Inverse Kinematics (IK)
  - Motion planning
- are combined and coordinated in a manipulation task
- Understand why certain target poses become unreachable after modifying the setup

---

### 📅 Experiment Log

- Orignal model imported from coppeliasim was tested and validated. 
- Following modifications were made:
    - Robot base was moved from its initial position to a place close to robot. 
    - Target dummies were randomly moved around the station. 
- The model was tested with the modifications and it was observed the robot couldn't reach the pickup after placing the first object. 
- **Quick Fix:** After every placement robot reaches initconfig.
- This fixed the issue. But this increases cycle time. 
- The code was analyzed and following observations were made:
    - IK Solver solves for the config and this is isolated from the motion planner.  
    - By combining IKSolver and MotionPlanner, this issue could be fixed. 

