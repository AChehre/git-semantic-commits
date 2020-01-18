# Semantic Git commit messages

Inspired by Sparkbox's awesome article on [semantic commit messages](http://seesparkbox.com/foundry/semantic_commit_messages).

## What is this?
These are **very simple** custom git commands that enforce the git user to write better git commit messages. If still confused, read the article above.

## Installation:

1. Clone this repo, preferably in your $HOME directory. ```git clone https://github.com/AChehre/git-semantic-commits ~/.git-semantic-commits```

  Tip: If you're using Cygwin, open it and type 'echo $USERPROFILE'. This will show you the location of the $HOME directory.

2. Install it as a set of bash scripts or git aliases:
  * bash scripts: ```./install.sh --scripts```
  * git aliases ```./install.sh```

  Tip: Installation script is idempotent and could be harmlessly executed multiple times. It adds bash scripts to the PATH in your `~/.bashrc` or `~/.zshrc` files or adds git aliases to the `~/.gitconfig` file respectively (without any duplication).

3. Commit away!

## Usage

New command -> what it does:

* ```git feat "A new feature"``` -> ```git commit -m 'feat: A new feature'```
* ```git docs "Documentation only changes"``` -> ```git commit -m 'docs: Documentation only changes'```
* ```git chore "updating gulp tasks etc."``` -> ```git commit -m 'chore: updating gulp tasks etc.'```
* ```git fix "A bug fix"``` -> ```git commit -m 'fix: A bug fix'```
* ```git refactor "A code change that neither fixes a bug nor adds a feature"``` -> ```git commit -m 'refactor: A code change that neither fixes a bug nor adds a feature'```
* ```git style "Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)"``` -> ```git commit -m 'style: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)'```
* ```git test "Adding missing tests or correcting existing tests"``` -> ```git commit -m 'test: Adding missing tests or correcting existing tests'```
* ```git localize "commit message here"``` -> ```git commit -m 'localize: commit message here'```
* ```git ci "Changes to our CI configuration files and scripts (example scopes: Circle, BrowserStack, SauceLabs)"``` -> ```git commit -m 'ci: Changes to our CI configuration files and scripts (example scopes: Circle, BrowserStack, SauceLabs)'```
* ```git vendor "update version for dependencies, packages"``` -> ```git commit -m 'vendor: update version for dependencies, packages'```
* ```git build "Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)"``` -> ```git commit -m 'build: Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)'```
* ```git perf "A code change that improves performance"``` -> ```git commit -m 'perf: A code change that improves performance'```

If you would like to add an optional scope, as described [here](https://conventionalcommits.org/), use the '-s' flag and quote the scope message:

* ```git docs -s "scope here" "commit message here"``` -> ```git commit -m 'docs(scope here): commit message here'```

If you would still like to use your text editor for your commit messages
you can omit the message, and do your commit message in your editor.

* ```git feat``` -> ```git commit -m 'feat: ' -e```

Aliases for those who use [git-extras](https://github.com/tj/git-extras) (will be installed only if you have `git-extras`):

* ```git rf "commit message here"``` -> ```git commit -m 'refactor: commit message here'```
* ```git ch "commit message here"``` -> ```git commit -m 'chore: commit message here'```


----
This document forked from https://github.com/fteem/git-semantic-commits
