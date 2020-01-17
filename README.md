# RTPSUG Git Playground

I'm hosting this repo as a means for the RTPSUG group to have a repository they can clone, that contains nothing of importance for the purposes of learning git.

# Getting this repository locally

The first step to being successful with git is to install a git client. You can install it manually, but that friggin sucks, so I'd do this:

```powershell
choco install git -y
```

If you don't have [Chocolatey](https://chocolatey.org) yet, you can install it, by opening a PowerShell console using "Run as Administrator" and executing the following code:

```powershell
Set-ExecutionPolicy Bypass -Force ; iex (New-Object System.Net.Webclient).DownloadString('https://chocolatey.org/install.ps1')
```

There are also some great GUI tools available if the command line of git is still a bit intimidating while getting started.

Git Fork is my favorite, though there are certainly others. You can install Git Fork with chocolatey using the following:

```
choco install git-fork -y
```

Once you have git installed, you should fork this repository, this will move it into your own Github account, and allow you to push changes. Otherwise, with a clone, you won't be able to push up your changes due to permissions. So hit the Fork button in the upper right. Once you have that done, it's time to clone it

Pop open a PowerShell console and execute the following:

```powershell
#Make a directory where this repo will "live"
mkdir C:\Git

#Clone the repo. Change this URL to the link from your fork (just change the username here basically).
git clone https://github.com/steviecoaster/rtpsug-git.git
```

# Making your first commit

Now that you have the repo cloned, you can start playing with it. Cloning the repo should have created a `C:\Git\rtpsug-git` directory, and you can open it in VSCode easily with `code C:\Git\rtpsug-git`.

Either create a new file or edit one of the existing files, and save your changes.

Head back to the command line, and run `git status`. You should see that the file you just created or changed has rather an untracked (if new file), or modified (if you changed an existing file) status. 

Add your changes to git's history so those changes are tracked with `git add .`. Note that this adds _all_ the untracked/modified changes to the commit.

Once you have added the changes, commit them using `git commit -m "Short message about your change"`

Your changes are now staged and ready to be pushed to the repository. You can do that by issuing `git push`.

Stevie rocks my world. :)
