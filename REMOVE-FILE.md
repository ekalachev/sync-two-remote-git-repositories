# Remove sensitive files and their commits from Git history

```cmd
git filter-branch --force --index-filter "git rm --cached --ignore-unmatch PATH-TO-YOUR-FILE-WITH-SENSITIVE-DATA" --prune-empty --tag-name-filter cat -- --all
```

```cmd
git push --force --verbose --dry-run
```

```cmd
git push --force
```

> Keep in mind that once you've pushed this code to a remote repository like GitHub and others have cloned that remote repository, you're now in a situation where you're rewriting history. When others try pull down your latest changes after this, they'll get a message indicating that the changes can't be applied because it's not a fast-forward.
