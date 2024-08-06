## Part 01: Git basics

### 01. Create a repo on GitHub

1. Go to Github and login.
1. Click on __[new]__.

    ![][01]

1. Name your repository.
1. Check **[Add a README]**
1. Click **[Create repository]**

    ![][02]

--------------------------------------------------

### 02. Clone the repo to your local machine (laptop/pc)

1. Go to your repository. (it should redirect if you just created it.)
1. Click on code and then **[Open with GitHub Desktop]**

    ![][13]

1. If this warning pops up, select the following options.

    ![][14]

1. It should open up GitHub desktop, choose a location, and click **[Clone]**

    ![][12]

1. You can also do this using CLI, with `git clone <url>`

--------------------------------------------------

### 03. Opening a local repository

1. Now it's time to learn some basic CLI commands.
1. Open VScode (you installed it right?)
1. Open the **[terminal]**.

    ![][15]

1. Enter command `git status`
1. Why does it give an error? Because your current location is not a git repository.

    ![][16]

1. Now open the folder of the repo.

    ![][17]

1. Sure

    ![][18]

1. How do we know if we are in a git repository? Go to repo in explorer and show hidden files. Should see **.git**, this contains all information required for version control. <sup>[[1]][_ref_01]</sup>

    ![][19]

1. Try `git status` again, this time it should give a different output.

    ![][20]

1. Enter `git log`, this will show your commits, ordered from latest, to oldest.

    ![][21]

1. Notice it may be unpleasant to read. Enter `git config --global color.ui auto`, to add more contrast. Now enter `git log --oneline`, to show a shorter version of the log.

    ![][22]

--------------------------------------------------

### 04. Branches

1. To see your current branch use `git branch`. The asterisk indicates we are on **main**.

    ![][23]

1. Use `git branch -a`, to show all your branches including the **remote** ones on GitHub.

    ![][24]

1. It is generally bad practice to make changes to the the **main** branch. So we need to create a **new branch**.
1. Use `git branch <branchName>`. Then `git branch`, and you will see that the new branch was made, but you are still on main.

    ![][25]

1. To switch to the branch you made, use `git checkout <branchName>`, now see which branch you are on.

    ![][26]

1. To rename your branch use `git branch -m <currentName> <newName>`.

    ![][47]

1. To delete your branch switch to another branch, then use `git branch -d <deleteBranchName>`.

    ![][48]

--------------------------------------------------

### 05. Commit a single file

1. Before you can make commits you need to add or modify files. So modify the README.md and save, then check run `git status`. What do you see.

    ![][27]

1. Now we need to add the modified file to the **staging area**. The **staging area** is essentially the files that will go into your next commit.
1. To put **README.md** into staging we will use `git add <path-to-file>`. To make it easier, start by entering a few of the letters, then hit **[tab]** to autocomplete the path to file.

    ![][28]
    ![][29]

1. Now check the status and you will now see

    ![][30]

1. Finally time to add a commit. Writing a **good** commit message is important so... <sup>[[2: READ ME]][_ref_02]</sup>

1. Also **git** uses **vim** as the default text editor <sup>btw</sup>. So let's use a slightly simpler terminal text editor. Enter `git config --global core.editor "nano"`

    ![][31]

1. Now `git commit`, and we are taken here. Write your commit message. To move the cursor around use your arrow keys.

    ![][32]

1. Then press **[ctrl + o]**, then **[enter]** to save

    ![][33]
    ![][34]

1. Then **[ctrl + x]** to exit. Use `git log --oneline`, to see the latest commit.

    ![][35]

--------------------------------------------------

### 06. Committing multiple files

1. What to do when you have many files you added or modified? This is a common occurance.

    ![][36]

1. Just use `git add .`, this is probably what you will use most of the time.

    ![][37]

1. Then use `git commit -m "<message>"`, to add a commit with just the subject line.

    ![][38]

1. Imagine there was a typo. Use `git commit --amend` to change the last commit message. If you're using nano, use the steps from "commit a single file" to navigate, save, and exit.

    ![][39]

--------------------------------------------------

### 07. Pushing to GitHub

1. Okay, now push, use `git push`. You will likely get a warning. Simply run the command it gives you. `git push --set-upstream origin <branchName>`.

    ![][40]

