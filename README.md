### 1. Initialize a Local Git Repository
•⁠  ⁠Create a local Git repository on your machine.
•⁠  ⁠Add an initial file (initial.txt) with some content and commit it to the main branch.
 Stage a second file (temp.txt) but unstage it using git restore --staged temp.txt. Then, modify temp.txt, stage it again, and unstage it using git reset HEAD temp.txt. 

### 2. Remote Repository Operations
•⁠  ⁠Create a remote repository on GitHub and link it to your local repository.
•⁠  ⁠Push the initial commit to the remote main branch.
•⁠  ⁠Make changes to initial.txt on the remote repository via the GitHub web interface (e.g., add a new line).
•⁠  ⁠Pull these changes to your local repository using git pull origin main.
=Stage multiple files locally (file1.txt, file2.txt), then unstage only file2.txt using git reset HEAD file2.txt. Commit file1.txt and push to the remote. 
Demonstrate the state of your working directory using git status after each operation.

### 3. Branching and Pull Request
•⁠  ⁠Create a branch g1 on the remote repository via GitHub.
•⁠  ⁠Clone or fetch the g1 branch locally using git fetch origin and git checkout g1.
•⁠  ⁠Add a new text file (g1_file.txt) on the g1 branch, commit, and push to the remote.
•⁠  ⁠Raise a pull request (PR) from g1 to main on GitHub. Merge the PR without conflicts.


### 4. Local Git Operations
Perform the following on your local repository:
•⁠  ⁠Get Updated Files: Run git fetch origin and git merge origin/main to ensure your local main branch is up-to-date.
•⁠  ⁠Reset Operations:
  - Create a commit on main with changes to initial.txt.
  - Perform a soft reset using git reset --soft HEAD~1 to keep changes in the working directory.
  - Stage and commit only part of the changes using git add -p (interactive staging).
  - Perform a hard reset on a new commit using git reset --hard HEAD~1 and demonstrate the loss of changes using git status and git log.
•⁠  ⁠List Changes:
  - Use git diff main g1 to show differences between branches.
  - Use git ls-files and git status to list tracked and untracked files.
•⁠  ⁠Create Local Branches:
  - From main, create branch b1 and update initial.txt.
  - From b1, create branch b2 and add a new file (b2_file.txt).
  - From b2, create branch b3 and modify b2_file.txt.
On b3, stage multiple changes across files, then use git reset --mixed HEAD to unstage all changes. Selectively stage specific hunks using git add -p and commit. Show the differences using git diff --staged.

### 5. Branch Merging and Cleanup
•⁠  ⁠Merge b3 into b2, then b2 into b1, and finally b1 into main locally.
•⁠  ⁠Advanced Task: Introduce a merge conflict by modifying the same line in initial.txt on b3 and b2. Resolve the conflict manually during the merge and document the process.
•⁠  ⁠Delete the local branches (b1, b2, b3) using git branch -d.
•⁠  ⁠Delete the remote g1 branch using git push origin --delete g1.

### 6. Fork Operations
•⁠  ⁠Fork your own repository on GitHub to a new repository under your account.
•⁠  ⁠Clone the forked repository locally.
•⁠  ⁠Make a change in the forked repository (e.g., add forked.txt) and push to the forked remote.
•⁠  ⁠Create a PR from the forked repository to the original repository’s main branch.

### 7. Advanced Unstaging Challenge
•⁠  ⁠Create a complex scenario with multiple staged and unstaged changes:
  - Modify initial.txt, b2_file.txt, and add a new file challenge.txt.
  - Stage all changes using git add ..
  - Unstage challenge.txt using git reset HEAD challenge.txt.
  - Use git add -p to selectively stage specific lines in initial.txt.
  - Commit the staged changes and use git stash to save the remaining unstaged changes.
  - Pop the stash using git stash pop and demonstrate a conflict in the stash application. Resolve it manually and commit.
•⁠  ⁠Document the state of the repository after each step using git status and git diff.
Also, perform rm and revert operations

---

## Submission Requirements
•⁠  ⁠Provide screenshots of your terminal for each major step.
•⁠  ⁠Push all changes to the remote repository and provide the repository URL.
•⁠  ⁠Ensure the repository contains a README.md with a brief overview of the assignment and links to your PRs.
