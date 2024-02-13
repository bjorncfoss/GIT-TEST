# GIT-TEST

Another line added

### First Configuration Step

Insert the following commands on bash/zsh

```sh
git config --global user.name "[Enter GitHub username]"
git config --global user.email "[Enter GitHub user e-mail address]"
```

### Adding a new SSH Key to your GitHub Account
```sh
ssh-keygen -t ed25519 -C "[Enter e-mail address here]"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

### To verify for existing SSH Keys
```sh
cat ~/.ssh/id_ed25519.pub
```

NOTE: you are using a legacy system that doesn't support the Ed25519 algorithm, use this command instead:

```sh
ssh-keygen -t rsa -b 4096 -C "[Enter e-mail address here]"
```

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
