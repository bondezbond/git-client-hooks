## git-client-hooks

Git hooks to help keep good git standards

### Usage

1. Clone repo
2. `git config --global core.hooksPath ~/path/to/repo/git-client-hooks`


### Scripts

There are two scripts that help keep commit messages clean. Our formats are

`([US0000000] or [DE000000] or [NOCARD]) - commit messages description`

1. [commit-msg](./commit-msg) - this hook makes sure you follow the commit regex pattern
2. [prepare-commit-msg](./prepare-commit-msg) - this hook makes making commit messages easier when working with branches.

Let's say your working on feature `[US123456]`. You create a branch `US123456` and do your work. When you commit you can just commit `git commit -m 'my changes'`. The pre-commit-msg hook will take the branch name and pre-fix your messages like so `[US123456] - my changes`