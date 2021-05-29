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

### view changes status

```
git status
```

### commit changes

```
git commit -m "initial commit"
```

<img src="../../../Users/Shamin_Yang/AppData/Roaming/Typora/typora-user-images/image-20210529150653963.png" alt="image-20210529150653963" style="zoom:67%;" />

### commit information

- ID
- Message
- Date/Time
- Author
- Complete snapshot

