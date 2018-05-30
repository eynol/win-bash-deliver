When you double click a .sh file, deliver it to WSL to excute.

# Requirement
Windows OS within WSL installed.

# Set Up
1. Download the `win-bash-deliver.exe` file from [realase page](./releases) or some where else, put it into a folder (Don't forget where it is).
2. Right click on a `*.sh` file. Select `Properties`, and then select `Change...`.
3. Select `more...` in the popup window, and then find and choose our `win-bash-deliver.exe`.
4. Check the `Default Program` above the yes button, setting the `win-bash-deliver.exe` as the default program to excute `.sh` file.
5. Finally, click the `Yes` button and have fun! Just double click a shell script file!


# How it works?
Well, first when you double click a sh file, the file's absolute path will be passed as the second argument to `win-bash-deliver.exe`. (The first arg was the absolute path of `win-bash-deliver.exe` file).

When the program knows where the shell script file is, it will transform it's Windows-like path to Unix-like path that can be accessed in WSL. For example, path of `D:\some\folders\dailycheckin.sh` will be transformed to `/mnt/d/some/folders/dailycheckin.sh`.


# Development - Build
`go build win-bash-deliver.go`