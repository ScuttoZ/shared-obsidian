## IBM cheat sheet
### Commands with syntax
1. **git add**
    
    - _Description_: It adds changes to the staging area. This command stages the changes made to the files and prepares them for the next commit.
        
    - _Syntax_:
        
        - **git add \<filename.txt>** (to add a specific file)
        - **git add .** (to add all the files that are new or changed in the current directory)
        - **git add -A** (to add all changes in the entire working tree, from the root of the repository, regardless of where you are in the directory structure)
2. **git reset**
    
    - _Description_: It resets changes in the working directory. When used with –hard HEAD, this command discards all changes made to the working directory and staging area and resets the repository to the last commit (HEAD).
        
    - _Syntax_:
        
        - **git reset**
        - **git reset –hard HEAD**
3. **git branch**
    
    - _Description_: It lists, creates, or deletes branches in a repository. To delete the branch, first check out the branch using **git checkout** and then run the command to delete the branch locally.
        
    - _Syntax_:
        
        - **git branch** (to list branches)
        - **git branch \<new-branch>** (to create a new branch)
        - **git branch -d \<branch-name>** (to delete a branch)
4. **git checkout main**
    
    - _Description_: It switches to the "main" branch. This will switch your current branch to "main."
        
    - _Syntax_: **git checkout main**
5. **git clone**
    
    - _Description_: It copies a repository from a remote source to your local machine. This will create a copy of the repository in your current working directory.
        
    - _Syntax_: **git clone \<repository URL>**
6. **git pull**
    
    - _Description_: It fetches changes from a remote repository and merges them into your local branch. First, switch to the branch that you want to merge changes into by running the **git checkout** command. Then, run the **git pull** command, which will fetch the changes from the main branch of the origin remote repository and merge them into your current branch.
        
    - _Syntax_: **git pull origin main**
7. **git push**
    
    - _Description_: It uploads local repository content to a remote repository. Make sure you are on the branch that you want to push by running the **git checkout** command first, then push the branch to the remote repository.
        
    - _Syntax_: **git push origin \<branch-name>**
8. **git version**
    
    - _Description_: It displays the current Git version installed on your system.
        
    - _Syntax_: **git version**
9. **git diff**
    
    - _Description_: It shows changes between commits, commit and working tree, etc. It also compares the branches.
        
    - _Syntax_:
        
        - **git diff** (shows the difference between the working directory and the last commit)
        - **git diff HEAD~1 HEAD** (shows the difference between the last and second-last commits)
        - **git diff \<branch-1> \<branch-2>** (compares the specified branches)
10. **git revert**
    
    - _Description_: It reverts a commit by applying a new commit. This will create a new commit that undoes the changes made by the last commit.
        
    - _Syntax_: **git revert HEAD**
11. **git config --global user.email \<Your GitHub Email>**
    
    - _Description_: It sets a global email configuration for Git. This needs to be executed before doing a commit to authenticate the user's email ID.
        
    - _Syntax_: **git config –global user.email \<Your GitHub Email>**
12. **git config --global user.name \<Your GitHub Username>**
    
    - _Description_: It sets a global username configuration for Git. This needs to be executed before doing a commit to authenticate users' username.
        
    - _Syntax_: **git config –global user.name \<Your GitHub Username>**
13. **git remote**
    
    - _Description_: It lists the names of all remote repositories associated with your local repository.
        
    - _Syntax_: **git remote**
14. **git remote -v**
    
    - _Description_: It lists all remote repositories that your local Git repository is connected to, along with the URLs associated with those remote repositories.
        
    - _Syntax_: **git remote -v**
15. **git remote add origin \<URL>**
    
    - _Description_: It adds a remote repository named "origin" with the specified URL.
        
    - _Syntax_: **git remote add origin \<URL>**
16. **git remote rename**
    
    - _Description_: The git remote rename command is followed by the name of the remote repository (origin) you want to rename and the new name (upstream) you want to give it. This will rename the "origin" remote repository to "upstream."
        
    - _Syntax_: **git remote rename origin upstream**
