# Github-Activity
# COMP301 Git Activity

Welcome to our collaborative Git exercise! In this activity, you will first work independently, then in pairs and teams, to practice branching, committing, resolving merge conflicts, and making pull requests.

---

## What You Will Learn

- Creating and pushing branches.  
- Making pull requests to a protected main branch.  
- Working in a team.  
- Organizing contributions from many people into one shared project.  

---

## (Required) Part 1: Individual Contribution (No Conflicts)

IntelliJ is not necessary for this activity, and it is meant to be done on the command line.  

(There are helpful commands at the bottom of the instructions)

1. Talk with your teammates and come up with a Team name.
2. Make a fork of this repository by clicking the "fork" button on the website.
3. Each member should clone the newly created repository to their computer.
4. You will need to set the upstream to point at the class COMP301-S26 repo.  There are a list of commands at the bottom of the instructions to help you do this.
5. Verify that the origin and remote are properly set by typing `git remote -v`.  Once you have verified that everything looks right, you are ready to begin.
6. Add all your team members as collaborators.  
7. You will see folders for the morning section and the afternoon section. Choose the appropriate folder to work in.  
8. Create a new branch named `team/<teamname>`.  
9. Now navigate to the `solo/` folder inside the Morning or Afternoon folder. Inside it, person 1 should create a new text file named `<onyen>.txt`.  
10. Add your full name inside the file.  
11. Stage, commit, and push your branch to your fork on GitHub.
12. The next person in the group should pull the repo, checkout the branch, and verify that they see the previous person's work.
13. Repeat steps 9-12 until all people in the team have created a file in the folder.  
14. Open a pull request **from your fork’s branch** to the **upstream repository’s `main`** with the title `team: <teamname>`.


Each student will have their own file, so there should be no conflicts in this step.    The pull request IS the submission for this assignment so make sure that you verify that you can see it in the pull requests tab on the website before leaving.  


---


## Quick Reference (Commands in Alphabetical Order)

- `git add <file>` — stage changes to be committed.  
- `git branch -vv` — show local branches and their remote tracking.  
- `git checkout -b <new-branch>` — create and switch to a new branch.  
- `git checkout <branch>` — switch to an existing branch.  
- `git clone <repo-url>` — clone the repository to your computer.  
- `git commit -m "<message>"` — commit staged changes with a message.  
- `git diff` — show unstaged changes.  
- `git diff --staged` — show staged but uncommitted changes.  
- `git fetch --all` — fetch all updates from remote branches.  
- `git log --oneline --graph --decorate --all` — visualize branch history.  
- `git merge <branch>` — merge another branch into your current branch.  
- `git merge --abort` — cancel a merge attempt.  
- `git pull --ff-only` — update your branch with the latest changes from remote.  
- `git push -u origin <branch>` — push your branch to GitHub and set upstream.  
- `git remote add upstream <url>` — add the class repo as upstream.  
- `git reset --hard origin/main` — reset your branch to match your fork’s main branch.  
- `git restore <file>` — discard changes to a file before staging.  

**Update local main from upstream:**
```bash
git checkout main
git fetch upstream
git merge --ff-only upstream/main
git push origin main
```

---

## Common Mistakes

1. **Confusing branch names with folder names.**  
Remember: `team/<teamname>` is the branch name; `solo/` is the folder. Both are required.

2. **Forgetting to pull the latest changes before branching or merging.**  
Always run `git pull --ff-only` on `main` or your base branch to avoid diverging histories.

3. **Leaving merge conflict markers in files.**  
Always remove `<<<<<<<`, `=======`, and `>>>>>>>`. 
---

## Extra Debugging Commands

- `git status` — check current branch and file state.  
- `git log` — view commit history.
- `git remote -v` - view current origin and remote urls.

---

**Setup remotes (run once per local clone):**
```bash
# already set automatically when you clone YOUR fork
git remote -v

# add the class repo as 'upstream'
git remote add upstream https://github.com/COMP301-S26/Github-Activity.git
git fetch upstream
```

**Keep your fork up to date (before new work):**
```bash
git checkout main
git fetch upstream
git merge --ff-only upstream/main
git push origin main
```
