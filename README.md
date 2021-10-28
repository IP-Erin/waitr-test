# waitr-test

WIP test automation, from soup to nuts.

## Getting Started

These instructions assume you're using a recent MacOSX. 

### Install nvm and node

See official nvm [Install & Update Script Steps](https://github.com/nvm-sh/nvm/blob/master/README.md#installing-and-updating)

<details>
  <summary><em>Basic nvm installation steps</em></summary>

Creates .zshrc file if one is not already present

```sh
touch ~/.zshrc
```

Request and run nvm install script

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | zsh
```

Export nvm configs

```sh
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
```

After editing your shell's rc file, either restart your terminal session, or re-source the rc file, e.g.

```sh
source ~/.zshrc
```

Verify nvm is installed by outputting the version

```sh
nvm -v
```

</details>

If you haven't already, clone this repository locally:

```sh
git clone git@github.com:IP-Erin/waitr-test.git; cd waitr-test
```
### Setup Visual Studio Code

1. Download and install [VSCode](https://code.visualstudio.com/)
1. Open the cloned repository
1. Install **Workspace Recommended** Extensions

## Running tests - TO DO

Required Variables: TO DO
Optional Variables: TO DO

## Architectual Landmarks - TO DO

## Other Tooling

### [ESLint](https://eslint.org/) (Code Quality Linter)

```sh
npx eslint . # Check code quality of all files
```

### [Prettier](https://prettier.io/) (Code Style Linter)

_Note: Format-on-save is setup during [VSCode Setup](#setup-visual-studio-code) and can be disabled (Settings -> Format On Save)_

```sh
npx prettier --check . # Check code style of all files
npx prettier --write . # Check and update code style of all files
```

### [Lefthook](https://github.com/evilmartians/lefthook) (Git Hook Manager) - usage tbd

Git hooks will run on their own, below is special case manual usage:

```sh
npx lefthook run pre-commit # Manually trigger the pre-commit hook group
LEFTHOOK=0 git commit -m "Commit message" # LEFTHOOK=0 skips git hooks
```
