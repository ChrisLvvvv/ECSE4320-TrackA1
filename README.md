> **Maintenance moved (2026-11-05).**
> The maintained course project is now in [ECSE4320-TrackA1](https://github.com/ChrisLvvvv/ECSE4320-Projects/tree/main/ECSE4320-TrackA1).
> Its original project files, ignore rules, and executable modes were verified in collection commit `f460a7d912533c1d14719fa32afeac71684c10be`.
> This repository retains its original Git history and the original README below.

---

This project explored several advanced OS and CPU mechanisms through the design of targeted micro-benchmarks, rather than relying on predefined tools or canned workloads. Each feature was selected to expose a different layer of the hardware–software interface, including scheduling decisions, thread placement, memory locality, and shared-core resource contention. All experiments were conducted with controlled execution parameters, explicit CPU and memory bindings where applicable, and repeated measurements to capture variability.

Across the four features, the results consistently demonstrate that performance behavior is highly dependent on workload characteristics and execution context. CPU affinity primarily improved execution stability rather than raw throughput, while scheduler oversubscription revealed clear limits to scalable parallelism once thread counts exceeded available cores. The NUMA experiment highlighted how performance tuning policies can become ineffective or even counterproductive in virtualized environments, emphasizing the importance of understanding the underlying hardware topology. Finally, the SMT interference study showed that shared-core execution can be either benign or severely detrimental depending on whether workloads contend for compute or memory resources.

Together, these experiments satisfy the project’s learning objectives by combining meaningful technical depth with reproducible experimental methodology and principled analysis. The findings reinforce core OS and architecture concepts such as cache locality, context-switch overhead, scheduler fairness, and shared resource contention. All code, scripts, and results are organized for clarity and reproducibility, enabling the experiments to be rerun and extended on other systems.