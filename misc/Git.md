# Git workflow

## Steps to implement a change
1. Create an **issue** for the task.
2. Create a **branch** and a **merge request** from that issue - on the issue page, click `Create merge request`.
    - Stick to the autogenerated name format.
    - The base branch must *always* be master.
    - Optionally, mark the MR as work-in-progress by prefixing the name with `WIP:`
3. Checkout your branch locally, commit and push your changes. Keep commits as simple as possible.
4. If there are any merge conflicts, resolve them locally
    - `git checkout <your-branch>`
    - `git merge origin/master`
5. Make sure the pipeline on your MR is passing - merging changes with failing pipelines is not allowed.
6. Ask someone to do **code review** for your MR - assign them as a Reviewer.
7. When the reviewer accepts your changes, the pipeline is passing, and there are no conflicts, *merge* the MR.
    - Your changes will be applied to the master branch.
    - Delete the original branch (this keeps the repo clean).
    - Do not squash your commits - save the commit history.

## Additional notes
* The `master` branch is protected - pushing directly is not allowed. Changes to the master branch can only be made through a gitlab merge request.
* We're keeping the branching simple - a `master` branch and `feature/fix` branches that are merged right back to master. This is subject to change in the future.
* Try to keep feature branches as short as possible. Large merges are dangerous.
* Code merged to `master` should be *production-ready*.
* All of the actions above (creating a branch, creating a MR, merging...) are available through the GitLab web UI. The [glab](https://github.com/profclems/glab) CLI tool is also available and supports working with issues, merge requests etc. (things that are gitlab-specific) through an interface similar to `git`.