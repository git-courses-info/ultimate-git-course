# ultimate-git-course

## 5. COLLABORATION

A course from codewithmosh.com

- `origin` is a reference to the cloned repo
- `origin/master` is a remote tracking branch

- git pull
  warning: Pulling without specifying how to reconcile divergent branches is
  discouraged. You can squelch this message by running one of the following
  commands sometime before your next pull:

  - git config pull.rebase false # merge (the default strategy)
  - git config pull.rebase true # rebase
  - git config pull.ff only # fast-forward only

### .9 Storing Credentials

- [Credential Storage](https://git-scm.com/book/en/v2/Git-Tools-Credential-Storage)
- [git-credential-cache](https://git-scm.com/docs/git-credential-cache) Helper to temporarily store passwords in memory  
   -`git config --global credential.helper cache`
- If you’re using a Mac, Git comes with an “osxkeychain” mode, which caches credentials in the secure keychain that’s attached to your system account. This method stores the credentials on disk, and they never expire, but they’re encrypted with the same system that stores HTTPS certificates and Safari auto-fills.
  - `git credential-osxkeychain`
  - `git config --global credential.helper osxkeychain`

### 10. Sharing tags

- By default git doesn't push our `tags` to our repo... So we `git push origin v1.0`
- To delete it: `git push origin --delete v1.0`
- Delete it on the local repo: `git tag -d v1.0`

### 11. Releases

- Use Releases to package your software, along with source code, binary files (e.g. compiled files of the app) and release notes.
- When you create a Release on github, it will be added to the latest commit.

### 12. Sharing Branches

- Similarly to tags, branches are local, private by default.
- Check if a branch has a remote tracking branch: `git branch -vv`

        * feature-1 11eb84c 11. Releases
        main      11eb84c [origin/main] 11. Releases

- Check for remote branches: `git branch -r`

        origin/HEAD -> origin/main
        origin/main

- So the first time you push a branch: `git push -u origin feature-1`
- To delete a branch in remote repo: `git push -d origin feature-1`
- To delete a branch in local repo: `git push -d feature-1`

### 13. Colaboration Workflow

- If you create a branch in the remote repo and then do `git fetch`, and then run `git branch`, you only see `main`,
  because when we run `fetch`, we only get the remote branch. So then we need to create a local one and map it to the remote one.
  - git switch -C feature-1 origin/feature-1
- Remove tracking branches that are deleted on the remote repo: `git remote prune origin`

<<<<<<< HEAD
...

### 18. Milestones

- We can add a banch of issues to a milestone, and then see the progress in that milestone.
=======
### 14. Pull Requests

- Pull requests let you tell others about changes you've pushed to a branch in a repository on GitHub. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add follow-up commits before your changes are merged into the base branch.
  - **Note: When working with pull requests, keep the following in mind:**
  - If you're working in the shared repository model, we recommend that you use a topic branch for your pull request. While you can send pull requests from any branch or commit, with a topic branch you can push follow-up commits if you need to update your proposed changes.
  - When pushing commits to a pull request, don't force push. Force pushing can corrupt your pull request.[docs](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/about-pull-requests).
- Pull requests display diffs to compare the changes you made in your topic branch against the base branch that you want to merge your changes into [docs](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/about-comparing-branches-in-pull-requests).
>>>>>>> bd7529f02fe2c9dd8e6c166b9ed3abf017b064b5
