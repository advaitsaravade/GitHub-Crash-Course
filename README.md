# GitHub Crash Course
Welcome to the idiot-proof guide to using the command line with GitHub. This guide is meant for MacOS/Unix users and a basic familiarity with Terminal commands is recommended. When starting out with GitHub I mainly used the GUI app that GitHub provides for uploading file to a repository. However, knowing how to use the command line tools is a major upside as it is so much faster, and helps you understand the grass-roots mechanism that GitHub runs on.

This mechanism is called `Git` and here is why it is useful. TODO add link.

Without further ado, let's get to how you can upload your code to GitHub using the command line. Let's go.

## Step 1: Create a repo on GitHub

Log into Github.com using your GitHub username and password. Create a repository and obtain it's `.git` URL.

## Step 2: Clone the repository from GitHub to your machine

Once your repository is ready, you need to use the `clone` command to create a copy of it to your machine in order to make changes.

At this point, you can optionally create a directory to store all your future GitHub repos in one place on your machine. To do this optional step type the following into Terminal:

`mkdir GitHub; cd GitHub`

Let's clone the repository to your machine now. Type the following into Terminal:

`git clone <Your repo's .git URL>`

Replace <Your repo's .git URL> with the .git URL you see in your repository's main page on GitHub.

This will create a directory in your Terminal with the name of your repository. If your repository has some files in it already, these will be downloaded to your machine in the same directory.

## Step 3: Add code to the repository's directory

Now that a directory has been created on your machine, simple copy your project's code base (files, folders, images etc etc.) into this directory. Whatever is in this folder on your machine will be uploaded to GitHub in the next step.

## Step 4: Prepare files for GitHub

Once you are ready to send your code to GitHub, navigate to the directory where the code is located and type the following into terminal:

`git status`

This command will provide a list of files, usually red in color. `git status` shows you which files are yet to be sent to a commit. If it is red, that means this file is not part of a commit. You want to upload to GitHub don't you? Just add them to a commit first using the following:

`git add --all`

This command prepares all the files in the directory with changes to be sent to GitHub. Now idealy, this should go across without problems but if it outputs an error with the title "Tell me who you are?" or similar, just type in the `.username` and `.email` commands it mentions with appropriate values (this doesn't need to be the same as your GitHub credentials as it is only for your local machine). Once this is done, run `git add --all` once again and you're ready to upload to GitHub.

## Step 5: Upload to GitHub

Commit your files to be sent. Type in the following:

`git commit -m "A brief description of your changes for everyone to see on GitHub.com"`

Once your commit is ready, check the status of your files to make sure. Type the following once again:

`git status`

This should show all the files in green color, if all went well. Assuming it did, type in the following to send it.

`git push`

This command will ask you for you GitHub username and password one by one. Type them in and press enter. If all goes well, this will pack and send your files and changes to your GitHub repository where they will be visible to you (and anyone else you have allowed to view your repository).
