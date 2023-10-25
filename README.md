<div align="center">

<img width="60px" src="https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png"></img>

# git-get-started

</div>

Welcome to the git course! I am going to be teaching the basics of Git/GitHub using the Windows operating system.

Read the requirements carefully and follow my instructions on the screen. If you get lost at any point, ask me directly to repeat.

You can copy and paste the commands we will be using from this repo.

## Requirements

* A functional computer with Windows 10/11 (for Linux/macOS ask me directly).
* A GitHub account
* Git Bash
* A text editor such as Visual Studio Code, sublime text, etc...

## Setting everything up...

### Let's install and configure Git!

Click the button below:

<div align="center">

<font size="5"> **[Download Git for Windows](https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe)** </font>

</div>

For other releases (Linux or macOS) check the [download page](https://git-scm.com/downloads).

### Let's create a GitHub account!

If you already have a GitHub account, you can completely skip this step. If not:

<div align="center">

<font size="5"> **[Create a GitHub account](https://github.com/signup)** </font>

</div>

### Let's configure SSH!

Open `cmd.exe` on Windows or the equivalent of a terminal and begin to type:

Go to home directory, create `.ssh` folder:
```cmd
cd %HOMEPATH%
mkdir .ssh
cd .ssh
```

To create the keys we are going to use for authentication copy and paste the following commands:

```cmd
ssh-keygen -t ed25519 -f <FILENAME>.key
```

Replace `<FILENAME>` with the filename of your preference.

Now, we will create a configuration file for SSH. Replace `<CODE_EDITOR>` with the code editor of your choice:

```cmd
<CODE_EDITOR> config
```

Paste the following template:

```
Host github-as-<GITHUB_USERNAME>
    HostName github.com
    User git
    IdentityFile C:\Users\<MACHINE_USERNAME>\.ssh\<PRIVATE_KEY>
```

Replace:

* `<GITHUB_USERNAME>` with your Github username (the same you use lo log-in).
* `<MACHINE_USERNAME>` with the user you are currently logged-in.
* `<PRIVATE_KEY>` with the name of your **PRIVATE** key file.

Now, go to the GitHub configuration page for keys:

<div align="center">

<font size="3"> **[Manage GitHub keys](https://github.com/settings/keys)** </font>

</div>

With help of the instructor add you **PUBLIC** key to GitHub.

### Let's start using Git!

You are now ready to go! You can now manage external Git repositories to keep track of the changes to your code and projects.

| Basic Git Commands | Description |
|---------------------|-------------|
| `git init`         | Initializes a new Git repository in the current directory. |
| `git clone <repository>` | Creates a copy of a remote Git repository on your local machine. |
| `git add <file>`   | Stages a file for the next commit. |
| `git commit -m "<message>"` | Records the changes in the staged files with a descriptive message. |
| `git status`       | Shows the status of your working directory, including changes to be committed. |
| `git log`          | Displays a log of all previous commits in the repository. |
| `git branch`       | Lists all local branches in your repository. |
| `git checkout <branch>` | Switches to a different branch. |
| `git pull`         | Fetches changes from a remote repository and merges them into your current branch. |
| `git push`         | Pushes your local changes to a remote repository. |
| `git diff`         | Shows the differences between the working directory and the last commit. |
| `git remote -v`    | Lists the configured remote repositories. |