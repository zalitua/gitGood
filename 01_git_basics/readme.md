## Worksheet 01: Git basics
### 01. Create a repo on GitHub
1. Go to [Github][01.01] and login.

1. Click on `new`.
![][01.02]

1. Name your repository.
1. Check `Add a README`
1. Click `Create repository`
![][01.03]


### 02. Clone the repo to your local machine (laptop/pc)
1. Go to your repository. (it should redirect if you just created it.)

1. Click on code and then `Open with GitHub Desktop`
![][02.11]

1. If this warning pops up, select the following options.
![][02.12]

1. It should open up GitHub desktop, choose a location, and click `Clone`
![][02.10]

1. You can also do this using CLI, with `git clone <url>`

### 03. Working with local repository
1. Now it's time to learn some basic CLI commands.
1. Open VScode (you installed it right?)
1. Enter command `git status`
1. Why does it give an error? Because your current location is not a git repository.
1. Now open the folder with VSCode.
1. How do we know if we are in a git repository?
1. Go to repo in explorer and show hidden files. Should see `.git`, this contains all information required for version control.


### 0x. GitHub Desktop
- Repeat all the steps above but with GitHub desktop.

### The .gitignore file

[01.01]: https://github.com/
[01.02]: ../images/_01_git_basics/01.png
[01.03]: ../images/_01_git_basics/02.png
[02.01]: ../images/_01_git_basics/03.png
[02.02]: ../images/_01_git_basics/04.png
[02.03]: ../images/_01_git_basics/05.png
[02.04]: ../images/_01_git_basics/06.png
[02.05]: ../images/_01_git_basics/07.png
[02.06]: ../images/_01_git_basics/08.png
[02.07]: ../images/_01_git_basics/09.png
[02.08]: ../images/_01_git_basics/10.png
[02.09]: ../images/_01_git_basics/11.png
[02.10]: ../images/_01_git_basics/12.png
[02.11]: ../images/_01_git_basics/13.png
[02.12]: ../images/_01_git_basics/14.png
