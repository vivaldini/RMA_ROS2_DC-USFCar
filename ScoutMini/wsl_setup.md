\# WSL2 Setup Guide for ROS 2 (Windows Users)



\## Overview



This guide explains how to prepare a clean Linux environment using \*\*WSL2 (Windows Subsystem for Linux)\*\* for ROS 2 development.



\### Final Goal



At the end of this setup, you should have:



\- WSL2 installed and working

\- A clean Ubuntu environment

\- No previous conflicting ROS installations

\- Ready to install ROS 2



\---



\## Step 1 — Check if WSL is Installed



Open \*\*PowerShell\*\* and run:



```powershell

wsl --status

```



\*\*Expected Output\*\*

You should see something like:



```text

Default Version: 2

Kernel version

Distribution info (optional)

```



\*\*If WSL is NOT Installed\*\*

Run:



```powershell

wsl --install

```

Then restart your computer.



\---



\## Step 2 — List Installed Linux Distributions



Run:



```powershell

wsl --list --verbose

```

or:



```powershell

wsl -l -v

```



\*\*Example Output\*\*



```text

NAME            STATE           VERSION

Ubuntu          Running         2

Ubuntu-22.04    Stopped         2

```



\*\*Interpretation\*\*



| Situation | Meaning |

| :--- | :--- |

| \*\*No distributions\*\* | Clean system, good starting point. |

| \*\*Ubuntu exists\*\* | You may reuse or reset it. |

| \*\*Multiple distros\*\* | Choose one or clean old ones. |



\---



\## Step 3 — Clean Existing Installations (Recommended)



> \*\*Warning:\*\* This deletes everything inside the selected Linux distribution.



To remove an existing Ubuntu distribution, run:



```powershell

wsl --unregister Ubuntu

```

or, if it has a versioned name:



```powershell

wsl --unregister Ubuntu-22.04

```



Then verify again:



```powershell

wsl -l -v

```



\---



\## Step 4 — Install a Fresh Ubuntu System



Install Ubuntu using:



```powershell

wsl --install -d Ubuntu-24.04

```

> \*\*Note:\*\* Ubuntu 24.04 is recommended for ROS 2 Jazzy.



\---



\## Step 5 — First Launch Setup



When Ubuntu starts for the first time, it will ask:



```text

Enter new UNIX username:

Enter new UNIX password:

```



Choose a username and password and complete the initialization.



\---



\## Step 6 — Verify Ubuntu Installation



Inside the Ubuntu terminal, run:



```bash

lsb\_release -a

```



\*\*Expected Output\*\*



```text

Distributor ID: Ubuntu

Description:    Ubuntu 24.04 LTS

```



\---



\## Summary Checklist



Before installing ROS 2, confirm the following:



\- \[ ] WSL is installed

\- \[ ] Ubuntu 24.04 is installed

\- \[ ] WSL version is 2

