# ultimate-git-course

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
