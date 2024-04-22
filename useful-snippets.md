# Useful Snippets

## Anaconda/Mamba

To create the environment from the `environment.yml` file:

```bash
mamba env create -f environment.yml
```

To export the environment changes in an OS-agnostic form:

```bash
mamba env export --from-history > environment.yml
```

## Using Git

Git works by tracking your changes locally (i.e. on your computer). You can then `push` your changes to GitHub so they are stored online, and others can access them.
Here's a brief rundown of how to push

```bash
# First `cd` into the git repository
git add .  # This will add all your changes to be tracked by git. Your changes are only "ready" to be recorded to the tree of changes. Committing will actually do the recording.
git status  # This allows you to see what is currently ready for git to `commit`. What's in green is ready, what's in red still needs to be added (i.e. with `git add .)
git commit -m "YOUR MESSAGE"  # This officially records your changes. Insert a message based on what you've changed so far.
# Now the changes are locally recorded. 

git push  # This will update GitHub to have your most recent changes.
```

Sometimes, if there's changes github has that you don't have locally, Github will reject your push and ask you to merge.
You can try the following below
```bash
git pull  # This will try to update your local git repository to have the changes on GitHub

# The pull might fail, which means you'll need to do a merge.
git merge origin/master  # git merge will try to merge your current branch with whatever branch name you give it. The origin/... refers to whatever the copy of the branch is on the remote (i.e. Github). So this command says merge my current branch with Github's copy of the master branch.
```
Once you've tried merging, git may ask you to decide what you want to merge then commit the new changes. In this situation, you'll want to look through the files it lists
and see if they look good as they are. If it says there are conflicts, then git will insert snippets into the file showing the two options you have between the conflicts. You'll have to manually edit the file (or you could use VSCode to do it more easily) to decide what to keep. Once you've done that, do the add, commit, push like you did before.