# Continuous Risk Exposure in UAV Path Planning

Trajectory timing changes how long a quadrotor spends in risk zones along its path. These notes explain how time parameterization affects total risk exposure and the longest continuous exposure in risk-aware motion planning.

## Total and consecutive exposure in risk zones

Total exposure is the sum of the time a UAV spends inside risk zones. Longest consecutive exposure is the duration of its longest uninterrupted visit. A new visit starts when the vehicle re-enters a risk zone after spending time outside all risk zones.

One 4-second visit and two 2-second visits separated by time outside the zones both give 4 seconds of total exposure. Their longest consecutive exposures are 4 seconds and 2 seconds, respectively. On a fixed geometric path, a different speed profile can change both metrics by changing how long the UAV spends in each zone.

[Read the full note](https://17622336232.github.io/quadrotor-path-timing-notes/).

## Path geometry and timing

A geometric path specifies where the quadrotor can fly. A time law specifies how quickly it progresses along the path. A collision-free route through a narrow opening can still demand excessive acceleration if it is flown too quickly.

On a fixed path, allowable speed depends on the path shape and the vehicle limits. Time parameterization assigns progress along that path. A joint optimizer can also change path shape and segment duration while enforcing clearance and dynamic constraints.

## Comparing planning methods

Report feasibility, clearance, travel time, and planning time on the same test cases. Per-segment speed and acceleration help explain behavior near constrained regions. Document the environment geometry, collision model, vehicle limits, and success criterion.

## References

- [H. Pham and Q.-C. Pham, A New Approach to Time-Optimal Path Parameterization based on Reachability Analysis](https://arxiv.org/abs/1707.07239)
- [Z. Wang, X. Zhou, C. Xu and F. Gao, Geometrically Constrained Trajectory Optimization for Multicopters](https://arxiv.org/abs/2103.00190)
- [R. Salzman et al., Efficient Motion Planning for Problems Lacking Optimal Substructure](https://ojs.aaai.org/index.php/ICAPS/article/view/13855)
