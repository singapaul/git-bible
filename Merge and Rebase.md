# Whats the difference?

- A merge will cram all the changes into the new branch.
- A rebase will add the new branch to the end of the main branch.

- We merge branches during a pull request.

If we are in the main branch and we want to merge a branch into it we can type

```
git merge test-branch
```

For a rebase

from a test branch, we do git commit, git add, commit. Then we go back to the master branch. and run the below command.
It will add the new branch to the master branch. git status will show us the result of this.
This is all rare though.

```
git rebase test-branch.
```

## reducing commits

Typical with jenkins pipelines. Sometimes we write too many commits and we want to reduce them before we commit to main.
In this case we want to run a rebase.

1. go to terminal, switch to test branch.
2. run the below command - 4 chosen as goes back latest 4 commits.

```
git rebase -i HEAD~4
```

3. We tell git to merge the last three changes and merge into one commit. Delete pick and replace with s. Swap comment for r. Work using VIM.
4. To exit VIM esc, :wq

---

# Merge Conflicts

If you have two branches which have different changes on the same line.

# Git Pull / Fetch

When people change the main, we want to pull the commits, we can either run

```
git fetch
git pull
```

Take home - before you start work, do a git pull.

# Forking

Let's us take a remote repository and create our own. 
