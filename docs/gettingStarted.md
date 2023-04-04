# Getting Started With Git

!!! Warning "Prerequisites"

    Before continuing with the guide, make sure you have completed the following prerequisites:
    <ul>
      <li> Windows 10 installed on your computer </li>
      <li> Created a github account </li>
      <li> Installed a working version of Git </li>
      <li> Installed Visual Studio Code </li>
    </ul>

## Verifying Git is installed

1. Open a terminal window by navigating to your search bar and typing `cmd`. Press enter to open the command prompt.
   <br />
   <br />
   <img src="/images/openTerminal.png" alt= "Opening command prompt" width="650px">
   <br />
   <br />
2. Verify you have Git installed by running the following command `git -v`.
   <br />
   <br />
   <img src="/images/verifyGitInstalled.png" alt= "Checking version of Git installed" width="650px">
   <br />
   <br />
3. Your command prompt should display your current Git version if you have successfully installed git.

!!! Tip

     If you are unsure what a command does, you can type `git help <command>` into the terminal to get more information about the command. For example, if you want to know what the `git -v` command does, type `git help -v` into the terminal.

## Creating a Remote Repository

1.  First, navigate to <https://github.com> and log into your GitHub account. If you do not have an account, create a GitHub account by going to <https://github.com/join>.

2.  After logging in, click on the “+” sign in the top right corner of the page and select “New repository” from the dropdown menu.
    <br />
    <br />
    <img src="/images/gettingStarted/createRepository.png" alt= "Creating a new github repository" width="650px">
    <br />
    <br />

3.  On the “Create a new repository” page, enter a name for your repository in the “Repository name” field. Make sure to choose a name that describes what your code does. You can also add a description if you like.
    <br />
    <br />
    <img src="/images/gettingStarted/namingRepository.png" alt= "Naming the new repository" width="650px">
    <br />
    <br />

4.  Select the repository’s visibility. If you want your code to be public, leave the repository as public. If you want it to be private, select “Private”.
    <br />
    <br />
    <img src="/images/gettingStarted/visibilityRepository.png" alt= "Selecting the visability of the new repository" width="650px">
    <br />

    !!! Warning

            Public repositories are visible to anyone on the internet. Private repositories are only visible to the owner and collaborators. If you are unsure which option to choose, select private. The visibility of your repository can be changed at any time.

5.  If you want to include a README file, check the box that says “Initialize this repository with a README”. This will create a README file in your repository that you can edit later.
    <br />
    <br />
    <img src="/images/gettingStarted/readMeRepository.png" alt= "Creating a README file for the new repository" width="650px">
    <br />

    !!! Tip

            A README file is a text file that contains information about your project. *It is always best practice to include a README file in your repository* because it will help other people understand what your project is about. For more information about README files, see <https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/about-readmes>.

6.  When you are ready to finalize the changes and create your repository, click the “Create repository” button at the bottom of the page.
    <br />
    <br />
    <img src="/images/gettingStarted/createFinalRepository.png" alt= "Finalize creating the repository" width="650px">
    <br />

## Creating a Local Copy of the Repository

1.  You will first need to create a folder on your computer to store the repository. To do this, open your file explorer, navigate to the directory where you want to store your project's code, right click and create a new folder for the project.
    <br />
    <br />
    <img src="/images/gettingStarted/createFolder.png" alt= "Create new folder for project" width="650px">
    <br />

    !!! Tip

            It is always best practice to create a new folder for each project you work on. This will keep your projects organized and make it easier to find them later.

2.  After creating the folder, open Visual Studio Code and open the directory you just created. To do this, click on the “File” tab in the top left corner of the screen and select “Open Folder”. Navigate to the directory you just created, select it and click the “Select Folder” button.
    <br />
    <br />
    <img src="/images/gettingStarted/openFolder.png" alt= "Open folder in Visual Studio Code" width="650px">
    <br />

3.  Once you’re inside the directory, open a new terminal instance in your Visual Studio Code by clicking on the “Terminal” tab in the top left of the screen and select “New Terminal”. This will create a new terminal instance in the directory you are currently in.
    <br />
    <br />
    <img src="/images/gettingStarted/openTerminalVSCode.png" alt= "Open terminal in Visual Studio Code" width="650px">
    <br />

