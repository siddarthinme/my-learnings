Here’s a comprehensive list of common Git and GitHub commands for managing repositories, branches, commits, and more:

---

### **General Git Setup**
1. **Configure Git username**  
   ```bash
   git config --global user.name "Your Name"
   ```
2. **Configure Git email**  
   ```bash
   git config --global user.email "your.email@example.com"
   ```
3. **Check Git configuration**  
   ```bash
   git config --list
   ```

---

### **Starting a Repository**
1. **Initialize a new Git repository**  
   ```bash
   git init
   ```
2. **Clone an existing repository**  
   ```bash
   git clone <repository-url>
   ```

---

### **Making Changes**
1. **Check the status of changes**  
   ```bash
   git status
   ```
2. **Add specific files to staging**  
   ```bash
   git add <file-name>
   ```
3. **Add all changes to staging**  
   ```bash
   git add .
   ```
4. **Unstage files (remove from staging)**  
   ```bash
   git reset <file-name>
   ```
5. **Commit changes with a message**  
   ```bash
   git commit -m "Your commit message"
   ```
6. **Amend the last commit**  
   ```bash
   git commit --amend
   ```

---

### **Branching**
1. **List all branches**  
   ```bash
   git branch
   ```
2. **Create a new branch**  
   ```bash
   git branch <branch-name>
   ```
3. **Switch to a branch**  
   ```bash
   git checkout <branch-name>
   ```
4. **Create and switch to a new branch**  
   ```bash
   git checkout -b <branch-name>
   ```
5. **Delete a branch**  
   ```bash
   git branch -d <branch-name>
   ```
6. **Delete a branch (force)**  
   ```bash
   git branch -D <branch-name>
   ```

---

### **Pushing and Pulling**
1. **Push changes to a remote repository**  
   ```bash
   git push origin <branch-name>
   ```
2. **Pull changes from a remote repository**  
   ```bash
   git pull origin <branch-name>
   ```
3. **Push all branches**  
   ```bash
   git push --all
   ```

---

### **Working with Remotes**
1. **Add a remote repository**  
   ```bash
   git remote add origin <repository-url>
   ```
2. **View remote repositories**  
   ```bash
   git remote -v
   ```
3. **Remove a remote repository**  
   ```bash
   git remote remove <name>
   ```

---

### **Merging and Rebasing**
1. **Merge a branch into the current branch**  
   ```bash
   git merge <branch-name>
   ```
2. **Rebase the current branch onto another**  
   ```bash
   git rebase <branch-name>
   ```
3. **Abort a rebase**  
   ```bash
   git rebase --abort
   ```

---

### **Stashing**
1. **Stash changes**  
   ```bash
   git stash
   ```
2. **Apply the latest stash**  
   ```bash
   git stash apply
   ```
3. **View stash list**  
   ```bash
   git stash list
   ```
4. **Drop the latest stash**  
   ```bash
   git stash drop
   ```

---

### **Logs and History**
1. **View commit history**  
   ```bash
   git log
   ```
2. **View a summary of commit history**  
   ```bash
   git log --oneline
   ```
3. **View changes in a commit**  
   ```bash
   git show <commit-id>
   ```

---

### **Tagging**
1. **Create a new tag**  
   ```bash
   git tag <tag-name>
   ```
2. **Push tags to remote**  
   ```bash
   git push origin --tags
   ```
3. **Delete a tag locally**  
   ```bash
   git tag -d <tag-name>
   ```
4. **Delete a tag remotely**  
   ```bash
   git push origin --delete <tag-name>
   ```

---

### **Undo Changes**
1. **Revert a specific commit**  
   ```bash
   git revert <commit-id>
   ```
2. **Reset to a specific commit (soft reset)**  
   ```bash
   git reset --soft <commit-id>
   ```
3. **Reset to a specific commit (hard reset)**  
   ```bash
   git reset --hard <commit-id>
   ```

---

### **GitHub-Specific Commands**
1. **Fork a repository** (done via GitHub UI)  
2. **Create a pull request** (done via GitHub UI)  
3. **Fetch and merge pull requests locally**  
   ```bash
   git fetch origin pull/<PR-number>/head:<local-branch-name>
   git checkout <local-branch-name>
   ```
4. **View remote pull requests**  
   ```bash
   git ls-remote origin
   ```

---

### **Additional Commands**
1. **View a file’s history**  
   ```bash
   git log -p <file-name>
   ```
2. **Blame a file**  
   ```bash
   git blame <file-name>
   ```

---

If you’re new to Git, start with the basic commands like `clone`, `add`, `commit`, `push`, and `pull`. You can explore advanced commands as you become more comfortable! Let me know if you need help with any specific command.
