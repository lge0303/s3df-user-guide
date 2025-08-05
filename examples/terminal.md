#### 6. examples/terminal.md

```markdown
# Terminal Job Submission Example

1. Write a simple Slurm job script `job.sh`:

```bash
#!/bin/bash
#SBATCH --job-name=my-job
#SBATCH --output=output.txt
#SBATCH --ntasks=1
#SBATCH --time=00:10:00

echo "Running my job"
sleep 30
echo "Job completed"

2. Submit the job with:
sbatch job.sh
