### git-cheat-sheet

### Basic git commands

1. To initialize a new Git repository
    ```bash
    git init
    ```

2. Get the status of changes as untracked, modified, or staged in your working directory
    ```bash
    git status
    ```

3. Used to stage all changes in the current directory and its subdirectories for the next commit
    ```bash
    git add .
    ```
    > git add button.tsx input.tsx
  
4. Used to commit the changes that you have staged using ```git add``` to the Git repository. The ```-m``` flag allows you to include a commit message directly from the command line
    ```bash
    git commit -m "<message>"
    ```
  
5. Used to unstage changes that have been previously staged using ```git add```
    ```bash
    git restore --staged <file>
    ```
    > git restore --staged button.tsx

6. Used to display a log of commits in a Git repository
    ```bash
    git log
    ```

7. Used to reset the current branch to a specific commit or to unstage changes
    ```bash
    git reset <hash-code>
    ```

---
### Working with branches

1. Used to create a new branch in your Git repository named ```branch-name```
    ```bash
    git branch <branch-name>
    ```

2. Used to switch your working directory to the branch named ```branch-name```. This command is commonly used when you want to move to a different branch in your Git repository
    ```bash
    git checkout <branch-name>
    ```

3. Used to integrate changes from one branch, typically named ```branch-name``` into the currently checked-out branch. The branch you are merging into is often referred to as the "target" or "destination" branch
    ```bash
    git merge <branch-name>
    ```
    > ```bash
    > # Switch to the branch where you want to merge the changes
    > git checkout main
    >
    > # Perform the merge with the feature branch
    > git merge feature
    > ```
    > This sequence of commands switches to the "main" branch (you can replace "main" with the name of your target branch) and then merges the changes from the "feature" branch into the "main" branch.

---
### Working with github

1. Used to display the URLs of the remote repositories associated with your local Git repository
    ```bash
    git remote -v
    ```

2. Used to add a remote repository named ```origin``` to your local Git repository
    ```bash
    git remote add <url-name> "<url-value>"
    ```
    > git remote add origin "git@github.com:imopbuilder/git-cheat-sheet.git"

3. Used to change the URL of the remote repository named ```origin``` in your local Git configuration. This command is helpful when you need to update the remote URL, such as when the repository location has changed
    ```bash
    git remote set-url <url-name> "<url-value>"
    ```
    > git remote set-url origin "git@github.com:imopbuilder/nextjs-express-turbo.git"

4. Used to push the changes from your local branch named ```branch-name``` to the remote repository named ```url-name```
   ```bash
   git push <url-name> <branch-name>
   ```
   > git push origin main
   
5. Used to pull the changes of branch named ```branch-name``` from the remote repository named ```url-name``` to the local Git repository
    ```bash
    git pull <url-name> <branch-name>
    ```
    > git pull origin main
