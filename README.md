# GIT-TEST

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

NOTE: If the command fails and you receive the error invalid format or feature not supported, you may be using a hardware security key that does not support the Ed25519 algorithm. <br> Enter the following command instead.

```sh
ssh-keygen -t ecdsa-sk -C "[Enter e-mail address here]"
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