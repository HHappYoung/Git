# Git学习笔记

## 3. 基本命令

```bash

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git
$ git init
Initialized empty Git repository in D:/MyBlog/Git/.git/

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ ls -al
total 4
drwxr-xr-x 1 LENOVO 197609 0 Jul 28 13:26 ./
drwxr-xr-x 1 LENOVO 197609 0 Jul 28 13:26 ../
drwxr-xr-x 1 LENOVO 197609 0 Jul 28 13:26 .git/

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ touch Git-note.md

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Git-note.md

nothing added to commit but untracked files present (use "git add" to track)

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git add .

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   Git-note.md


LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git commit -m "add Git-note.md"
[main (root-commit) 12e6ed3] add Git-note.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Git-note.md

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git status
On branch main
nothing to commit, working tree clean

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git log
commit 12e6ed3390d4f1c594e28f97a63283ade0197869 (HEAD -> main)
Author: hhy <hhy200319@gmail.com>
Date:   Sun Jul 28 13:32:05 2024 +0800

    add Git-note.md

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ vscode Git-note.md
bash: vscode: command not found

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ code Git-note.md

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Git-note.md

no changes added to commit (use "git add" and/or "git commit -a")

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git add .

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   Git-note.md


LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git commit -m "update Git-note.md"
[main 9fa6354] update Git-note.md
 1 file changed, 1 insertion(+)

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git status
On branch main
nothing to commit, working tree clean

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git log
commit 9fa635483740af6585e3caffee447471cc3847c4 (HEAD -> main)
Author: hhy <hhy200319@gmail.com>
Date:   Sun Jul 28 13:38:02 2024 +0800

    update Git-note.md

commit 12e6ed3390d4f1c594e28f97a63283ade0197869
Author: hhy <hhy200319@gmail.com>
Date:   Sun Jul 28 13:32:05 2024 +0800

    add Git-note.md

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ mkdir test01

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git status
On branch main
nothing to commit, working tree clean

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git add .

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git status
On branch main
nothing to commit, working tree clean

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ cd ./test01

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git/test01 (main)
$ touch test0101.txt

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git/test01 (main)
$ cd ..

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test01/

nothing added to commit but untracked files present (use "git add" to track)

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git add ,
fatal: pathspec ',' did not match any files

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git add .

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   test01/test0101.txt


LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git log
commit 9fa635483740af6585e3caffee447471cc3847c4 (HEAD -> main)
Author: hhy <hhy200319@gmail.com>
Date:   Sun Jul 28 13:38:02 2024 +0800

    update Git-note.md

commit 12e6ed3390d4f1c594e28f97a63283ade0197869
Author: hhy <hhy200319@gmail.com>
Date:   Sun Jul 28 13:32:05 2024 +0800

    add Git-note.md

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git commit -m "add subfolder test01"
[main dbebd7d] add subfolder test01
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test01/test0101.txt

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git log
commit dbebd7dd0d86ff81975c53acd3d6253a6015c6e0 (HEAD -> main)
Author: hhy <hhy200319@gmail.com>
Date:   Sun Jul 28 14:21:47 2024 +0800

    add subfolder test01

commit 9fa635483740af6585e3caffee447471cc3847c4
Author: hhy <hhy200319@gmail.com>
Date:   Sun Jul 28 13:38:02 2024 +0800

    update Git-note.md

commit 12e6ed3390d4f1c594e28f97a63283ade0197869
Author: hhy <hhy200319@gmail.com>
Date:   Sun Jul 28 13:32:05 2024 +0800

    add Git-note.md

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git reset --hard 9fa635483740af6585e3caffee447471cc3847c4
HEAD is now at 9fa6354 update Git-note.md

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$ git status
On branch main
nothing to commit, working tree clean

LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog/Git (main)
$

```

#### 分支

HEAD指明当前处于哪个分支



## 4. 远程仓库

### 4.1 常用的托管服务（远程仓库）

GitHub

### 4.2 创建远程仓库

### 4.3 配置SSH公钥

远程仓库的名字默认设为origin，不要用其他名字。SSH地址会在创建github仓库时给出，复制即可，例如 git@github.com:HHappYoung/Git-note.git

### 4.4 操作远程仓库

#### 4.4.1 添加远程仓库



#### 4.4.5 从远程仓库克隆

命令：git clone <仓库路径> [本地目录]

- 在`Code`界面，点击绿色的`Code`按钮，获取仓库的SSH地址，

![image-20240729112148093](md-images/image-20240729112148093.png)

- 在你想要克隆仓库的目标位置打开Git Bash，例如我想把仓库克隆到`D:\MyBlog\Git01\`文件夹下，那我就在`D:\MyBlog\`中打开Git Bash，并执行以下指令。（如果没有`Git01`文件夹会自动创建）

```bash
git clone git@github.com:HHappYoung/Git-note.git Git01
```

结果如下：

```bash
LENOVO@LAPTOP-AUK9CS5V MINGW64 /d/MyBlog
$ git clone git@github.com:HHappYoung/Git-note.git Git01
Cloning into 'Git01'...
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (7/7), done.
Receiving objects: 100% (16/16), done.
Resolving deltas: 100% (3/3), done.
remote: Total 16 (delta 3), reused 16 (delta 3), pack-reused 0

```

