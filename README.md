# GIT-TEST

### First Configuration Step

Insert the following commands on bash/zsh

```shell
git config --global user.name "[Enter GitHub username]"
git config --global user.email "[Enter GitHub user e-mail address]"
```

### Adding a new SSH Key to your GitHub Account
```shell
ssh-keygen -t ed25519 -C "[Enter e-mail address here]"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

### To verify for existing SSH Keys
```shell
cat ~/.ssh/id_ed25519.pub
```

NOTE: you are using a legacy system that doesn't support the Ed25519 algorithm, use this command instead:

```shell
ssh-keygen -t rsa -b 4096 -C "[Enter e-mail address here]"
```

### To create a new repository
```shell
echo "# GIT-TEST" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:bjorncfoss/GIT-TEST.git
git push -u origin main
```

### To push an existing repository
```shell
git remote add origin git@github.com:bjorncfoss/GIT-TEST.git
git branch -M main
git push -u origin main
```
