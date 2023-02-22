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
										
Tasks 

Initialization
 Start the program, robot sensors and actuators should be initialized. Initial set of positions of motors and sensors. Configure any communication with external devices. 


Autonomous Mode
The robot begins competition in autonomous mode ? this is best to perform set of task without any input from the driver , this code contains the instructions for the robot to complete the task in 


Intake
Wheels : 
2 omni wheels 
	-Omni Wheels code :  Use these wheels to make your robot turn smoothly or build a holonomic drivetrain.

Wheels :
 4 Hygrips wheels  .
Be able to suck up game pieces, both cubes & cones.
Some sort of motion sensor -> Be able to detect/stop when game piece is grabbed 
As well as being able to turn 360 → in order to grab game pieces from ground, charge station, and not have to turn without having to turn the whole drive base. 
Another sensor to help us determine distance from robot to cone  → in order to know if we are within reach to score (be more precise with our scoring)
 
Teleoperated Mode : after autonomous mode has been changed driver takes over and controls the robot manually . This code has drivers inputs, controlling movement of the robot and any manipulators 

Endgame : “End game period “ , Robot Sensors !! 
-Robot can earn extra points by completing additional task 
Sensor Feedback and Error Handling
Sensors need to provide the state of the robot and the environment 
Code must include instructions for handling any errors that occur during the competition 






Accelerometer  Code Anology  thanks to a collab with another programming team in West Lake HighSchool 

Yaw Pitch Roll analogy for getting the angle for your robot (stability) 
Yaw (orientation)
pitch(turning) xy in 3d space 

Create yawl , pitch roll , 

double  xy()
Double get yz 

Angle xy = (a number/ math.pi) 

Math lib 


Pathagorem theorem angle 

Tangent of that value 
Double angle xy math.atan2(ACCEx , ACCCEy) 

//convert your value into degrees angles 
Double angle xy*(180/MATH.PI) 

—------------------------------------------
ACCELOMATER JAVACODE 

//PITCH XY


//ROLL YZ 













Sensors for Programming 

Pixy2 Smart Vision Sensor Camera am-3477a

Ultrasonic Proximity Sensor, EZ, mb1013,MaxBotix
Sensor code must be able to detect 

Camera 1: Microsoft Life cam HD-300 
Camera Code : Must be able to Scan QR Code in the competition 

Camera 2: Rear view camera HD 1080p Logi
Code for rear view 


Software Guide  from Every Bot 

To start testing the robot do the following Steps 
Configure Spark MaXes 
https://docs.revrobotics.com/rev-hardware-client/getting-started/installation-instructions




























Subsystems for Programming Team 


This must be separate java classes  each in its own file, 

Import them into your main robot class 

Example template 


Create subsystem for the robot system 
Ex: template analogy 

public class RobotSubsystem {
    private final WPI_TalonSRX intakeMotor;
    private final WPI_TalonSRX armMotor;
    private final WPI_TalonSRX climberMotor;
    private final SpeedControllerGroup leftDriveMotors;
    private final SpeedControllerGroup rightDriveMotors;
    private final DifferentialDrive drive;
    private final DigitalInput armLimitSwitch;
    private final XboxController controller;

    private static final double INTAKE_SPEED = 0.5;
    private static final double ARM_SPEED = 0.5;
    private static final double CLIMBER_SPEED = 0.5;

    public RobotSubsystem() {
        intakeMotor = new WPI_TalonSRX(1);
        armMotor = new WPI_TalonSRX(2);
        climberMotor = new WPI_TalonSRX(3);

        SpeedControllerGroup middleDriveMotors = new SpeedControllerGroup(new WPI_TalonSRX(4), new WPI_TalonSRX(5));
        SpeedControllerGroup centerDriveMotors = new SpeedControllerGroup(new WPI_TalonSRX(6));

        leftDriveMotors = new SpeedControllerGroup(middleDriveMotors, centerDriveMotors, new WPI_TalonSRX(7));
        rightDriveMotors = new SpeedControllerGroup(middleDriveMotors, centerDriveMotors, new WPI_TalonSRX(8));

        drive = new DifferentialDrive(leftDriveMotors, rightDriveMotors);

        armLimitSwitch = new DigitalInput(1);

        controller = new XboxController(0);
    }

    public void teleopPeriodic() {
        // Intake control
        if (controller.getBumper(Hand.kLeft)) {
            intakeMotor.set(INTAKE_SPEED);
        } else {
            intakeMotor.set(0.0);
        }

        // Arm control
        if (controller.getXButton()) {
            armMotor.set(ARM_SPEED);
        } else if (controller.getYButton() && !armLimitSwitch.get()) {
            armMotor.set(-ARM_SPEED);
        } else {
            armMotor.set(0.0);
        }

        // Climber control
        if (controller.getAButton()) {
            climberMotor.set(CLIMBER_SPEED);
        } else if (controller.getBButton()) {
            climberMotor.set(-CLIMBER_SPEED);
        } else {
            climberMotor.set(0.0);
        }

        // Drive control
        drive.arcadeDrive(controller.getY(Hand.kLeft), controller.getX(Hand.kRight));
    }
}




















public class RobotSubsystem {
    private final WPI_TalonSRX intakeMotor;
    private final WPI_TalonSRX armMotor;
    private final WPI_TalonSRX climberMotor;
    private final SpeedControllerGroup leftDriveMotors;
    private final SpeedControllerGroup rightDriveMotors;
    private final DifferentialDrive drive;
    private final DigitalInput armLimitSwitch;
    private final XboxController controller;

    private static final double INTAKE_SPEED = 0.5;
    private static final double ARM_SPEED = 0.5;
    private static final double CLIMBER_SPEED = 0.5;

    public RobotSubsystem() {
        intakeMotor = new WPI_TalonSRX(1);
        armMotor = new WPI_TalonSRX(2);
        climberMotor = new WPI_TalonSRX(3);

        leftDriveMotors = new SpeedControllerGroup(new WPI_TalonSRX(4), new WPI_TalonSRX(5), new WPI_TalonSRX(7));
        rightDriveMotors = new SpeedControllerGroup(new WPI_TalonSRX(6), new WPI_TalonSRX(5), new WPI_TalonSRX(8));

        drive = new DifferentialDrive(leftDriveMotors, rightDriveMotors);

        armLimitSwitch = new DigitalInput(1);

        controller = new XboxController(0);
    }

    public void teleopPeriodic() {
        // Intake control
        if (controller.getBumper(Hand.kLeft)) {
            intakeMotor.set(INTAKE_SPEED);
        } else {
            intakeMotor.set(0.0);
        }

        // Arm control
        if (controller.getXButton()) {
            armMotor.set(ARM_SPEED);
        } else if (controller.getYButton() && !armLimitSwitch.get()) {
            armMotor.set(-ARM_SPEED);
        } else {
            armMotor.set(0.0);
        }

        // Climber control
        if (controller.getAButton()) {
            climberMotor.set(CLIMBER_SPEED);
        } else if (controller.getBButton()) {
            climberMotor.set(-CLIMBER_SPEED);
        } else {
            climberMotor.set(0.0);
        }

        // Drive control
        double forwardSpeed = controller.getY(Hand.kLeft);
        double turnSpeed = controller.getX(Hand.kRight);
        drive.arcadeDrive(forwardSpeed, turnSpeed);
    }
}






