# kSTEP: Characterization and Deterministic Testing of Linux CPU Scheduler Bugs

## About the Project

I worked on implementing and exploring **kSTEP**, a framework for characterizing and testing bugs in the Linux CPU scheduler.

The project is based on the research paper *kSTEP: Characterization and Deterministic Testing of Linux CPU Scheduler Bugs*, which focuses on making scheduler behavior reproducible and analyzing bugs that are difficult to identify through conventional testing.

My work involved setting up the project, understanding its experimental workflow, working with scheduler bug test cases, organizing experiment outputs, and studying the results produced by the experiments.

The project covers **17 Linux CPU scheduler bug experiments**.

## Research Paper

**Paper:** [kSTEP: Characterization and Deterministic Testing of Linux CPU Scheduler Bugs](https://www.usenix.org/conference/osdi26/presentation/cao)

**Conference:** 20th USENIX Symposium on Operating Systems Design and Implementation (OSDI '26)

**Research Repository:** [kstep-dev/kstep](https://github.com/kstep-dev/kstep)

**Research Paper PDF:** [osdi26-cao.pdf](osdi26-cao.pdf)

## What I Worked On

- Set up the kSTEP project and explored its architecture and execution workflow.
- Studied how Linux CPU scheduler bugs can be reproduced through controlled experiments.
- Worked with individual scheduler bug test cases.
- Organized experiment configurations and result files.
- Executed and analyzed scheduler experiments.
- Examined the generated traces and outputs to understand scheduler behavior.
- Maintained separate experiment commits to keep the project history organized.

## Experiments

I worked with the following 17 scheduler bug experiments:

| No. | Experiment |
|---:|---|
| 1 | `sync_wakeup` |
| 2 | `vruntime_overflow` |
| 3 | `freeze` |
| 4 | `extra_balance` |
| 5 | `util_avg` |
| 6 | `long_balance` |
| 7 | `lag_vruntime` |
| 8 | `rt_runtime_toggle` |
| 9 | `uclamp_inversion` |
| 10 | `h_nr_runnable` |
| 11 | `even_idle_cpu` |
| 12 | `local_group_imbalance` |
| 13 | `util_avg_jump` |
| 14 | `slice_update` |
| 15 | `avg_vruntime_ceil` |
| 16 | `min_deadline` |
| 17 | `zero_vruntime` |

Each experiment focuses on a particular scheduler behavior or bug scenario. Together, they provide a way to examine different aspects of Linux CPU scheduling.

## Results

The experiment outputs are organized under:

```text
kstep/
└── results/
    ├── repro_sync_wakeup/
    ├── repro_vruntime_overflow/
    ├── repro_freeze/
    ├── repro_extra_balance/
    ├── ...
    └── repro_zero_vruntime/
```

The results contain experiment-specific output files and traces that can be used to examine scheduler behavior.

I used these outputs to study the behavior of the individual test cases and understand how the scheduler responds to different conditions.

## Understanding kSTEP

The central idea behind kSTEP is to make Linux CPU scheduler testing more deterministic.

Scheduler behavior can depend on timing, CPU placement, and event ordering. This makes certain bugs difficult to reproduce consistently.

kSTEP addresses this challenge by controlling scheduler-related events and enabling repeatable testing. This makes it easier to investigate scheduler behavior and analyze bug scenarios.

## Technologies and Concepts

- Linux Kernel
- C
- Linux CPU Scheduler
- Kernel-level testing
- Deterministic execution
- Scheduler debugging and characterization
- Experiment analysis

## Repository Structure

```text
.
├── osdi26-cao.pdf
├── README.md
└── kstep/
    ├── ...
    └── results/
        ├── repro_sync_wakeup/
        ├── repro_vruntime_overflow/
        └── ...
```

## References

1. **Research Paper:** [USENIX OSDI '26 – kSTEP](https://www.usenix.org/conference/osdi26/presentation/cao)
2. **kSTEP Research Repository:** [GitHub – kstep-dev/kstep](https://github.com/kstep-dev/kstep)
3. **My Implementation:** [OS Project – kSTEP](https://github.com/Rishi000000/OS_Project---kSTEP-Characterization-and-Deterministic-Testing-of-Linux-CPU-Scheduler-Bugs)

---

**Project Focus:** Understanding, implementing, and evaluating deterministic experiments for Linux CPU scheduler bug characterization.