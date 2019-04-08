# The FLASH Van 
The team name stands for **F**u**l**ly **A**utonomous but **S**tuff **H**appens and we are from **Van**derbilt.
Team members are:
* Feiyang Cai
* Tim Darrah
* Nathaniel (Nate) Hamilton
* Diego Manzanas Lopez
* Patrick Musau         (Project Leader)
* Shreyas Ramakrishna
* Ayana Wild

# Vehicle Configuration
Our car is modeled after the V2 using a Hokuyo UST-10LX lidar and ZED Camera for sensing and localization, with a NVIDIA TX2 for processing.

# Repository Organization
**COME UP WITH THIS INFO**

# How to Build the Code
The particle filter used for localization depends on [RangeLibc](https://github.com/kctess5/range_libc). Run the following to install the python wrappers for range_libc:

```cd range_libc/pywrappers```

##### on VM

```./compile.sh```

##### on car - compiles GPU ray casting methods

```./compile_with_cuda.sh ```

# Simulation Files (work in progress, will add more details later)

#### Run Simulation:
```roslaunch race f1tenth.launch```
#### Run particle filter:
```roslaunch particle_filter localize.launch```

#### Run pure pursuit
```roslaunch a_stars_pure_pursuit pure_pursuit_sim.launch  ```

#### Hallway simulation using teb planner, amcl, map built from gmapping:

```roslaunch wall_following move_base.launch```
