# Git Introduce

## 2 Types of Version Control System

- Centralized
- Distributied

### Centralized Type

<img src="../../../Users/Shamin_Yang/AppData/Roaming/Typora/typora-user-images/image-20210528144815512.png" alt="image-20210528144815512" style="zoom:80%;" />

### Distributed Type

<img src="../../../Users/Shamin_Yang/AppData/Roaming/Typora/typora-user-images/image-20210528145107520.png" alt="image-20210528145107520" style="zoom:70%;" />

## Why Git

- Free
- Open Source
- Super Fast
- Scalable
- Cheap Branching/Merging

## Extension Tools for VS Code

GitLens - Git supercharged

## Git GUI IDE

all list in website: https://git-scm.com/downloads/guis

### 2 top popular Git UI IDE

| GIT IDE Tools | Remark                   |
| ------------- | ------------------------ |
| GitKraken     | not free for commercial  |
| SourceTree    | free for Windows and Mac |

## Why need Git Command Line

- GUI tools have limitations
- GUI tools are not always available

# Git Settings

- Name
- Email
- Default Editor
- Line Ending

## Setting Scope

| Level  | Remark                               |
| ------ | ------------------------------------ |
| System | All users                            |
| Global | All repositories of the current user |
| Local  | The current repository               |

## Setting Command

### user name

```
git config --global user.name "shamin"
```

local

```
git config user.name "shamin"
```

### user email

```
git config --global user.email xxxx@xxx.com
```

### code edit (VS Code)

```
git config --gloabal core.editor "code --wait"
```

### git config

```
git config --global -e
```

## core.autocrlf

### Difference between windows and macOS

| Windows | macOS |
| ------- | ----- |
| abc\r\n | abc\n |

\r = carriage return

\n = line feed

### autocrlf Behavior

<img src="../../../Users/Shamin_Yang/AppData/Roaming/Typora/typora-user-images/image-20210528155052814.png" alt="image-20210528155052814" style="zoom:67%;" />

### autocrlf setting command

windows

```
git config --global core.autocrlf true
```

macOS

```
git config --global core.autocrlf input
```

## git config command

git config command help (open a web page)

```
git config --help
```

git config command parameters

```
git config -h
```

git config variables list

```
git config -l
```

# Git Command

## Initial Repository

create a local git repository for a project

```
git init
```

view files

```
ls
ls -a
```

re-initial an empty git repository for current project

```
rm -rf .git
git init
```

## Workflow

### add files

```
git add file1 file2
```

<img src="../../../Users/Shamin_Yang/AppData/Roaming/Typora/typora-user-images/image-20210529150503334.png" alt="image-20210529150503334" style="zoom:67%;" />

### add all files not sub directories

```
git add .
```

### add all files include sub directories

```
git add -A
```

### add specific files

```
git add *.cs
```

### add changed files into unstage

```
rm file_name
git add file_name
git ls-files
```

the result won't output file_name any more.

### view changes status

```
git status
```

```
git ls-files
```

### remove files from both working directory and staging area

```
git rm file2.txt *.txt
git rm -f file2.txt *.txt
```

### commit changes

```
git commit -m "initial commit"
git commit -am "initial commit with all files"
```

<img src="../../../Users/Shamin_Yang/AppData/Roaming/Typora/typora-user-images/image-20210529150653963.png" alt="image-20210529150653963" style="zoom:67%;" />

### commit information

- ID
- Message
- Date/Time
- Author
- Complete snapshot

## git ignore

### create a git ignore file

```

echo logs/ > .gitignore
code .gitignore
```

### edit .gitignore file

```
logs/
bin/
debug/
test.txt
*.bac
backup.txt
```

### add and commit .gitigore

```
git add .gitignore
git commit -m "add logs .gitignore"
```

it will impact the git repository

### remove one item in .gitignore when commit

temp remove settings in .gitignore

```
git rm --cached -r bin/
git ls-files
```

above command won't list any files under "bin/"

check change status, we will see the changes

```
git status
```

```
git status -s
```

check output result:

??  = the changes which have not been added into stage

M = modified files

A = new files

### gitignore reference template

https://github.com/github/gitignore

## View staged and unstaged codes