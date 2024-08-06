# gitGood
## Setup git / GitHub
1. Create/login to a [GitHub account][01.01].

1. Once signed up go to settings.
![][01.05]
![][01.06]

1. Check `Keep my email addresses private`, and read what it does.
![][01.07]

1. Install [git][01.02].
1. Install [GitHub Desktop][01.03], and sign in.
1. Install [VSCode][01.04].
1. Done

## Part 01: Git basics
- tbc

## Part 02: GitHub flow
- tbc

## Git and GitHub <sup>[[1]][03.01]</sup>
### Introduction to git <sup>[[2]][03.02]</sup>
Git is a version control system that intelligently tracks changes in files. Git is particularly useful when you and a group of people are all making changes to the same files at the same time.

Typically, to do this in a Git-based workflow, you would:
- Create a branch off from the main copy of files that you (and your collaborators) are working on.
- Make edits to the files independently and safely on your own personal branch.
- Let Git intelligently merge your specific changes back into the main copy of files, so that your changes don't impact other people's updates.
- Let Git keep track of your and other people's changes, so you all stay working on the most up-to-date version of the project.

### Introduction to GitHub
GitHub is a cloud-based platform where you can store, share, and work together with others to write code. Collaborative working, one of GitHub’s fundamental features, is made possible by the open-source software, Git, upon which GitHub is built.

Storing your code in a "repository" on GitHub allows you to:
- Showcase or share your work.
- Track and manage changes to your code over time.
- Let others review your code, and make suggestions to improve it.
- Collaborate on a shared project, without worrying that your changes will impact the work of your collaborators before you're ready to integrate them.

### How do Git and GitHub work together?
When you upload files to GitHub, you'll store them in a "Git repository." This means that when you make changes (or "commits") to your files in GitHub, Git will automatically start to track and manage your changes.

There are plenty of Git-related actions that you can complete on GitHub directly in your browser, such as creating a Git repository, creating branches, and uploading and editing files.

However, most people work on their files locally (on their own computer), then continually sync these local changes—and all the related Git data—with the central "remote" repository on GitHub. There are plenty of tools that you can use to do this, such as GitHub Desktop.

Once you start to collaborate with others and all need to work on the same repository at the same time, you’ll continually:
- Pull all the latest changes made by your collaborators from the remote repository on GitHub.
- Push back your own changes to the same remote repository on GitHub.
- Git figures out how to intelligently merge this flow of changes, and GitHub helps you manage the flow through features such as "pull requests."

[01.01]: https://github.com/
[01.02]: https://git-scm.com/downloads
[01.03]: https://github.com/apps/desktop
[01.04]: https://code.visualstudio.com/
[01.05]: ./images/readme_01.png
[01.06]: ./images/readme_02.png
[01.07]: ./images/readme_03.png
[03.01]: https://docs.github.com/en/get-started/start-your-journey/about-github-and-git
[03.02]: https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F
