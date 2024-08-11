## Part 02: GitHub Flow<sup>[[1]][_ref_01]</sup>
> 1. Create branch.
> 2. Make changes and commit.
> 3. Push to GitHub.
> 4. Create a pull request (PR).
> 5. Address review comments on PR.
> 6. Merge your pull request.
> 7. Delete your branch.

This worksheet will go over adding a **.gitignore** file to the repository, and then merging it into the main branch. Now that you understand some of the fundamentals of git CLI, now we can use the GUI.

### 00. The .gitignore file<sup>[[2]][_ref_02]</sup>
- This specifies the files and directories that you don't want to track. For example any file that holds API keys, as you never want to expose them online. If you do accidentally commit and push to GitHub, you should rotate the API key for your app.
- Most of the time a **.gitignore** is generated when setting up a project, or a template can be found online. There is also the case where you may want to prevent **git** from tracking something yourself.
- For example here we have a **.env**, containing a super secret password.

    ![][01]

- Obviously it's just not smart to commit that. So what we can do is add **.env** to the **.gitignore** and save. Then we can see that **git** will ignore it.

    ![][02]

--------------------------------------------------

### 01. Create branch

1. Open GitHub desktop, and click on **[New branch]**.

    ![][03]

1. Give it a name and base it on the **dev** branch.

    ![][04]

1. Add a the following files: **.env** , **foo.c**. And a folder **node_modules**, with a file inside **bar.java**. Feel free to add some code, or text inside the files. The structure should look like this:

    ![][05]

1. In GitHub Desktop, you will now see the changed files, as these are being **tracked** by git. Note that staging/adding files on GitHub desktop is represented with the tickbox and only the ticked files will be included when committing.

    ![][06]

1. Let's prevent git from **tracking** the files we made. In VSCode add a **.gitignore** file at the root of the directory. Then add the following and save:

    ```
    # Ignore all .env files, in root
    .env

    # Ignore all .c files, in all directories
    **/*.c

    # Ignore the node_modules directory
    /node_modules
    ```

    ![][07]

1. In GitHub Desktop, we can now see that the files we added before are gone. See what happens if you remove items from the **.gitignore** file.

    ![][08]

--------------------------------------------------

### 02. Make changes and commit

1. Now commit the change.

    ![][09]

1. Go to history, and we can see the commit was made.

    ![][10]

--------------------------------------------------

### 03. Push to GitHub

1. Push this to GitHub.

    ![][11]

--------------------------------------------------

### 04. Create a pull request (PR)

1. Click on **Preview Pull Request**

    ![][12]

1. Choose which **branch** you want to **merge** gitignore into. Then create the pull request.

    ![][13]

1. It will then take you to the GitHub website to confirm the **PR** and then create it. You are also able to ask collaborators to review the **PR**.

    ![][14]

1. The pull request is now created.

    ![][15]

--------------------------------------------------

### 05. Address review comments on PR

1. You can add comments or start a review on the lines of the code. This works best when you have someone else review your code.

    ![][16]
    ![][17]

1. After confirming all items are viewed. Click on **[Finish your review]**

    ![][18]
    ![][19]

1. Now you should resolve the conversation.

    ![][20]

--------------------------------------------------

### 06. Merge your pull request

1. With all that done, you can **[Merge pull request]**. Obviously it won't always be this simple. In more complex repositories, there will probably be merge conflicts.

    ![][21]
    ![][22]

--------------------------------------------------

### 07. Delete your branch

1. Deleting your branch indicates that the work on the branch is complete and prevents you or others from accidentally using old branches.

    ![][23]
    ![][24]

1. You are able to view closed pull request here.

    ![][25]
    ![][26]

--------------------------------------------------
--------------------------------------------------
--------------------------------------------------

[_ref_01]: https://docs.github.com/en/get-started/using-github/github-flow
[_ref_02]: https://git-scm.com/docs/gitignore/en

[01]: ../images/_02_github_flow/01.png
[02]: ../images/_02_github_flow/02.png
[03]: ../images/_02_github_flow/03.png
[04]: ../images/_02_github_flow/04.png
[05]: ../images/_02_github_flow/05.png
[06]: ../images/_02_github_flow/06.png
[07]: ../images/_02_github_flow/07.png
[08]: ../images/_02_github_flow/08.png
[09]: ../images/_02_github_flow/09.png
[10]: ../images/_02_github_flow/10.png
[11]: ../images/_02_github_flow/11.png
[12]: ../images/_02_github_flow/12.png
[13]: ../images/_02_github_flow/13.png
[14]: ../images/_02_github_flow/14.png
[15]: ../images/_02_github_flow/15.png
[16]: ../images/_02_github_flow/16.png
[17]: ../images/_02_github_flow/17.png
[18]: ../images/_02_github_flow/18.png
[19]: ../images/_02_github_flow/19.png
[20]: ../images/_02_github_flow/20.png

[21]: ../images/_02_github_flow/21.png
[22]: ../images/_02_github_flow/22.png
[23]: ../images/_02_github_flow/23.png
[24]: ../images/_02_github_flow/24.png
[25]: ../images/_02_github_flow/25.png
[26]: ../images/_02_github_flow/26.png
