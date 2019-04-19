---
title: N/A version "N/A -> N/A" is not yet installed.
subTitle: You need to run "nvm install N/A" to install it before using it.
category: "issues"
cover: photo-1490474418585-ba9bad8fd0ea.jpg
---

After installing node via the `nvm`, I kept getting an error in my VS Code Terminal:
```
N/A version "N/A -> N/A" is not yet installed.
You need to run "nvm install N/A" to install it before using it.
```

### Backstory
I had been using Node 11 installed using brew and I found out that I had also been using Node v8.12.0 which was installed using NVM. I had been scouring Google for a couple of days about "How to uninstall Node" and found that it can easily be done via brew (if it was installed using brew) and using nvm (if it were installed using nvm).

### How to uninstall NodeJS?
If you're using `brew`:
```
brew uninstall node --ignore-dependencies
```
The `--ignore-dependencies` flag is for brew to ignore any applications like Yarn that might have been using it. But don't worry, we'll install Node again.
---
If you're using `nvm`
```
nvm uninstall v8.12.0
```
Replace v8.12.0 with any version that you'd like to uninstall.


### How I fixed the issue:
I installed `NodeJS` using `nvm`.
```
nvm install node
```
However, I kept getting the error mentioned in the title. Somehow, I found this solution.
```
nvm alias default node
```

And it worked!