1. If it's the first time, then it should ask you to login. Simply login with your browser, and authorise.

    ![][41]

1. Return back to your terminal and you should see:

    ![][42]

1. Go to your repository in the browser and you can see what you did.

    ![][43]
    ![][44]
    ![][45]

--------------------------------------------------

### 08. Bonus

1. That was a lot of typing. So if you didn't know, you can use your **[up]** and **[down]** arrows go backwards and forwards in your command history. Try it out.

1. The most useful one is **[ctrl + r]** which allows you to do a reverse search of previous commands. You can keep pressing **[ctrl + r]** to cycle through the search results. Press **[tab]** to pick the command, then **[enter]** to run it.

    ![][46]

--------------------------------------------------

### 09. Summary of Commands

```c
git config --global color.ui auto // better contrast
git config --global core.editor "nano" // easy
git config --global core.editor "vim" // very fun

git status // shows current status
git log // show log of commit history
git log --oneline //shorter version of log

git branch // shows branch information
git branch -a // include remote branches
git branch <branchName> // create a new branch
git checkout <branchName> // switch to an existing branch
git branch -m <currentName> <newName> // rename branch
git branch -d <deleteBranchName> // delete branch, must switch to another one beforehand

git add <path-to-file> // add file to staging
git add . // add all changes in current working directory to staging

git commit // allow you to write longer commit message
git commit -m "subject line" // short, use impertaive mood
git commit --amend // change previous commit message

git push // pushes to remote repository
git push --set-upstream origin <branchName> // tells which place to push to
```

--------------------------------------------------
--------------------------------------------------
--------------------------------------------------

[_ref_01]: https://stackoverflow.com/questions/29217859/what-is-the-git-folder
[_ref_02]: https://cbea.ms/git-commit/

[01]: ../images/_01_git_basics/01.png
[02]: ../images/_01_git_basics/02.png
[03]: ../images/_01_git_basics/03.png
[04]: ../images/_01_git_basics/04.png
[05]: ../images/_01_git_basics/05.png
[06]: ../images/_01_git_basics/06.png
[07]: ../images/_01_git_basics/07.png
[08]: ../images/_01_git_basics/08.png
[09]: ../images/_01_git_basics/09.png
[10]: ../images/_01_git_basics/10.png
[11]: ../images/_01_git_basics/11.png
[12]: ../images/_01_git_basics/12.png
[13]: ../images/_01_git_basics/13.png
[14]: ../images/_01_git_basics/14.png
[15]: ../images/_01_git_basics/15.png
[16]: ../images/_01_git_basics/16.png
[17]: ../images/_01_git_basics/17.png
[18]: ../images/_01_git_basics/18.png
[19]: ../images/_01_git_basics/19.png
[20]: ../images/_01_git_basics/20.png
[21]: ../images/_01_git_basics/21.png
[22]: ../images/_01_git_basics/22.png
[23]: ../images/_01_git_basics/23.png
[24]: ../images/_01_git_basics/24.png
[25]: ../images/_01_git_basics/25.png
[26]: ../images/_01_git_basics/26.png
[27]: ../images/_01_git_basics/27.png
[28]: ../images/_01_git_basics/28.png
[29]: ../images/_01_git_basics/29.png
[30]: ../images/_01_git_basics/30.png
[31]: ../images/_01_git_basics/31.png
[32]: ../images/_01_git_basics/32.png
[33]: ../images/_01_git_basics/33.png
[34]: ../images/_01_git_basics/34.png
[35]: ../images/_01_git_basics/35.png
[36]: ../images/_01_git_basics/36.png
[37]: ../images/_01_git_basics/37.png
[38]: ../images/_01_git_basics/38.png
[39]: ../images/_01_git_basics/39.png
[40]: ../images/_01_git_basics/40.png
[41]: ../images/_01_git_basics/41.png
[42]: ../images/_01_git_basics/42.png
[43]: ../images/_01_git_basics/43.png
[44]: ../images/_01_git_basics/44.png
[45]: ../images/_01_git_basics/45.png
[46]: ../images/_01_git_basics/46.png
[47]: ../images/_01_git_basics/47.png
[48]: ../images/_01_git_basics/48.png