17. **git remote rm \<name>**
    
    - _Description_: It removes a remote repository with the specified name.
        
    - _Syntax_: **git remote** _rm origin_
18. **git format-patch**
    
    - _Description_: It generates patches for email submission. These patches can be used for submitting changes via email or for sharing them with others.
        
    - _Syntax_: **git format-patch HEAD~3** (creates patches for the last three commits)
19. **git request-pull**
    
    - _Description_: It generates a summary of pending changes for an email request. It helps communicate the changes made in a branch or fork to the upstream repository maintainer.
        
    - _Syntax_: **git request-pull origin/main \<myfork or branch_name>**
20. **git send-email**
    
    - _Description_: It sends a collection of patches as emails. It allows you to send multiple patch files to recipients via email. Please make sure to set the email address and name using the **git config** command so that the email client knows the sender's information when sending the emails.
        
    - _Syntax_: **git send-email *.patch**
21. **git am**
    
    - _Description_: It applies patches to the repository. It takes a patch file as input and applies the changes specified in the patch file to the repository.
        
    - _Syntax_: **git am \<patchfile.patch>**
22. **git daemon**
    
    - _Description_: It exposes repositories via the Git:// protocol. The Git protocol is a lightweight protocol designed for efficient communication between Git clients and servers.
        
    - _Syntax_: **git daemon –base-path=/path/to/repositories**
23. **git instaweb**
    
    - _Description_: It instantly launches a web server to browse repositories. It provides a simplified way to view repository contents through a web interface without the need for configuring a full web server.
        
    - _Syntax_: **git instaweb –httpd=webrick**
24. **git rerere**
    
    - _Description_: It reuses recorded resolution of previously resolved merge conflicts. Please note that rerere.enabled configuration option needs to be set to "true" (**git config –global rerere.enabled true**) for git rerere to work. Additionally, note that git rerere only applies to conflicts that have been resolved using the same branch and commit.
        
    - _Syntax_: **git rerere**



### Commands with examples

