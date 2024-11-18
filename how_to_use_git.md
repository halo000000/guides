## **Step-by-Step Guide to Download and Set Up Git**

#### **Step 1: Download Git**
1. Visit the official Git website: [https://git-scm.com/](https://git-scm.com/).
1. or if you use Windows click this link to download the git [download_git](https://github.com/git-for-windows/git/releases/download/v2.47.0.windows.2/Git-2.47.0.2-64-bit.exe)
1. download Github cli or Github desktop [download_github_cli](https://cli.github.com/)
2. Click the **Download** button for your operating system (Windows, macOS, or Linux).
3. Follow the instructions on the website to download the correct version for your system.

#### **Step 2: Install Git**
1. Locate the downloaded installer and run it.
2. During installation:
   - Accept the license agreement.
   - Choose the installation path (default is fine for most cases).
   - Select components (default selections are sufficient).
   - Configure the terminal emulator:
     - For Windows, you can choose "Git Bash" or use Git in a terminal of your choice.
3. Click **Next** on the remaining screens and complete the installation.

#### **Step 3: Verify Git Installation**
1. Open a terminal or Git Bash.
2. Type the following command and press Enter:
   ```bash
   git --version
   ```
   If installed correctly, it will display the installed Git version.

#### **Step 4: Set Up Git**
1. Configure your name:
   ```bash
   git config --global user.name "Your Name"
   ```
2. Configure your email (use the same email as your GitHub or other repository account):
   ```bash
   git config --global user.email "youremail@example.com"
   ```
3. Optionally, set your default text editor:
   ```bash
   git config --global core.editor "editor-name"
   ```
   Replace `editor-name` with your preferred editor, e.g., `code` for VS Code.

4. Confirm your configuration:
   ```bash
   git config --list
   ```


#### **Step 5: login to  Git**
1. lets make sure we have github cli installed
```
gh --version
```
2. lets login to Github using Github cli
paste this command 
```
gh auth login
```
3. chose github.com
```
> GitHub.com
  Other
```
chose Https
```
> HTTPS
  SSH
```
4. know open the link it gives you and type the code that is in your terminal and click Authenticate
5. rest yor terminal 
---

# **Step-by-Step Guide to Use Git**

#### **Step 1: Initialize a Repository**
1. Navigate to the folder where you want to create a repository:
   ```bash
   cd /path/to/your/folder
   ```
2. Initialize a Git repository:
   ```bash
   git init
   ```

#### **Step 2: Clone a Repository**
To clone an existing repository from a remote source:
```bash
git clone <repository-url>
```

#### **Step 3: Add Files**
1. Check the status of your repository:
   ```bash
   git status
   ```
2. Add files to the staging area:
   ```bash
   git add filename
   ```
   To add all files:
   ```bash
   git add .
   ```

#### **Step 4: Commit Changes**
Commit the staged changes with a message:
```bash
git commit -m "Your commit message"
```

#### **Step 5: Connect to a Remote Repository**
Add a remote repository:
```bash
git remote add origin <repository-url>
```

#### **Step 6: Push Changes**
Push commits to the remote repository:
```bash
git push -u origin main
```
For subsequent pushes:
```bash
git push
```

#### **Step 7: Pull Changes**
Fetch and merge changes from the remote repository:
```bash
git pull
```

---

### **Most Used Git Commands and Their Functions**

| **Command**                  | **Function**                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------|
| `git init`                   | Initializes a new Git repository.                                                           |
| `git clone <repo-url>`       | Clones an existing repository from a URL.                                                   |
| `git status`                 | Shows the status of the working directory and staging area.                                  |
| `git add <file>`             | Adds specific files to the staging area.                                                    |
| `git add .`                  | Adds all changes in the current directory to the staging area.                              |
| `git commit -m "message"`    | Commits staged changes with a descriptive message.                                          |
| `git log`                    | Displays the commit history.                                                                |
| `git remote add origin <url>`| Links your local repository to a remote repository.                                         |
| `git push`                   | Pushes changes to the remote repository.                                                   |
| `git pull`                   | Pulls the latest changes from the remote repository and merges them into the local branch.  |
| `git branch`                 | Lists all branches in the repository.                                                      |
| `git checkout <branch>`      | Switches to a specific branch.                                                              |
| `git merge <branch>`         | Merges changes from another branch into the current branch.                                 |
| `git diff`                   | Shows differences between the working directory and the index/staging area.                |
| `git fetch`                  | Downloads updates from the remote repository but doesn’t merge them automatically.          |
| `git reset`                  | Unstages files or resets commits.                                                           |

