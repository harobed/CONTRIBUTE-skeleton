# How to contribute to [ProjectName]

- Follow [GitFlow branching model](https://nvie.com/posts/a-successful-git-branching-model/)
- Follow [Standard Go Project Layout](https://github.com/golang-standards/project-layout)

## Follow GitLab Workflow

- First create one Issue
- Next Create « Work in Progress » Merge Request
- Enter in Code, Test and Review cycle
- When code review is ok, push to `develop` branch
- When the integration tests are ok, push to `staging`
- When tests are ok in `staging` push to `master` to auto deploy

More information: [« GitLab Workflow: An Overview »](https://about.gitlab.com/2016/10/25/gitlab-workflow-an-overview/)

## Git workflow

- [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/) ([comments](https://news.ycombinator.com/item?id=13889155)), extract:

  A properly formed Git commit subject line should always be able to complete the following sentence:

  - If applied, this commit will your subject line here

  For example:

  - If applied, this commit will **refactor subsystem X for readability**
  - If applied, this commit will **update getting started documentation**
  - If applied, this commit will **remove deprecated methods**
  - If applied, this commit will **release version 1.0.0**
  - If applied, this commit will **merge pull request #123 from user/branch**

  Notice how this doesn’t work for the other non-imperative forms:

  - If applied, this commit will **fixed bug with Y**
  - If applied, this commit will **changing behavior of X**
  - If applied, this commit will **more fixes for broken stuff**
  - If applied, this commit will **sweet new API methods**
- Use Git Pull Rebase:
  - Why use Git Rebase?: [« Git Merge vs. Rebase: What’s the Diff? »](https://hackernoon.com/git-merge-vs-rebase-whats-the-diff-76413c117333)
  - From Git Pro book:
    - [« Git Branching - Rebasing »](https://git-scm.com/book/en/v2/Git-Branching-Rebasing)
    - [« Git Tools - Rewriting History »](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History),
  - you can make `git pull -r` the default behaviour:
  ```
  git config --global pull.rebase true
  ```
- Write [Atomic Commits](https://seesparkbox.com/foundry/atomic_commits_with_git)


## Editor configuration

Python:

- Use [Black](https://github.com/ambv/black) to format Python code.
- Use [flake8](https://pypi.org/project/flake8/) for Linter

Golang:

- Use [goimports](https://godoc.org/golang.org/x/tools/cmd/goimports) (more [maintained](https://go.libhunt.com/compare-goreturns-vs-tools) than goreturns)

Bash:

- Use a linter [shellcheck](https://www.shellcheck.net/)

If you use [VSCode editor](https://code.visualstudio.com/):

- Install [https://github.com/Microsoft/vscode-go](https://github.com/Microsoft/vscode-go).
- Set project Workspace settings: copy [`vscode/settings.json`](vscode/settings.json) content in `.vscode/settings.json` file at root in your projet repository.

If you use [Atom editor](https://atom.io/):

- Install [linter-flake8](https://atom.io/packages/linter-flake8)
- Install [python-black](https://atom.io/packages/python-black)
- Install [atomenv package](https://atom.io/packages/atomenv).<br />
  After installation, execute `atomenv: Load` command in Atom editor to load good GOLANG variable environment (from [`/.atomenv.cson`](.atomenv.cson))


## Misc

- Avoid as far as possible to use acronyms or code name. See why here: [Acronyms Seriously Suck - Elon Musk](https://gist.github.com/klaaspieter/12cd68f54bb71a3940eae5cdd4ea1764)
