# Workflow Example: Running ACE3P on Terminal
This document provides a step-by-step guide on how to run the ACE3P executable on S3DF, including accessing the system, preparing your job, and monitoring its execution.

## Step 1: Log In to the S3DF System

### 1. Access the Bastion Host:
Open your terminal and log in to the S3DF bastion host using the following command:

    ssh s3dflogin.slac.stanford.edu

### 2. Connect to an Interactive Pool Node:
Once logged into the bastion host, connect to an interactive pool node to prepare your job:


    ssh <interactive_pool_name>

Replace <interactive_pool_name> with the name of your desired interactive pool (e.g., iana, rubin-devl, etc.).

## Step 2: Prepare Your ACE3P Job
### 1. Load the Required Modules:
Ensure that you have the necessary environment modules loaded for running ACE3P. Use the following command:

module load XXX

### 2. Create a Job Submission Script:
Create a text file (e.g., ace3p_job.sh) for your job submission script using your preferred text editor. Here’s a sample script:

    #!/bin/bash

    #SBATCH --partition=milano       # Choose the appropriate partition
    #SBATCH --job-name=ace3p_job     # Job name
    #SBATCH --output=ace3p_output-%j.txt   # Output file
    #SBATCH --error=ace3p_error-%j.txt     # Error file
    #SBATCH --ntasks=1                # Number of tasks (usually 1 for ACE3P)
    #SBATCH --cpus-per-task=16        # Number of CPU cores per task
    #SBATCH --mem=64G                  # Memory required
    #SBATCH --time=0-02:00:00         # Time limit (2 hours)

    # Run ACE3P executable with the appropriate input files
    srun ace3p your_input_file.ace3p
Replace your_input_file.ace3p with the name of your ACE3P input file.

## Step 3: Submit the Job
### 1. Submit the Job to Slurm:
Use the sbatch command to submit your ACE3P job script:

    sbatch ace3p_job.sh

### 2. Monitor the Job Status:
To check the status of your job, you can use the following command:

    squeue -u your_username
Replace your_username with your actual S3DF username.

### 3. Check Job Details:
For detailed information about your job's progress, including resources requested and state, use:

    scontrol show job <job_id>
Replace <job_id> with the specific job ID provided upon job submission.

## Step 4: Postprocess


You have successfully submitted and run an ACE3P executable on S3DF. By following this workflow, you can efficiently utilize the S3DF resources for your computational tasks. If you encounter any issues, refer to the S3DF documentation or contact support for assistance.
