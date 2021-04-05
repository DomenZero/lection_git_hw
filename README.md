# lection_git_hw

1.
  1. Create local repository named lection_git_hw
  ```git
  $ mkdir lection_git_hw
  $ cd lection_git_hw
  $ git init
  ```
  2. Create file "homework" in this repo and commit it in master branch
  ```git
  $ touch homework
  $ git add homework
  $ git commit -m "Made: create file homework"
  ```
  3. Create branch "hw_git" and insert anything in the file and commit these changes to this branch
  ```git
  (master) $ git branch
  * master
  $ git branch hw_git
  (master)$ git branch
  hw_git
  * master
  (master)$ git checkout hw_git
  Switched to branch 'hw_git'
  (hw_git)$ touch test
  (hw_git)$ git add test
  (hw_git)$ git commit -m "Made: create file test"
  ```
  4. Switch back to master branch and add anything else to the empty file "homework" there too
  ```git
  (hw_git) $ echo "Hello" > homework
  (hw_git) $ cat homework 
  Hello
  (hw_git) $ git add homework
  warning: LF will be replaced by CRLF in homework.
  The file will have its original line endings in your working directory
  (hw_git) $ git commit -m "Change: Add Hello in the file homework"
  ```
  5. Merge branch "hw_git" to "master", keep only changes from "hw_git" branch
  ```git
  (master)$ git merge hw_git
  ```
  6. Switch to "hw_git" branch again and create new file "temp_file" and commit it
  ```git
  (master)$ git checkout hw_git
  (hw_git)$ touch temp_file
  (hw_git)$ git commit -am "Made: create file temp_file"
  ```
  7. Revert to the first commit in "hw_git" branch
  ```git
  $ git log --pretty=oneline
  $ git revert c5b3385e2221
  OR
  $ git revert HEAD~1
  ```

2.
  1. Register in Github (if you are not registered yet) and create empty repository "lection_git_hw"
  2. Set remote from your local repo from task 1 to this new repo (https://help.github.com/articles/changing-a-remote-s-url/)
  3. Push all branches to the remote repo
  ```git
  $ git push --all origin
  ```
  4. Change everything in file "homework" in branch "hw_git" to one line "Hello Github", commit it and push
  5. Create Pull Request from branch "hw_git" to the master branch and assign me as reviewer to this merge request
