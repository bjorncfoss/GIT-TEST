# GIT-TEST

* GIT Testing Repository.

### To create a new repository

```sh
echo "# GIT-TEST" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:bjorncfoss/GIT-TEST.git
git push -u origin main
```

### To push an existing repository

```sh
git remote add origin git@github.com:bjorncfoss/GIT-TEST.git
git branch -M main
git push -u origin main
```