# Motion Planning and Decision Making for Autonomous Vehicles

In this project, you will implement two of the main components of a traditional hierarchical planner: The Behavior Planner and the Motion Planner. 

Both will work in unison to be able to:
* Avoid static objects (cars, bicycles and trucks) parked on the side of the road (but still invading the lane). The vehicle must avoid crashing with these vehicles by executing either a “nudge” or a “lane change” maneuver.
* Handle any type of intersection (3-way,  4-way intersections and roundabouts) by STOPPING in all of them (by default)
* Track the centerline on the traveling lane.

To accomplish this, you will implement:

* Behavioral planning logic using Finite State Machines - FSM
* Static objects Collision checking.
* Path and Trajectory generation using Cubic Spirals
* Best trajectory selection though a cost function evaluation. This cost function will mainly perform a collision check and a proximity check to bring cost higher as we get closer or collide with objects but maintaining a bias to stay closer to the lane center line.


This project is finished in workspace VM.

## Preparation
```
cd /home/workspace/
git clone https://github.com/udacity/nd013-c5-planning-starter.git
```
Followed the [rebric](https://review.udacity.com/#!/rubrics/2949/view) to modify the codes.

## Usage

GPU must be enabled and we have to use remote desktop for visualization.

To run the Carla simulator by using following commands:

```
su - student # Ignore outout for permission Denied
cd /opt/carla-simulator/
SDL_VIDEODRIVER=offscreen ./CarlaUE4.sh -opengl
```



Start another terminal if we use terminator, press Ctrl + Shift + e
```
./install-ubuntu.sh
cd starter_files/
cmake .
make
cd nd013-c5-planning-starter/project
./run_main.sh
```