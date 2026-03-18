# Inverse Kinematics

## Intro:

In computer animation and robotics, inverse kinematics (IK) is the mathematical process of calculating the variable joint parameters needed to place the end of a kinematic chain, such as a robot manipulator or an animation rig's hand or foot, in a given position and orientation (relative to the start of the chain). IK operations are computationally much more complex than forward kinematics, in which joint parameters are trigonometrically calculated to achieve the position and orientation of the chain's end.

## Kinemaic Analysis:

Kinematic analysis is one of the first steps in the design of most industrial robots. Kinematic analysis allows the designer to obtain information on the position of each component within the mechanical system. This information is necessary for subsequent dynamic analysis along with control paths.

Inverse kinematics is an example of the kinematic analysis of a constrained system of rigid bodies, or kinematic chain. The kinematic equations of a robot can be used to define the loop equations of a complex articulated system. These loop equations are nonlinear constraints on the configuration parameters of the system. The independent parameters in these equations are known as the degrees of freedom of the system.

While analytical solutions to the inverse kinematics problem exist for a wide range of kinematic chains, computer modeling and animation tools often use Newton's method to solve the nonlinear kinematics equations.[2] When trying to find an analytical solution it is often convenient to exploit the geometry of the system and decompose it using subproblems with known solutions.[8][9]

Other applications of inverse kinematic algorithms include interactive manipulation, animation control and collision avoidance.

## Analytical solution of IK:

In some, but not all cases, there exist analytical solutions to inverse kinematic problems. One such example is for a robot with 6 degrees of freedom (DOF) (for example, 6 revolute joints) moving in 3D space (with 3-position DOF, and 3 rotational DOF). If the DOF of the robot equals or exceeds that of the end effector, for example with a 7-DoF robot with 7 revolute joints, then there exist infinitely many solutions to the IK problem and an analytical solution does not exist. Further extending this example, it is possible to fix one joint and analytically solve for the other joints, but a better solution is perhaps offered by numerical methods, which can instead optimize a solution given additional preferences (costs in an optimization problem).[citation needed]

An analytic solution to an inverse kinematics problem is a closed-form expression that takes the end-effector pose as input and gives joint positions as output, 
q
=
f
(
x
)
{\displaystyle q=f(x)}. Analytical inverse kinematics solvers can be significantly faster than numerical solvers and provide more than one solution, but only a finite number of solutions, for a given end-effector pose.

Many different programs (Such as FOSS programs IKFast and Inverse Kinematics Library) are able to solve these problems quickly and efficiently using different algorithms such as the FABRIK solver. One issue with these solvers, is that they are known to not necessarily give locally smooth solutions between two adjacent configurations, which can cause instability if iterative solutions to inverse kinematics are required, such as if the IK is solved inside a high-rate control loop.

