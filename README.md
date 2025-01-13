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

## Basic Git commands
- `git status` Displays the state of the working directory and staging area. Use this command to check modified, staged, and untracked files.
- `git add` Adds the specified file(s) to the staging area, making them ready for the next commit.
- `git commit -m "message"` Saves changes in the staging area to the repository with a descriptive commit message.
- `git push` Uploads your local repository changes to a remote repository, such as GitHub.
- `git pull` Fetches changes from a remote repository and integrates them into your local repository.
- `git log` Displays the commit history, showing all previous commits with details such as the author, date, and commit message.

## Rules for Writing Commit Messages

To maintain clarity and consistency in commit history, follow these rules when writing commit messages:

1. **Use the Present Tense**  
   - Write commit messages in the present tense (e.g., "Add feature" instead of "Added feature").  

2. **Capitalize the First Letter**  
   - Start the commit message with a capital letter.

3. **Keep it Short**  
   - Limit the commit message to 50 characters or less. If additional details are necessary, use the body of the commit.

4. **Use Prefixes for Categorization**  
   - Begin commit messages with specific prefixes to categorize changes:  
     - **`fix:`** For bug fixes or issue-related changes.  
     - **`feat:`** For adding or removing features or functionalities.  
     - **`chore:`** For routine updates, maintenance tasks, or refactoring.  
     - **`docs:`** For changes or updates in the documentation.  
   - **Details of Prefixes:**
     1. **fix** - Bugs or issues related.
     2. **feat** - Addition or removal of a feature or functionality.
     3. **chore** - Routine maintenance or updates.
     4. **docs** - Changes in the documentation.

#### Examples:
- `fix: resolve issue with login button not working`
- `feat: add dark mode toggle to settings`
- `chore: update dependencies to latest versions`
- `docs: update README with setup instructions`

## Branching in GitHub

### Branching Strategy
At ChaiCode, we follow a structured branching strategy to ensure smooth collaboration and maintain code quality. Our main branches are:

1. **`main`**: This branch contains the production-ready code. It should always remain stable and deployable.
2. **`development`**: This branch is used for integrating features and testing. It acts as a staging area before merging into the `main` branch.
3. **Feature Branches**: Feature branches are created for individual tasks or features. They allow isolated work without impacting the `main` or `development` branches.

### Creating and Switching Branches
To create a new branch and switch to it, use the following commands:

```
git branch feature/tea-menu
git checkout feature/tea-menu
```
- You can combines these two steps in one by using this command:
`git checkout -b feature/tea-menu`

### Guidelines for merging branches
1. **Always Test Before Merging:** Ensure your changes are tested and free from errors.
2. **Update Your Branch:** Pull the latest changes from the development or main branch before merging to avoid conflicts:
```
git pull origin development
```
3. Create a Pull Request (PR): Use GitHub to create a PR for merging changes.
4. Resolve Conflicts: If conflicts arise, resolve them locally and push the changes.

## Pull Requests (PR)
### Creating a PR on GitHub
1. Push your branch to GitHub
```
git push origin feature/tea-menu
```
2. Go to the repository on GitHub and click on the Pull Requests tab.
3. Click New Pull Request.
4. Select the base branch `(e.g., development)` and compare it with your feature branch `(e.g., feature/tea-menu)`.
5. Add a descriptive title and detailed description for your PR.

### Writing PR Descriptions

1. **Title**  
   Use a concise title that summarizes the change.  
   _Example:_ `Add tea menu feature`

2. **Description**  
   - Include the purpose of the change.  
   - Reference any relevant issues.  
     _Example:_ `Closes #123`  
   - Provide testing instructions, if applicable.

3. **Request Reviews**  
   - Assign reviewers.  
   - Tag relevant team members to provide feedback.

## Best Practices
### Regular Commits
- Commit your changes regularly to ensure a well-documented history.
- Each commit should represent a single, logical change.
### Descriptive Commit Messages
- Use clear and concise commit messages.
- Follow the format: `<prefix>: <message>` (e.g., `feat: add tea menu feature`).
### Pull Updates Regularly
- Regularly pull updates from the `main` or `development` branches to keep your branch up to date:
```
git pull origin development
```
- This helps avoid large, complex merge conflicts later.
By adhering to these workflows and best practices, we can ensure effective collaboration and maintain a clean, organized codebase.
