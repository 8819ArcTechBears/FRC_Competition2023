# Everybot 2023


Path Planning	"is the process of creating and following trajectories. These paths use WPLib trajectory APIs for generaton and Ramsete Controller for following.

Using PathWeaver

WPLib support for generating parameterized spline trajectories and following those trajectories with typical FRC robot drives"									
Trajectory Generation 	A trajectory is a smooth curve, with velocties and accelerations at each point along the curve, connecting two endpoints on the field. 									
	"simple autonomos routine involves moving forward, stopping, turning 90 degress to the right, then moving forward.

using trajectories allows for motion along a smooth curve.
advantage for speding up autonomous routines, creating more time for other tasks.
Tools for robot
opticals flow sensors gy-521.                   "									
	Generation and following of trajectories is incredibly useful for performing autonomous tasks.									
	https://docs.wpilib.org/en/stable/docs/software/advanced-controls/trajectories/trajectory-generation.html									
Manipulating Trajectories										
	https://docs.wpilib.org/en/stable/docs/software/advanced-controls/trajectories/manipulating-trajectories.html									
										
Robot Program code resources										
	https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-4/creating-benchtop-test-program-cpp-java.html									
PathWeaver Introduction 										
	https://docs.wpilib.org/en/stable/docs/software/pathplanning/pathweaver/creating-pathweaver-project.html									
										
ARM Robot Functions										
review the code for arm robot we currently have 										
any adjustments modifications we would add based on scoring points										
										
Build the subsytem		Subsystems are the parts of your robot that are independently controlled 								
		 collectors, shooters, drive bases, elevators, arms, wrists, grippers.								
		Each subsystem is coded as an instance of the Subsystem class. 								
		Subsystems should have methods that define the operation of the actuators and sensors but not more complex behavior that happens over time.								
										
		https://docs.wpilib.org/en/2020/docs/software/old-commandbased/subsystems/simple-subsystems.html#:~:text=Subsystems%20are%20the%20parts%20of,instance%20of%20the%20Subsystem%20class.								
										
										
