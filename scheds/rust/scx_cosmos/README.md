# scx_cosmos

This is a single user-defined scheduler used within [sched_ext](https://github.com/sched-ext/scx/tree/main), which is a Linux kernel feature which enables implementing kernel thread schedulers in BPF and dynamically loading them. [Read more about sched_ext](https://github.com/sched-ext/scx/tree/main).

## Overview

Lightweight scheduler designed for optimal CPU placement.

The scheduler tries to keep tasks running on the same CPU as much as
possible when the system is not saturated.

At system saturation the scheduler switches to a deadline-based policy and
a shared DSQ, so that tasks are more likely migrating across the available
CPUs and interactive tasks get a better chance to run.

## Typical Use Case

General-purpose scheduler: the scheduler should adapt itself both for
server workload or desktop workload.

## Production Ready?

No.