4.  Next, navigate to the GitHub repository you created in steps 2 to 6 of the previous section. Click on the “Code” button and copy the URL of the repository.
    <br />
    <br />
    <img src="/images/gettingStarted/gitLink.png" alt= "Copy the URL of the remote repository" width="650px">
    <br />

5.  Back in the Visual Studio Code terminal, use the `git clone [repository URL]` command to link the remote repository to your local repository. Replace the `[repository URL]` with the URL you copied in the previous step.
    <br />
    <br />
    <img src="/images/gettingStarted/gitClone.png" alt= "Cloning the remote repository" width="650px">
    <br />

    !!! Danger "git clone: command not found"

         If you get the error `git clone: command not found`, it means you may have not installed Git correctly. To fix this, go back to the introduction page and try installing Git again.

    !!! Success

         You have successfully created a local copy of the repository in your computer. After you have added a few files to your local repository, continue with the guide to learn how you can push them to a remote repository on GitHub!

## Adding Files to the Repository

After making some changes in your local repository, you can add them to the remote repository on GitHub. To do this, you will need to follow the Git workflow. If you need a refresher on the Git workflow, you can review the Git workflow section in the introduction page. To add files to the repository, follow the steps below:

1.  First, change your terminal directory to the directory of your local repository. To do this, type `cd [directory name]` into the terminal. Replace the `[directory name]` with the name of the directory you created in the previous section.
    <br />
    <br />
    <img src="/images/gettingStarted/gitCd.png" alt= "Changing the terminal directory" width="650px">
    <br />

    !!! Warning

            The directory in the terminal must be the same as the directory you created in the previous section.

2.  Use the `git add` command to add the files to the staging area. For example, if you want to add a file called `index.html`, type `git add index.html` into the terminal. Alternatively, you can add all the files in the directory by typing `git add .` into the terminal.
    <br />
    <br />
    <img src="/images/gettingStarted/gitAdd.png" alt= "Adding files to the staging area" width="650px">
    <br />

    !!! Info "`git add`"

               This is the first step of the Git workflow. The staging area is a temporary area where you can add files before committing them to the repository. You can add as many files as you want to the staging area before committing them to the repository. For more information about the Git workflow, you can review the Git workflow section in the introduction page.

    !!! Tip

               If at anytime you are unsure about what files are in the staging area, you can type `git status` into the terminal. This will show you a list of all the files in the staging area.

3.  After adding the files to the staging area, commit the changes using the `git commit -m "[Your commit message]"` command. You should see a similar output message in the terminal. Adding a `-m` flag allows you to add a message explaining the changes you made. For example, if you added a new file called `index.html`, you can type `git commit -m "Added index.html"` into the terminal. Others with access to your repository will be able to see this message when they view the commit history.
    <br />
    <br />
    <img src="/images/gettingStarted/gitCommit.png" alt= "Committing the changes" width="650px">
    <br />

    !!! Info "`git commit`"

            This is the second step of the Git workflow. After adding the files to the staging area, you can commit them to the repository. For more information about the Git workflow, you can review the Git workflow section in the introduction page.

    !!! Info "Best Practices"

            It is always best practice to add a message when committing your changes. This will help you and others understand what changes you made. It is also best to write a commit message starting with a verb in the present tense. For example, if you fixed a bug in the code, you can write a commit message like “Fix bug in code”.

4.  Finally, use the `git push` command in the terminal. This will push the changes to the remote repository on GitHub. You should see a similar output message in the terminal.
    <br />
    <br />
    <img src="/images/gettingStarted/gitPush.png" alt= "Pushing the changes to the remote repository" width="650px">
    <br />

    !!! Info "`git push`"

            This is the third step of the Git workflow. After committing the changes, you can push them to the remote repository on GitHub. For more information about the Git workflow, you can review the Git workflow section in the introduction page.

    !!! Success "Congratulations!"

            You have successfully pushed your code to GitHub. You should now be able to see your code on GitHub. When you make more changes in the future, you can follow the same steps to push your code to GitHub.