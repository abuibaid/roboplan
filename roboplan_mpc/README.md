# roboplan-mpc

Joint-space model predictive control (MPC) for RoboPlan.

Tracks a desired joint state within the joint position, velocity, acceleration, and torque limits
of the scene. The joint accelerations are the inputs of a double integrator, and the torques follow
from the robot dynamics (Pinocchio RNEA). The optimal control problem is formulated with multiple
shooting in CasADi and solved with IPOPT. Each call returns the predicted joint trajectory over the
horizon, which can be sent to a joint trajectory controller.
