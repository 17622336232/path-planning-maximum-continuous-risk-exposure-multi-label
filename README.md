# Quadrotor Path Timing Notes

Technical notes on quadrotor path geometry, time parameterization, and joint optimization of trajectory shape and segment duration. [Read the full note](docs/index.html).

## Path geometry and timing

A geometric path specifies where the quadrotor can fly. A time law specifies how quickly it progresses along the path. A collision-free route through a narrow opening can still demand excessive acceleration if it is flown too quickly.

On a fixed path, allowable speed depends on the path shape and the vehicle limits. Time parameterization assigns progress along that path. A joint optimizer can also change path shape and segment duration while enforcing clearance and dynamic constraints.

## Comparing planning methods

Report feasibility, clearance, travel time, and planning time on the same test cases. Per-segment speed and acceleration help explain behavior near constrained regions. Document the environment geometry, collision model, vehicle limits, and success criterion.

## References

- [H. Pham and Q.-C. Pham, A New Approach to Time-Optimal Path Parameterization based on Reachability Analysis](https://arxiv.org/abs/1707.07239)
- [Z. Wang, X. Zhou, C. Xu and F. Gao, Geometrically Constrained Trajectory Optimization for Multicopters](https://arxiv.org/abs/2103.00190)
