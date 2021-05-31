## How to create a PR

 1. Branch name
  - `feature-blah` or `add-blah` for features
  - `fix-blah` for bug fix
  - Note that our CI does not pick up branches with names starting with "feature/", "fix/" etc (anything with a slash in it). Lets not use this naming pattern for our branches. lets separate words in branch names with a hyphen.
 2. PR message
  - Please write down a brief of PR changes, so that reviewer can understand what the PR is about easily.
  - Attach front-end screenshots if there's any front-end changes.
  - Write down migration script in the PR message if any.
 3. After PR is created
  - Attach the PR to Trello card

## How to resolve merge conflicts

We don’t normally use the merging mechanism because of how our releases work. We rebase.
Merging basically pulls the master branch commits to the current branch and then you can resolve the conflicts in a “merge commit”.

The problem is that it’s difficult to cherry-pick these merge commits.
Rebasing places your commits on the top of the lastest master.

```
git checkout master
git pull
git checkout <your branch>
git rebase master
```
While rebasing, some commits that result in conflict will pause for you to resolve them. You can follow the instructions in console. 
