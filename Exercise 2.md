## 📝 Homework Exercises – Version Control (Git & GitHub)

### 📌 Exercise 1: Install & Initialize

**Objective:** Set up Git on your local machine.

- Install Git if not already installed.
- Run `git --version` to verify installation.
- Create a new folder, navigate to it in your terminal.
- Initialize a Git repository using `git init`.

cd "Folder Name"
$ git --version
git version 2.49.0.windows.1

---

### 📌 Exercise 2: First Commit

**Objective:** Practice basic commands.

- Create a new file called `hello.txt` and add some content.
- Run `git status` to see changes.
- Add the file using `git add hello.txt`
- Commit it using `git commit -m "Initial commit with hello.txt"`

1- git status

On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Exercise 2.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        hello.txt

no changes added to commit (use "git add" and/or "git commit -a")

2- git add hello.txt
3- git status

On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   hello.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Exercise 2.md

4- git commit -m "Initial commit with hello.txt"

[main 1f81f03] Initial commit with hello.txt
 1 file changed, 1 insertion(+)
 create mode 100644 hello.txt
---

### 📌 Exercise 3: Using .gitignore

**Objective:** Learn how to ignore files.

- Create a folder called `temp` and a file `notes.log`.
- Add `temp/` and `*.log` to a `.gitignore` file.
- Run `git status` and make sure Git ignores these files.

---

### 📌 Exercise 4: Branching and Merging

**Objective:** Understand feature branching.

- Create a new branch: `git checkout -b feature-readme`
- Add a `README.md` file and commit it.
- Switch back to `main` and merge the new branch: `git merge feature-readme`
- Handle any merge conflicts if they occur.

Solution can be found in the remote Repo
---

### 📌 Exercise 5: Connect to GitHub

**Objective:** Push code to a remote repository.

- Create a new repository on GitHub.
- Link it to your local repo:

  ```bash
  git remote add origin https://github.com/your-username/your-repo.git
  git push -u origin main
  ```

Solution can be found in the remote Repo
---

### 📌 Exercise 6: Pull Requests Simulation

**Objective:** Simulate team collaboration.

- Pair up with a classmate.
- Create a new repo.
- You Both Clone it, make a change, push it, then open a Pull Request.
- Review and approve each other's PR.

---

### 📌 Exercise 7: Commit Message Practice

**Objective:** Write meaningful commit messages.

- Make 3 small changes to your code/files.
- For each, write a commit message using this format:

  ```
  [Type] Short description

  - What changed?
  - Why it was necessary?
  ```

  Example:

  ```
  [Fix] Correct typo in README

  - Fixed spelling of "installation" in README.md.
  - Improves professionalism and clarity.
  ```

1- git commit -m "Solved Exercise 1.md"
2- git commit -m "Solved Exercise 1 in Exercise 2.md"
3- git commit -m "Solved Exercise 2 in Exercise 2.md"
---

**💬 Bonus Challenge:** Create a `.bash_aliases` or `.zshrc` file to define aliases for common Git commands like `gs` for `git status`, `gc` for `git commit`, etc.

Happy Coding! 🚀
