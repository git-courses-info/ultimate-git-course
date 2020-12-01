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
