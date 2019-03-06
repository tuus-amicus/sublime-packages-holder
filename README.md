# Installation

## Fresh
``` shell
git init
git remote add origin git@github.com:tuus-amicus/sublime-packages-holder.git
git fetch
git reset --hard origin/master
```

With the last line, the existing setting files will be overwritten by those from the repository. If you want your local files to be committed, just make a backup before and copy the files back to the created repository to commit the changes. Or remove the “hard” flag of the reset instruction and merge all changes manually.

## Manually

``` shell
git -C ~/.config/sublime-text-3/Packages/User pull
```
It occurs, that the settings files differ right after pulling the current versions from the repository (especially when Package Control loads missing packages) e.g. because of a different order of entries in the packages list or the settings elements. In that case you can just use the hard-reset instruction to overwrite your unwanted local changes.

## Using GIT package in Sublime
It’s even easier to sync the settings with the Git Package for Sublime Text. Here you don’t have to switch to a Git Shell to pull or push the changes but you can do it right in Sublime Text.

Simply open your settings file and you will see any changes in the status bar. If you have to pull or push something just hit CTRL+SHIFT+P to open the command palette and start typing “git”. Now you can see all options to pull, push or reset your current working directory

# ATTENTION
Please, be aware that the name of Default (OSX).sublime-keymap file will be different across different OS (in case the target OS is MacOS or Linux), so better to have three different files with the same content among them, just duplicate the file and rename it according to your target OS.

[https://medium.com/@devmount/using-git-to-sync-sublime-text-settings-f70b8dc7a40d](Source)
