# git-hooks-experiment

## Restrict specific branches to be merged into any other branch 

### Step 1:                    
Create a symlink like from your project root like 

`ln -s -f ../../git-hooks/prepare-commit-msg.sh .git/hooks/prepare-commit-msg`

The name of the file *must* be "prepare-commit-msg" for Git to pick it up.

`OR` 

For `git >= 2.9` you can use `git config core.hooksPath git-hooks`

### Step 2:
Make sure it is executable. `chmod +x .git-hooks/prepare-commit-msg.sh`

### Step 3:
Disable Fast Forward Merges : `git config branch.master.mergeoptions "--no-ff"`