| **Package/Method**                 | **Description**                                                                                                                                          | **Code Example**                                                                                                                                                                 |
| :--------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **git add**                        | Used to move changes from the working directory to the staging area                                                                                      | `git add sample.md`                                                                                                                                                              |
| **git add .**                      | Allows to move the changed files into the staging area on GitHub repositories                                                                            | `git add .`                                                                                                                                                                      |
| **git am**                         | Used to apply patches emailed to the repository                                                                                                          | `git am < patchfile.patch`                                                                                                                                                       |
| **git branch**                     | Allows to create an isolated environment within the repository to make changes                                                                           | `git branch <new-branch>`                                                                                                                                                        |
| **git checkout**                   | Allows to see and change existing branches                                                                                                               | `git checkout <existing-branch>`                                                                                                                                                 |
| **git checkout main**              | Allows to switch to the main branch                                                                                                                      | `git checkout main`                                                                                                                                                              |
| **git clone**                      | Allows to create a copy of the remote repository                                                                                                         | `git clone <repository-url>`                                                                                                                                                     |
| **git commit**                     | Allows you to take staged snapshots if changes and commit them to the project                                                                            | `git commit -m "Your commit message here"`                                                                                                                                       |
| **git config --global user.email** | Example 1: Sets a global email configuration for Git  <br>  <br>Example 2: Sets a global username configuration for Git                                  | Example 1:  <br>`git config --global user.email "your.email@example.com"`<br>Example 2:  <br>`git config --global user.name "Your Name"`                                         |
| **git daemon**                     | Used to allow anonymous download from the repository                                                                                                     | `git daemon --reuseaddr --verbose`                                                                                                                                               |
| **git diff**                       | Helps others to review your code to identify and compare the changes                                                                                     | `git diff example.txt`                                                                                                                                                           |
| **git fetch**                      | Used to transfer the changes from the remote repo to your local repo                                                                                     | `git fetch <options> <remote name> <branch name>`                                                                                                                                |
| **git fetch upstream/master**      | Used to grab upstream branches                                                                                                                           | `git fetch upstream master:upstream-master`                                                                                                                                      |
| **git format-patch**               | Generates or prepares e-mail submission if you adopt Linux kernel-style public forum workflow                                                            | `git format-patch -n <number_of_commits>`                                                                                                                                        |
| **git http-backend**               | Provides a server-side implementation of Git-over-HTTP, allowing both fetch and push services                                                            | `git clone --bare /path/to/repos/myrepo.git`<br>`cd myrepo.git`<br>`git update-server-info`                                                                                      |
| **git init**                       | Used to clone an existing repository                                                                                                                     | `git init <directory>`                                                                                                                                                           |
| **git instaweb**                   | Allows to set up web front-end to Git repositories                                                                                                       | `git instaweb -p 8080`                                                                                                                                                           |
| **git log**                        | Enables to browse previous changes to a project                                                                                                          | `git log -p filename`                                                                                                                                                            |
| **git merge**                      | Used to merge changes in the active branch into another branch                                                                                           | `git merge feature_branch`                                                                                                                                                       |
| **git merge upstream/master**      | Merges changes from the 'upstream/master' branch to the current branch                                                                                   | `git merge upstream/master`                                                                                                                                                      |
| **git pull**                       | Used to transfer the changes from the remote repo to your local repo, and merge them to a branch                                                         | `git pull origin main`                                                                                                                                                           |
| **git pull downstream**            | Pulls changes from a downstream repository, specifically from the master branch of that repository                                                       | `git pull downstream main`                                                                                                                                                       |
| **git pull upstream**              | Pulls changes from the "upstream" repository into the current branch                                                                                     | `git pull upstream main`                                                                                                                                                         |
| **git push**                       | Used to push all the committed changes into the repository                                                                                               | `git push origin your_branch_name`                                                                                                                                               |
| **git remote**                     | A command to manage a set of tracked repositories                                                                                                        | `git remote add upstream https://github.com/original/repo.git`                                                                                                                   |
| **git remote add origin <URL>**    | Adds a remote repository named "origin" with the specified URL                                                                                           | `git remote add origin https://github.com/yourusername/your-repo.git`                                                                                                            |
| **git remote add upstream**        | Adds the original repository as a new remote repository labeled upstream                                                                                 | `git remote add upstream https://github.com/original/repo.git`                                                                                                                   |
| **git remote rename**              | The git remote rename command is followed by the name of the remote repository(origin) you want to rename and the new name(upstream) you want to give it | `git remote rename origin new-origin`                                                                                                                                            |
| **git remote -v**                  | Allows to view the remotes associated with the local repository                                                                                          | `git remote -v`                                                                                                                                                                  |
| **git request-pull**               | Example 1: Creates a summary of changes for your upstream to pull  <br>  <br>Example 2: Generates a summary of pending changes for an email request      | Example 1:  <br>`git request-pull origin/main your-branch`<br>Example 2:  <br>`git request-pull <base> <head> <repository>`                                                      |
| **git rerere**                     | Reuses recorded resolution of previously resolved merge conflicts                                                                                        | `git rerere`<br>`git rerere diff`                                                                                                                                                |
| **git reset**                      | Undoes changes that were made to the files in your working directory                                                                                     | `git reset HEAD~1`                                                                                                                                                               |
| **git revert**                     | Used to undo botched commits                                                                                                                             | `git revert HEAD`                                                                                                                                                                |
| **git send-email**                 | Example 1: Sends your email submission without corruption by your MUA  <br>  <br>Example 2: Sends a collection of patches as emails                      | Example 1:  <br>`git send-email --to=recipient@example.com`<br>`path/to/patchfile.patch`<br>Example 2:  <br>`git send-email --to recipient@example.com`<br>`patches/*.patch`<br> |
| **git-shell**                      | Used as a restricted login shell for shared central repository users                                                                                     | `sudo usermod -s /usr/bin/git-shell gituser`                                                                                                                                     |
| **git status**                     | Allows to see the state of your working directory and the staged snapshot of the changes                                                                 | `git status`                                                                                                                                                                     |
| **git version**                    | Displays the current Git version installed on your system                                                                                                | `git --version`                                                                                                                                                                  |
| **git web**                        | Provides a web front-end to Git repositories                                                                                                             | `git instaweb --port=8080`                                                                                                                                                       |

