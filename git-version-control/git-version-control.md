# GIT VERSION CONTROL

---

# commands:
```bash
   $ git status
```
* shows the current status of staging
  * tracked => files that have been added to version control
  * staged => files/changes that have been added and ready to be committed
* [git status](https://git-scm.com/docs/git-status)
---

```bash
  $ git add 
```
* stages a file for commit
```bash
  $ git add -p 
```
* -p flag allows user to move through changes and choose to add them or not
  * 'y' will stage the changes
  * 'n' will skip the changes
* [git add](https://git-scm.com/docs/git-add)
---

```bash
  $ git commit 
```
* creates snapshot of code that can be pushed
* allows you to save code to your version control
* will open text file for commit message
  * top line of file is subject
    * brief tagline of what the commit contains
  * empty line separates subject from body
  * body is after empty line
    * contains a detailed description of changes
* [git commit](https://git-scm.com/docs/git-commit)
---

```bash
  $ git push xyz abc
```
* saves changes to remote repo names xyz and branch named abc and makes a pull request if necessary
* [git push](https://git-scm.com/docs/git-push)
    
```bash
  $ git branch
```
* lists all branches 


```bash
  $ git branch xyz
```
* creates a branch names 'xyz'
* [git branch](https://git-scm.com/docs/git-branch)
---

```bash
  $ git merge xyz 
```
* brings in changes from the xyz branch into the current branch
* [git merge](https://git-scm.com/docs/git-merge)
---

```bash
  $ git rebase xyz 
```
* moves changes in current branch to front of xyz branch
* [git rebase](https://git-scm.com/docs/git-rebase)
---

```bash
  $ git diff xyz
```
* shows unstages changes to the file named xyz
* [git diff](https://git-scm.com/docs/git-diff)
---

```bash
  $ git checkout xyz
```
* moves to the branch named xyz
* [git checkout](https://git-scm.com/docs/git-checkout)
---

```bash
  $ git clone xyz
```
* creates a local copy of xyz repository
* [git clone](https://git-scm.com/docs/git-clone)
---

```bash
  $ git rebase xyz
```
* makes xyz branch the ancestor of current branch
* [git rebase](https://git-scm.com/docs/git-rebase)
---

```bash
  $ git cherry-pick commithash
```
* brings in changes from a specific commit
* [git cherry-pick](https://git-scm.com/docs/git-cherry-pick)
---

```bash
  $ git log
```
* shows commit history 
* press 'q' to quit out of git log
* [git log](https://git-scm.com/docs/git-log)



# branching workflow:
### strategies/methodologies
* **"always be integrating"**
  * only have a small number of branches at a single time
  * keep commits small 
  * requires a strong QA team
* **"start, release, feature"**
  * have different forms of branches
    * e.g. main vs dev vs feature
---
### long running branch vs short running branch
* **long-running** 
  * not intended to be deleted 
  * usually contains short-running branches
  * e.g. main or dev
* **short-running**
  * has an anticipated termination point
  * exists to be integrated and then deleted
  * e.g. feature branch
---
  
# pull requests
### overview
* a feature of hosting platforms (github)
* designed for when a user who doesn't have direct write access wants to make changes
* allows user with write access to view changes and pull them in if desired
---
### forking
* allows user to create personal remote copy of another remote repo
---
### cloning
* allows user to create a local copy of a remote repo
  * established remote and local connection
    * user can then make push to the remote repo
---
```bash
  $ git push -u origin xyz 
```
* creates a remote repository named xyz
* establishes remote and local connection
* pushes changes to newly created remote repo
---
# merge
### overview
* when two unique branches are combined
* looks to common ancestor and most common ancestor shared by both branches
* it combines the changes from each branch from the common ancestor and makes a new common ancestor
* does not change commit history
* [official documentation](https://git-scm.com/docs/git-merge)
![git merge](https://wac-cdn.atlassian.com/dam/jcr:4639eeb8-e417-434a-a3f8-a972277fc66a/02%20Merging%20main%20into%20the%20feature%20branh.svg?cdnVersion=140)

---
### merge conflict
* occurs when local branch tries to push changes but is missing changes from remote branch
* requires user to resolve conflicts before pushing
  * user will pick and choose changes from each branch and then make a new commit after choosing desired changes to keep
---
  
# rebase
### overview
* attempts to move all commits after current ancestor to the front of the branch being rebased from
* changes git history to look as if the front of the rebased branch was the common ancestor
* NEVER rebase commits that have already been pushed or else git history issues
* [official documentation](https://git-scm.com/docs/git-rebase)
![git rebase](https://wac-cdn.atlassian.com/dam/jcr:2908e0e6-f74b-4425-b5d2-f5eca8cfcd99/05%20Rebasing%20the%20main%20branch.svg?cdnVersion=140)
---
# cherry-pick
### overview
* allows user to bring in changes from any commit (not just most recent)
* automatically makes a commit after choosing to cherry-pick
  * use -n flag to avoid auto commit
* [official documentation](https://git-scm.com/docs/git-cherry-pick)
# resources
### [GitHub's git Documentation](https://docs.github.com/en/get-started/using-git)
### [Atlassian's tutorials](https://www.atlassian.com/git/tutorials)
### [Official Documentation](https://git-scm.com/docs)