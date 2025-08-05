#### 5. getting-started/preparing-and-submitting-slurm-job-scripts.md

```markdown
# Preparing and Submitting Slurm Job Scripts

This section provides guidelines on using the Slurm workload manager for job scheduling.

## What is Slurm?
Slurm is an open-source job scheduler designed for Linux clusters. It manages job queuing and execution on clusters.

## What is the Queue?
In Slurm, jobs are submitted to a queue. The scheduler allocates resources based on the specified options and availability.

## Is There a Way to Cut in Line?
Using priority flags when submitting jobs can help improve their position in the queue, but ensure it adheres to your organization’s policies.

## Requesting a Compute Node to Use Interactively
To request an interactive session, you can use:
```bash
srun --pty bash
