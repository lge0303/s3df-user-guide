S3DF New User Guide

Welcome to the SLAC Shared Scientific Data Facility (S3DF)!

This guide will help new users get started with accessing and using S3DF resources. It is modeled after the NERSC beginner guide and complements the official S3DF onboarding site.

🔑 Access Requirements

Before logging into S3DF, make sure you:

Have a valid SLAC Unix account

Have been added to the appropriate project

Have an SSH key pair (for terminal access)

🖥️ Login to S3DF

There are three main ways to access S3DF, depending on your needs: terminal (SSH), remote desktop (NoMachine), and browser-based portal (OnDemand).

✅ Example 1: Login via SSH (Terminal)

Scenario: You are on your laptop (macOS, Linux, or Windows using WSL) and want to connect to S3DF via the command line.

ssh your_username@s3dflogin.slac.stanford.edu

Replace your_username with your SLAC Unix login.

You may be asked to confirm the SSH fingerprint.

After login, you'll be in your S3DF home directory: /sdf/home/your_username/

File transfer:

scp file.txt your_username@s3dflogin.slac.stanford.edu:/sdf/home/your_username/

⚠️ Windows Users: If you encounter an error like Corrupted MAC on input or message authentication code incorrect, try:

ssh -m hmac-sha2-512 your_username@s3dflogin.slac.stanford.edu

🔄 These SSH login nodes are bastion hosts with access only to your home directory. To use compute or storage resources, you must SSH from here to an interactive compute node.

✅ Example 2: Login via S3DF OnDemand (Web Portal)

Scenario: You want to access S3DF through your browser (no command line required).

Open this link in your browser:

https://s3df.slac.stanford.edu

Click "Login" in the upper right.

Enter your SLAC credentials.

After login, you can:

Launch a Shell Terminal

Start a Jupyter Notebook

Open a Remote Desktop

View and manage jobs, storage, and more

💡 The OnDemand portal is beginner-friendly and does not require software installation.

✅ Optional: Use NoMachine (Graphical Remote Desktop)

Scenario: You want a persistent graphical desktop session.

Download and install the NoMachine client for your platform.

Connect to:

s3dfnx.slac.stanford.edu

Benefits:

Better performance for graphical/X11 apps over slow networks

Sessions persist across disconnections

See the NoMachine section of the official S3DF site for more setup details.

Next Steps

Learn about storage locations

Submit your first Slurm job

Explore available modules and environments

For more details, visit the official S3DF site.

This guide is maintained on GitHub — contributions welcome!


# Logging on to S3DF

This section provides guidance on how to log in to the S3DF using various methods:

## Log In Using a Terminal
1. Open your terminal application.
2. Use SSH to log in:
   ssh username@s3df.slac.stanford.edu
3. Enter your password when prompted
 
## Log In Using NoMachine
1. Open NoMachine on your computer.
2. Enter the connection details:
   Host: s3df.slac.stanford.edu
3. Username: Your S3DF username
Connect and enter your password.

## Log In Using OnDemand
1. Navigate to the OnDemand portal at OnDemand Login.
2. Enter your S3DF credentials.
3. Once logged in, you can launch interactive applications.
