# gitstudy
login as: ec2-user
Authenticating with public key "imported-openssh-key"
Last login: Sun May 23 05:46:07 2021 from ec2-13-233-177-0.ap-south-1.compute.amazonaws.com

       __|  __|_  )
       _|  (     /   Amazon Linux 2 AMI
      ___|\___|___|

https://aws.amazon.com/amazon-linux-2/
[ec2-user@ip-172-31-40-78 ~]$ sudo su
[root@ip-172-31-40-78 ec2-user]# ls
[root@ip-172-31-40-78 ec2-user]# which git
/bin/git
[root@ip-172-31-40-78 ec2-user]# mkdir mumbaigit
[root@ip-172-31-40-78 ec2-user]# ls
mumbaigit
[root@ip-172-31-40-78 ec2-user]# cd mumbaigit
[root@ip-172-31-40-78 mumbaigit]# git init
Initialized empty Git repository in /home/ec2-user/mumbaigit/.git/
[root@ip-172-31-40-78 mumbaigit]# cat >mumbai1
This is Mumbai Repo file
[root@ip-172-31-40-78 mumbaigit]# git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        mumbai1

nothing added to commit but untracked files present (use "git add" to track)
[root@ip-172-31-40-78 mumbaigit]# git add .
[root@ip-172-31-40-78 mumbaigit]# git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   mumbai1

[root@ip-172-31-40-78 mumbaigit]# git commit -m "My first commit from mumbai."
[master (root-commit) a040d47] My first commit from mumbai.
 1 file changed, 1 insertion(+)
 create mode 100644 mumbai1
[root@ip-172-31-40-78 mumbaigit]# git status
On branch master
nothing to commit, working tree clean
[root@ip-172-31-40-78 mumbaigit]# git log
commit a040d47fa84cabc4e5468428b6b69afe6686b9b3 (HEAD -> master)
Author: vishal <narvishal1@gmail.com>
Date:   Sun May 23 05:58:31 2021 +0000

    My first commit from mumbai.
[root@ip-172-31-40-78 mumbaigit]# git show  a040d47fa
commit a040d47fa84cabc4e5468428b6b69afe6686b9b3 (HEAD -> master)
Author: vishal <narvishal1@gmail.com>
Date:   Sun May 23 05:58:31 2021 +0000

    My first commit from mumbai.

diff --git a/mumbai1 b/mumbai1
new file mode 100644
index 0000000..fefa85e
--- /dev/null
+++ b/mumbai1
@@ -0,0 +1 @@
+This is Mumbai Repo file
[root@ip-172-31-40-78 mumbaigit]# git remote add origin https://github.com/narvishal1/gitstudy.git
[root@ip-172-31-40-78 mumbaigit]# git push -u origin master
Username for 'https://github.com': narvishal1
Password for 'https://narvishal1@github.com':
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 242 bytes | 242.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/narvishal1/gitstudy.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
[root@ip-172-31-40-78 mumbaigit]# cat >mumbai1
this is test file for mumbai repo. done here.
[root@ip-172-31-40-78 mumbaigit]# git status
On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   mumbai1

no changes added to commit (use "git add" and/or "git commit -a")
[root@ip-172-31-40-78 mumbaigit]# git add .
[root@ip-172-31-40-78 mumbaigit]# git status
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   mumbai1

[root@ip-172-31-40-78 mumbaigit]# git commit -m "this is edit once"
[master aa0081f] this is edit once
 1 file changed, 1 insertion(+), 1 deletion(-)
[root@ip-172-31-40-78 mumbaigit]# git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
[root@ip-172-31-40-78 mumbaigit]# git log
commit aa0081f80c3cb7d5be5f6cdcf7ccf2b915e665e8 (HEAD -> master)
Author: vishal <narvishal1@gmail.com>
Date:   Sun May 23 06:09:24 2021 +0000

    this is edit once

commit a040d47fa84cabc4e5468428b6b69afe6686b9b3 (origin/master)
Author: vishal <narvishal1@gmail.com>
Date:   Sun May 23 05:58:31 2021 +0000

    My first commit from mumbai.
[root@ip-172-31-40-78 mumbaigit]# git show  aa0081f8
commit aa0081f80c3cb7d5be5f6cdcf7ccf2b915e665e8 (HEAD -> master)
Author: vishal <narvishal1@gmail.com>
Date:   Sun May 23 06:09:24 2021 +0000

    this is edit once

diff --git a/mumbai1 b/mumbai1
index fefa85e..4c3278b 100644
--- a/mumbai1
+++ b/mumbai1
@@ -1 +1 @@
-This is Mumbai Repo file
+this is test file for mumbai repo. done here.
[root@ip-172-31-40-78 mumbaigit]# git push origin master
Username for 'https://github.com': narvishal1
Password for 'https://narvishal1@github.com':
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (3/3), 282 bytes | 282.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/narvishal1/gitstudy.git
   a040d47..aa0081f  master -> master
[root@ip-172-31-40-78 mumbaigit]#
