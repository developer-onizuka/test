# 1. Initial release
```
$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint: 	git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint: 	git branch -m <name>
Initialized empty Git repository in /mnt/test/.git/

$ git config --global user.email test@example.com
$ git config --global user.name test

$ git add README.md
$ git commit -m "Initial release"
```

# 2. Feature branch
```
$ git branch feature
$ git checkout feature
Switched to branch 'feature'

$ git log
commit 676ed2c42ffab236522a711444c2f1cdfa8d795f (HEAD -> master, feature)
Author: test <test@example.com>
Date:   Thu Sep 22 11:23:59 2022 +0900

    Initial release

$ git add README.md 
$ git commit -m "Feature branch"
```

# 3. Merge branch
```
$ git checkout master
Switched to branch 'master'

$ git log
commit 676ed2c42ffab236522a711444c2f1cdfa8d795f (HEAD -> master)
Author: test <test@example.com>
Date:   Thu Sep 22 11:23:59 2022 +0900

    Initial release

$ git merge feature
Updating 676ed2c..e6657da
Fast-forward
 README.md | 16 ++++++++++++++++
 1 file changed, 16 insertions(+)

$ git log
commit e6657da718e5b53eac1cd0a562b17bb69c876769 (HEAD -> master, feature)
Author: test <test@example.com>
Date:   Thu Sep 22 11:26:49 2022 +0900

    Feature branch

commit 676ed2c42ffab236522a711444c2f1cdfa8d795f
Author: test <test@example.com>
Date:   Thu Sep 22 11:23:59 2022 +0900

    Initial release

$ git add README.md
$ git commit -m "Merge branch"
```
