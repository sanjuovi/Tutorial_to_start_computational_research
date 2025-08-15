# Tutorial_to_start_computational_research
This tutorial is a record of the steps I followed when starting my journey in computational research. I began with zero experience in coding, comput. tools, or resources in this field. My aim is to provide a basic, beginner-friendly guide for others like me who may have limited resources or experience and to serve as a future reference for myself.

## My Computing Environment
When working in computational chemistry, biology, or physics, many tools and software packages are designed to run more efficiently on Linux systems. While not all programs require Linux — some work equally well or even better on Windows — having a Linux environment can give you more flexibility and compatibility.

I began my journey in computational research on a Windows 10 laptop while working with Gaussian for catalysis reaction mechanism studies during my time at IIT Bhilai, India. At that stage, I worked entirely within Windows. Later, when I moved to TU Delft and started working on molecular dynamics (MD) simulations, I realized that most of my work involved command-line operations, and many tools were better supported in Linux. That’s when I decided to install a Linux subsystem using Windows Subsystem for Linux (WSL). I chose Ubuntu as my Linux distribution and set up my working environment using Miniconda to manage packages and environments.

Today, my workflow is:
- Operating System: Windows 10 (primary)
- Linux Environment: Ubuntu via WSL
- Package/Environment Manager: Conda (Miniconda)
- Usage: Run MD simulation tools, data analysis scripts, and other computational workflows directly in Ubuntu.
  

This setup allows me to run Linux-based computational tools on my Windows laptop without needing a separate Linux machine. WSL 2 provides near-native performance and excellent compatibility with most scientific software.

> Note: I have not documented every installation step at the time, so this section is based on my personal experience and memory. The aim is to share the motivation and general process rather than a strict installation guide.
>

### How I (likely) set up WSL + Ubuntu on my laptop
Although I did not record every step at the time, the process I followed was most likely:

1. Enabled WSL on Windows 10  
   - Opened PowerShell as Administrator and ran:  
     ```powershell
     wsl --install
     ```
     or  
     ```powershell
     dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
     dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
     ```

2. Installed Ubuntu from the Microsoft Store 
   - Searched for Ubuntu 20.04 in the Microsoft Store and installed Ubuntu 20.04 (may be latest available that time).

3. Launched Ubuntu for the first time  
   - Typed `Ubuntu` in the Windows search bar and clicked the app and followed the instructions to set up a Linux username and password.

4. Install Miniconda
   - Download the installer:
     ```bash
     wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
     ```
   - Install:
     ```bash
     bash Miniconda3-latest-Linux-x86_64.sh
     ```
   - Restart the terminal so Conda is active.

5. Create Conda Environment for Work
   conda create -n md_env python=3.10
   conda activate md_env

6. Update Ubuntu
   - Inside Ubuntu terminal:
     sudo apt update && sudo apt upgrade -y (it will ask for your password once in a day).


### 🔍 Why this setup
- Most molecular dynamics and computational chemistry tools are better supported on Linux, WSL 2 lets me use these tools directly on my Windows laptop without a virtual machine or dual boot.
- I can still use Windows applications alongside Linux tools.
Setting up Linux using WSL.



> Note: I did not record every single installation step when I first set up my system. The process described here is based on my personal experience and memory, meant to share the reasoning and general workflow rather than a step-by-step technical guide.

