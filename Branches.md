# Branches

Allows you you create your own stream of work. 

```
git branch -> will show the current branch
```

To create a new branch we can type

```
git checkout -b newBranchName
```

to switch to a different branch you can use the following

```
git checkout branchName
```

to see all the difference branches and their status we can  use the following.

```
ls -al
```

When we make a new branch locally, in order to push it to github we need to tell GIT which branch we will push to. So when on the branch we can type. git push won't work. We need to wrie

```
git push --set-upstream origin *branchName*
```
We can create new branches from any of these branches, we don't have to create a branch from main. But we most likely want to.


## Branching strategies

There are two main ones 

### Trunk flow

Everything is done on the master branch. Good for small organizations but not for large organizations. 
 - Feature
 - Bug Fix
 - Release branches

 It doesn't scale particularly well. 


### Git Flow

Arguably the best way to work with Git. Two main branches. 

- Master
- Develop

All the work should be done on the develop branch. Feature requests get done off the develop branch. Releases get released and merged into the master branch. The idea is that only release level code goes into the master branch. Therefore the master branch can be used as a snapshot of releases over time and doesn't contain insignificant merges. Whilst development is always in a state of flux. Because develop is always in a state of flux, we have to ensure we do squashing on the master branch (Github does this for us)