### Glossary
| Term                                          | Definition                                                                                                                                                                                                                                                                                                                  |
| --------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Branch**                                    | A separate line of development that allows to work on features or fixes independently.                                                                                                                                                                                                                                      |
| **Clone**                                     | A local copy of the remote Git repository on the computer.                                                                                                                                                                                                                                                                  |
| **Cloning**                                   | A process of creating a copy of the project's code and its complete version history from the remote repository on the local machine.                                                                                                                                                                                        |
| **Commit**                                    | A snapshot of the project's current state at a specific point in time, along with a description of the changes made.                                                                                                                                                                                                        |
| **Continuous delivery (CD)**                  | The automated movement of software through the software development lifecycle.                                                                                                                                                                                                                                              |
| **Continuous integration (CI)**               | A software development process in which developers integrate new code into the code base at least once a day.                                                                                                                                                                                                               |
| **Developer**                                 | A computer programmer who is responsible for writing code.                                                                                                                                                                                                                                                                  |
| **Distributed version control system (DVCS)** | A system that keeps track of changes to code, regardless of where it is stored. It allows multiple users to work on the same codebase or repository, mirroring the codebase on their computers if needed, while the distributed version control software helps manage synchronization amongst the various codebase mirrors. |
| **Fork**                                      | A copy of a repository. You can fork a repository to use it as the base for a new project or to work on a project independently.                                                                                                                                                                                            |
| **Forking**                                   | Forking creates a copy of a repository on which one can work without affecting the original repository.                                                                                                                                                                                                                     |
| **Git**                                       | Free and open-source software distributed under the GNU General Public License. It is a distributed version control system that allows users to have a copy of their own project on their computer anywhere in the world.                                                                                                   |
| **GitHub**                                    | A web-hosted service for the Git repository.                                                                                                                                                                                                                                                                                |
| **GitHub branches**                           | A branch stores all files in GitHub. Branches are used to isolate changes to code. When the changes are complete, they can be merged back into the main branch.                                                                                                                                                             |
| **GitLab**                                    | A complete DevOps platform delivered as a single application. It provides access to Git repositories, controlled by source code management.                                                                                                                                                                                 |
| **Integrator**                                | A role that is responsible for managing changes made by developers.                                                                                                                                                                                                                                                         |
| **Master branch**                             | A branch that stores the deployable version of your code. The master branch is created by default and is definitive.                                                                                                                                                                                                        |
| **Merge**                                     | A process to combine changes from one branch to another, typically merging a feature branch into the main branch.                                                                                                                                                                                                           |
| **Origin**                                    | A term that refers to the repository where a copy is cloned from.                                                                                                                                                                                                                                                           |
| **Pull request**                              | A process used to request that someone reviews and approves your changes before they become final.                                                                                                                                                                                                                          |
| **Remote repositories**                       | Repositories that are stored elsewhere. They can exist on the internet, on your network, or on your local computer.                                                                                                                                                                                                         |
| **Repository**                                | A data structure for storing documents, including application source code. It contains the project folders that are set up for version control.                                                                                                                                                                             |
| **Repository administrator**                  | A role that is responsible for configuring and maintaining access to the repository.                                                                                                                                                                                                                                        |
| **SSH protocol**                              | A method for secure remote login from one computer to another.                                                                                                                                                                                                                                                              |
| **Staging area**                              | An area where commits can be formatted and reviewed before completing the commit.                                                                                                                                                                                                                                           |
| **Upstream**                                  | A term used by developers to refer to the original source where the local copy was cloned from.                                                                                                                                                                                                                             |
| **Version control**                           | A system that allows you to keep track of changes to your documents. This process allows you to recover older versions of the documents if any mistakes are made.                                                                                                                                                           |
| **Working directory**                         | A directory in your file system that contains files and subdirectories on your computer that are associated with a Git repository.                                                                                                                                                                                          |