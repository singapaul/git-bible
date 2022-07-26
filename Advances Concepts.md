# Roll backs

How to roll back. We might want to roll back or roll forward after a certain amount of commits to a branch.

to see out history of commits we run

```
git log
git log --pretty=format:pretty-print commits
```

The HEAD in the terminal will tell us which commit were are on.
We can copy the hash code and write

```
git revert HASHCODE
```

This will create a conflict -> We have to accept the incoming changes.

To accept and save these changes we then add, commit and push the commit.

## Detached head mode

```
git checkout HASHCODE
```

Will enter detached head mode. To go back we do git checkout branchName which will return us with the head in the right place.

### Time saving hack

On githiub you can search the repository for the exact commit/release in the top left corner of the screen. We can then search for the identities of the committers to speak to them to troubleshoot. 

### Git Blame
On the github website, we can view the history of the commit, and see who wrote the single line and what commit it came in when trouble shooting.

### Git Ignore

Create a file in the repository called ".gitignore". This file tells git what to ignore based on what we specify by name.

type 
- .foldername
- *.name will ignore any file which has that name.