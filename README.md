# Adaptive Task Scheduler (Rust + Tokio), duplicate copy

> **This repository is a duplicate.** The maintained version of these design notes is **[Mattbusel/adaptive-task-scheduler](https://github.com/Mattbusel/adaptive-task-scheduler)** (same name, without the trailing dot). Please read, star or open issues there.

## Summary

A design for a Tokio-based runtime that notices when an async task is holding up the tasks that depend on it, and promotes that task onto a dedicated thread (`tokio::task::spawn_blocking`) so the chain unblocks. The idea borrows from priority inheritance in real-time operating systems and from work-stealing schedulers.

**Status: design notes only.** Like the main repository, this one contains no Rust code (no `Cargo.toml`, no `src/`), so there is nothing to build or run. See the main repository for the full design, the intended architecture and the open design questions.
