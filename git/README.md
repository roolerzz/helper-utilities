<h3>Git Helpers</h3>
Contains helper functions and notes for dealing with git.

<H4>Commands:</H4>

- `git remote -v`
- `git checkout -b "${{BRANCH_NAME}}"`
- `git checkout -- ${{FILE_NAME}}`
- `git checkout -- .`
- `git reset HEAD ${{FILE_NAME}}`
- `git reset HEAD .`
- // Soft Reset
- // Hard Reset
- `git pull`
- `git fetch`
- `git push --set-upstream=origin/${{REMOTE_BRANCH_NAME}} ${{LOCAL_BRANCH_NAME}}`
- `git rebase {{BRACH_NAME}}`
- `git add -p`
- `git commit --amend`

<H4>Aliases:</H4>


<H4>Issues due to unclean local Branch history With Conflicting Changes</H4>

- During Rebase, its getting difficult because multiple commits have overwritten changes and its difficult to remember which one you want. It would be great if the commits of the personal branch were squashed together so that re-basing is easier. 
- Need More details on this.
