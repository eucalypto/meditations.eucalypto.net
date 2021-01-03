# meditations.eucalypto.net
"Meditations (by Eucalypto) blog" 


## Setup 

### Branches

This repository has two important branches
 - main
 - public-html

The `main` branch is the development branch with the source files for Hugo to make html from. Hugo generates the static site files in the `public` folder.

The `public-html` branch tracks those generated static files.

So it makes sense to check out this branch in the `public` folder. Git can do it with `git worktree`:

```bash
git worktree add public public-html
```

After a change, I have to commit/push both the main and public-html branches. When it becomes too annoying, I'll automate this with a script.


### Themes as git submodules

The imported themes have their own git repository and their installation guide says to incude them as git submodules.

Installed themes are already in the `.gitmodules` file and when you clone this repo, you have to check out those with

```bash
git submodule update --init
```
