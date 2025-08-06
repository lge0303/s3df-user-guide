
# 🔑 How to Access S3DF

S3DF supports three main access methods depending on your needs: terminal (SSH), remote desktop (NoMachine), and browser-based access (OnDemand). Below is a breakdown of each option:


## 1. 🖥️ SSH (Terminal Access)

If you're comfortable using a terminal, SSH is the most direct way to access S3DF.

- Use any SSH client such as:

  - macOS/Linux: Built-in terminal with ssh

  - Windows: PuTTY or Windows Terminal with OpenSSH

- Connect to the S3DF login pool using this command:

     ssh your_username@s3dflogin.slac.stanford.edu

- These login nodes are bastion hosts and only give access to your home directory.

- To use storage or run compute jobs, you’ll need to SSH again from the login node to an interactive compute node.

## ⚠️ Windows Users:
If you see an error like:

    Corrupted MAC on input or message authentication code incorrect
    
try adding this flag to your SSH command:

    ssh -m hmac-sha2-512 your_username@s3dflogin.slac.stanford.edu

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
