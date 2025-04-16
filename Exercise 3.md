## 📝 Homework Exercises – Git Recovery & Advanced Operations

### 📌 Exercise 8: Soft Reset Practice

**Objective:** Learn how to undo commits while keeping your changes.

- Create three commits with different files.
- Use `git log` to view the history.
- Run:
  
  git reset --soft HEAD~2
  
  to undo the last two commits but keep the changes staged.
- Recommit with improved messages.
- Verify the new log with `git log`.

///////////////////////////////

1- git add "file 1.txt"
2- git commit -m "Created file 1.txt"
3- git add "file 2.txt"
4- git commit -m "Created file 2.txt"
5- git add "file 3.txt"
6- git commit -m "Created file 3.txt"
7 - git log --oneline

0fb8030 (HEAD -> main) Created file 3.txt
d6523cf Created file 2.txt
2ad9de0 Created file 1.txt
48d5cb2 (origin/main, origin/HEAD) 1-Ignore all files in folder temp/ 2- ignore all files with extension .log

8-git reset --soft Head~2

2ad9de0 (HEAD -> main) Created file 1.txt
48d5cb2 (origin/main, origin/HEAD) 1-Ignore all files in folder temp/ 2- ignore all files with extension .log

9- git commit -m "Created file 2.txt and file 3.txt in one commmit "
10- git log --oneline

7d47368 (HEAD -> main) Created file 2.txt and file 3.txt in one commmit
2ad9de0 Created file 1.txt
48d5cb2 (origin/main, origin/HEAD) 1-Ignore all files in folder temp/ 2- ignore all files with extension .log
---

### 📌 Exercise 9: Revert Simulation

**Objective:** Undo a commit safely without rewriting history.

- Make a change and commit it with a message like `"Break layout"`.
- Run `git log` and copy the commit hash.
- Run:
  
  git revert <commit-hash>
  
  to create a new commit that undoes the previous one.
- Confirm the result using `git log` and check your files.

/////////////////////////////////
1-git add "file 1.txt"
2-git commit -m "Break layout"
3- git log --oneline

559ed64 (HEAD -> main) Break layout
7d47368 Created file 2.txt and file 3.txt in one commmit
2ad9de0 Created file 1.txt

4- git revert 559ed64
5- git log --oneline

7617f13 (HEAD -> main) Revert "Break layout"
559ed64 Break layout
7d47368 Created file 2.txt and file 3.txt in one commmit
2ad9de0 Created file 1.txt

---

### 📌 Exercise 10: Stash Use Case

**Objective:** Temporarily save uncommitted work.

- Edit two files without committing.
- Run:
  
  git stash
  
- Switch to another branch using `git checkout`.
- After switching back, run:
  
  git stash pop
  
- Run `git status` before and after stashing to observe changes.

////////////////////////

1- git stash
2- git checkout -b feature/stash
3- git stash pop

On branch feature/stash
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   file 2.txt
        modified:   file 3.txt

4-git status

On branch feature/stash
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   file 2.txt
        modified:   file 3.txt

5-git add "file 2.txt"
6-git add "file 3.txt"
7-git commit -m "stash poped"
8-git push origin feature/stash
---

### 📌 Exercise 11: Cherry-Pick Challenge

**Objective:** Apply a commit from one branch to another.

- Create a new branch `feature-a` and commit a change.
- Switch to `main` and run:
  
  git cherry-pick <commit-hash>
  
- Use:
  
  git log --oneline
  
  to confirm the commit appears on both branches.

  ///////////////////////////////////////

1-git checkout -b feature-a
2-git add "cherry-pick.txt"
3-git commit -m "feature-a made this change"
4-git log --oneline

b0235a1 (HEAD -> feature-a) feature-a made this change
d931936 (origin/main, origin/HEAD, main) Merge pull request #4 from AmrBadran95/E6-collab\

5-git checkout main
6-git cherry-pick b0235a1
7-git log --oneline

0e5263e (HEAD -> main) feature-a made this change
d931936 (origin/main, origin/HEAD) Merge pull request #4 from AmrBadran95/E6-collab

### ✅ Submission Guidelines

- Create a GitHub repo named `git-homework`
- Push all your exercises there.
- Submit the repo link before [21/04/2025].
