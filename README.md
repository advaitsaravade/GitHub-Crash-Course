# Using GitHub with Git - a crash course
Welcome to the idiot-proof guide to using the command line with GitHub.

>This guide is meant for MacOS/Unix users and a basic familiarity with Terminal commands like `mkdir` and `cd` is recommended.

When starting out with GitHub I mainly used the GUI app that GitHub provides for uploading file to a repository. However, knowing how to use the command line tools is a major upside as it is so much faster, and helps you understand the grass-roots mechanism that GitHub runs on.

This mechanism is called `Git` and [here is why it is so useful.](http://blog.robertelder.org/what-is-git/)

Without further ado, let's get to how you can upload your code to GitHub using the command line. Let's go.

## Step 1: Create a repo on GitHub

Log into Github using your username and password. Create a repository and obtain it's `.git` URL.

## Step 2: Clone the repository from GitHub to your machine

Once your repository is ready, you need to use the `clone` command to create a copy of it to your machine in order to make changes.

>At this point, you can <b><i>optionally</i></b> create a directory to store all your future GitHub repos in one directory on your machine. I personally do this as it helps me organize my code. To do this optional step type the following into Terminal: `mkdir GitHub; cd GitHub`

Now, in order to clone the repository to your machine, you'll need to install a command line tool called `git`. In order to install git on your system, [follow this super-easy guide](https://gist.github.com/derhuerst/1b15ff4652a867391f03)

Once git is ready, we can proceed with this guide. Let's get cloning. Type the following into Terminal:

`git clone <Your repo's .git URL>`

Replace `<Your repo's .git URL>` with the .git URL you see in your repository's main page on GitHub.

This will create a directory on your machine with the same name as your repository.
>If you were cloning a repository that already has files uploaded to it, these files will be downloaded to this directory

## Step 3: Add code to the repository's directory

Now that a directory has been created on your machine, simple copy your project's code base (files, folders, images etc etc.) into this directory. Whatever is in this folder on your machine will be uploaded to GitHub in the next step.

## Step 4: Prepare files for GitHub

Once you are ready to send your code to GitHub, navigate to the directory where the code is located and type the following into terminal:

`git status`

`git status` shows you which files are yet to be sent to a commit. If file names are in red, it means those files are not part of a commit just as yet. A commit is a revision or version of your project. Every time you make changes to your code, you'll need to *commit the changes*.

Anyway, you want to upload to GitHub don't you? Just add them to a commit first by typing in the following:

`git add --all`

This command prepares all the files in the directory with changes to be sent to GitHub. It adds the files to the upcoming commit.

>Now ideally, this should go across without problems but if it outputs an error with the title <b><i>"Tell me who you are?" or similar</i></b>, just type in the `.username` and `.email` commands it mentions with the appropriate values for email and username. These values don't need to be the same as your GitHub credentials and are used only for your local machine to track changes. Once this is done, run `git add --all` once again and your files are ready to upload to GitHub.

## Step 5: Upload to GitHub

Commit your files to be sent. Type in the following:

`git commit -m "A brief description of your changes for everyone to see on GitHub.com"`

Once your commit is ready, check the status of your files to make sure by typing in the following:

`git status`

This should show all your files in green color. Assuming all went well, type in the following to send it to GitHub, also known as *sending a push* or *syncing*.

`git push`

This command will ask you for you GitHub username and password sequentially. Type them in and press enter. If all goes well, this will pack and send your files and changes to your GitHub repository where they will be visible to you (and anyone else you have allowed to view your repository).

## Conclusion

That's it. Visit your repository using a browser, and your changes show show up soon.

I hope this guide helped you. I use this guide as a reference regularly and will be making changes to it as I learn more about Git and GitHub.
