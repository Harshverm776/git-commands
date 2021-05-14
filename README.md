# Git Commands

## 1. Install git

check version `git --version`

## 2. Configuring some settings

>Like Name, Email, Default Editor & Line Ending

>Different levels for setting - System, Global & Local.

```bash
git config --global user.name "Harsh Verma"
```

```bash
git config --global user.email harshverm776@gmail.com
```

```bash
git config --global core.editor "code --wait"
```

```bash
git config --global -e
```

**Line endings -**

| Windows | macOS/Linux |
| ------- | ----------- |
| \r\n    | \n          |

* *For Windows* 
```bash
git config --global core.autocrlf true 
```
* *For Linux*
```bash
git config --global core.autocrlf input
```

## 3. Taking help 
Use `-h` or `--help`

## 4. Initializing a Repo

```bash
git init
```

**Additional cmds -**

* Make directory - `mkdir Moon`

* Open directory - `cd Moon`

* Open a file -
  * `start .git` *for Windows*
  * `open .git` *for Linux*

* Remove a file -
  * rm -rf .git

* Listing files - 
    * ls 
    * ls -a

## 5. Staging Area

>For checking the state of repo and staging area
```bash
git status 
```

**Additional cmds -**

* Creating a new file `echo hello > file1.txt`
* Appending content `echo world >> file1.txt`
* Adding files to staging area -
    * `git add file1.txt file2.txt`
    * `git add *.txt`
    * `git add .`


## 6. Commiting Changes

* Adding short comment
```bash
git commit -m "Initial commit"
```
* Adding short and long comment
```bash
git commit
```

## 7. Skipping the stagging area

>Rarely used
```bash
git commit -a -m "Some message"
```
or
```bash
git commit -am "Some message"
```

## 8. Removing files
    WD : Working Directory
    SA : Staging Area

> Removing file from both WD & SA

```bash
git rm file2.txt 
```

**Additional cmds -**

* File only remove from WD - `rm file2.txt`
* Checking SA - `git ls-files`

## 9. Renaming or Moving files

> Changes reflected in both WD and SA

```bash
git mv file1.txt main.js 
```

**Additional cmds -**

* Renaming file - `mv file1.txt main.js`

* Adding to SA - `git add file1.txt main.js`

## 10. Ignoring Files

>We can add file names like logs/ *.class  *.log  bin/

```bash
echo logs/ > .gitignore
```
or
```bash
echo > .gitignore
```

**Removing a file only from SA -**
```bash
git rm --cached bin/
```
```bash
git rm --cached -r bin/
```

## 11. Short status

```bash
git status -s
```

## 12. Viewing the staged and unstaged changes

* Staged changes
```bash
git diff --staged 
```

* Unstaged changes
```bash
git diff
```

**Additional cmds -**
* Open file in cmd - `cat file2.txt`
* Open file in cmd with numbers - `cat -n file2.txt`


## 13.  Using Visual diff Tools

* Configuring VScode-

```bash 
git config --global diff.tool vscode
```
*  Configuring launching -

```bash
git config --global difftool.vscode.cmd "code --wait --diff $LOCAL $REMOTE"
```
* Viewing unstaged changes -
```bash
git difftool
```
* Viewing staged changes -
```bash
git difftool --staged
```

## 14.  Viewing the history

* Full logs -
```bash
git log
```
* Logs in single line -
```bash
git log --oneline
```
* Reverse Order -
```bash
git log --oneline --reverse
```
> **"space"** for moving a head and **"q"** for quitting

## 15.  Viewing the commit
* Using unique identifier -
```bash
git show 921a
```

* Viewing Last commit -
```bash
git show HEAD 
```
*  One step back -
```bash
git show HEAD~1
```
* Viewing particular file - 
```bash
git show HEAD~1:.gitignore
```
* Listing all the files -
```bash
git ls-tree HEAD~1
```

## 16.  Unstaging the files
```bash
git restore --staged file1.txt
```

## 17. Discharding local changes

```bash
git restore .
```

**Additional cmds -**
*  Removing all untracked files -
```bash
git clean
```
```bash
git clean -fd
```

## 18. Restoring a file to an Earlier Version

```bash
git restore --source=HEAD~1 file1.js
```

---
---
###### Sources :
* Videos -
  * [Git Tutorial](https://youtu.be/8JJ101D3knE)
  * [Markdown Formatting](https://youtu.be/bpdvNwvEeSE)
* Websites -
  * [Basic writing and formatting syntax
](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax)
