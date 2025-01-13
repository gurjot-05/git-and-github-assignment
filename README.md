# Welcome to Git and GitHub at ChaiCode Cohort!
This documentation serves as a comprehensive guide for ChaiCode developers to use Git and GitHub effectively in their workflows.

## Why Git?
Imagine starting a game of GTA San Andreas, and you are on the last mission, and that mission fails because, God knows what, it's frustrating, right? You have to start all over again. Instead, you could've saved your progress after completing each mission, and if any mission failed you'd at least have saved progress till previous missions. The same is the case with our code. Imagine you have a working code and now you have made a lot of changes to implement a new feature in your website and now the whole website has crashed. You've lost track of the changes you made and now it's impossible to return to the previous code. This is where version control helps. 

**Git** is a version control system that allows you to track changes to your files and collaborate with others. It is used to manage the history of your code and to merge changes from different branches.

## What is GitHub?
Sending a code via USB seems outdated and time-consuming right? GitHub is a web-based platform that provides hosting and collaboration tools for developers to manage and share their code. It is built on top of Git, a distributed version control system, and enhances it with features that facilitate team collaboration, project management, and code deployment.

## Importance of Git and GitHub
### Git Advantages:
- Keep a record of all changes
- See progress over time
- Work on different parts of a project without interfering with others
- Use it anywhere, even without an internet connection

### GitHub Advantages:
- Cloud-based hosting that provides Easy collaboration (pull requests)
- View anyone’s changes in the codebase around the globe

## Git Installation and Setup
**1. Windows**

Visit the official [git website](https://git-scm.com/downloads) to download git for Windows.
![image](https://github.com/user-attachments/assets/211627a6-3e8d-4a15-95db-aec931ec83f2)

**2. MacOS**

For MacOS, git can be installed using the following command:
```
brew install git
```
**3. Linux**

For Linux, git can be installed using the following command:
```
sudo apt update
sudo apt install git
```
> 💡 **Tip:** To check if git is successfully installed, use `git --version`. It should show the installed version of git on your system.

- Run the following commands to set your name and email of your GitHub account:
```
git config --global user.name "Your Name" 
git config --global user.email "your.email@example.com
```
Once you've set your name and email globally using the git config --global command, Git will use those settings automatically for every project you work on, so you don't need to enter them every time you make a commit

- Run the following command to check if your Git Configuration was set correctly
```
git config --global --list
```
If you see values like `user.name='your-name'` then the configurations were set correctly.

## Clone a Git repository
Cloning in Git refers to the process of copying a remote repository (often public) including its histories to your local machine. This allows you to work on the project locally, make changes, and commit those changes independently from the remote repository. However, the changes you make locally won't affect the remote repository unless you push your changes back to the remote.
1. Clone the repo
```
git clone <repo-url>
Example: git clone https://github.com/HKUDS/LightRAG.git
```
Repo-URL can be found from the repo's `code` dropdown
![image](https://github.com/user-attachments/assets/4563f822-e997-40ca-add5-2b1e6c0db2f7)
2. Navigating to the repo
```
cd <cloned-project-folder-name> // to go to the cloned repo
code . // to open your repo in vs-code
```
