# Commands used

## New origin
```
git remote remove origin
git remote add origin git@github.com:holmmi/metropolia-git-intro.git
git branch -M main
git push -u origin main
```

## Pushing to origin
```
git status
git add .
git commit -m "Add notes.md"
git push
```

## Merge conflict
Editing the same file `index.html` on branches `dev` and `main`. Then merging `dev` into `main`. On branch `main`:
```
git merge dev
git checkout --theirs index.html
git add .
git commit
```
Now the merge conflict in `index.html` is resolved. Changes made on branch `dev` are applied in `main`. `main` branch changes could have been kept with command `git checkout --ours index.html`. Alternatively the `index.html` could have been edited to something else so that the code executes.