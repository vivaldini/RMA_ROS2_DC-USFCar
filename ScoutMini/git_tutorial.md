# Git Tutorial for Students

This guide covers the essential Git skills you need for this course: cloning the repository and keeping your local copy up to date as new content is pushed.

---

## 1. First-time Setup

### Install Git

```bash
sudo apt update
sudo apt install git -y
```

Verify it worked:

```bash
git --version
```

### Configure your identity (one-time)

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## 2. Clone the Repository

You only do this **once**, to get a local copy of the project:

```bash
cd ~/
git clone https://github.com/vivaldini/scout_ws.git
cd scout_ws
```

This creates a folder `~/scout_ws/` on your machine that is linked to the remote repository on GitHub.

---

## 3. Getting Updates

Whenever the instructor pushes new files or fixes, you need to pull those changes into your local copy.

### Check if there are any new changes first (optional but recommended)

```bash
cd ~/scout_ws
git fetch origin
git status
```

- `git fetch` downloads new changes from GitHub without applying them yet.
- `git status` tells you whether your local branch is behind the remote.

### Pull the updates

```bash
cd ~/scout_ws
git pull
```

This downloads and applies the latest changes to your local copy.

After pulling, always rebuild the workspace so your ROS 2 environment picks up any new packages:

```bash
colcon build
source install/setup.bash
```

---

## 4. Understanding What Changed

To see a summary of what was updated in the latest pull:

```bash
git log --oneline -10
```

This shows the 10 most recent commits (each line = one change set), newest first. Example output:

```
e5f4983 Fix warnings - maze_class5 world file
81cbbca Update launch files
d33896d fix: resolve all linting and style errors
```

To see exactly which files changed in the last commit:

```bash
git show --stat HEAD
```
---
