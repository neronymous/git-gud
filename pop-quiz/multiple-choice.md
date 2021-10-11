# Multiple Choice Quiz

## Guide

1. Please don't edit any of the content of this file, except for the answer boxes, otherwise you'll have to start again later because this file matters.

2. There is one correct (or most correct) answer per question, you **won't** be expected to choose more than answer per question.

3. To pick an answer replace the `_` inside of the square brackets with a capital x IE `X`. So `[_]` becomes `[X]`.

4. Once you've answered all the questions run the following command exactly (same case and everything, no extra spaces or flair) `git commit -am "done"`

5. Run the command `git log -1`, this should give you the details about the last commit you just made.

6. Now help the person to the immediate left and right of you until you're all done.

## Quiz

**Part A**

1. Which of the following commands will "stage" every modified file as well as every one of the untracked files too?

   - [-] git add -u
   - [-] git commit .
   - [-] git add -A
   - [-] git commit -am "trololol"

2. Given a smattering of modified files have been staged, how would you "unstage" all of the files in the `docs/` folder?

   - [_] git checkout docs/
   - [_] git reset .
   - [_] git reset docs/
   - [_] find -f docs/**/*.* | git reset $0

3. Having modified the `README.md` file of this repo, how would you undo these changes and restore the file back to the state it was committed in?

   - [_] git checkout README.md
   - [_] git reset README.md
   - [_] git undo README.md
   - [_] git reset README.md --hard

**Part B**

The following questions rely on the following output of a `git status` command:

```
On branch master
Your branch is ahead of 'origin/master' by 365 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   infra/snowflake-pipeline/ecs.tf
        modified:   server/src/main/java/co/vgw/pm/Main.java
        modified:   server/pom.xml

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        infra/ecr/repositories.tf
        server/src/main/java/co/vgw/pm/Utils.java
```

1. For the above output, what command would stage only the modified .tf files, leaving the untracked .tf file alone?

   - [_] git add *.tf
   - [_] git add .
   - [_] git add -u *.tf
   - [_] git add .; git reset *.tf

2. For the above output, if I were to run the command `git checkout .` which of the following would happen?

   - [_] The 3 modified files and the 2 untracked files would have all their changes undone.
   - [_] Nothing would happen because none of those files have been staged.
   - [_] The 3 modified files will have all their changes undone, the untracked files will be left untouched.
   - [_] The 3 modified files will be now be flagged as 'untracked'

3. For the above output, if I were to run the command `git reset .` which of the following would happen?

   - [_] The 3 modified files and the 2 untracked files would have all their changes undone.
   - [_] Nothing would happen because none of those files have been staged.
   - [_] The 3 modified files will have all their changes undone, the untracked files will be left untouched.
   - [_] The 3 modified files will be now be flagged as 'untracked'

**Part C**

The following questions rely on the following output of a `git status` command:

```
On branch master
Your branch is ahead of 'origin/master' by 365 commits.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   infra/ecr/repositories.tf
        modified:   server/src/main/java/co/vgw/pm/Utils.java

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   infra/snowflake-pipeline/ecs.tf
        modified:   server/src/main/java/co/vgw/pm/Main.java
        modified:   server/pom.xml
```

1. For the above output, if I were to run the command `git checkout .` which of the following would happen?

   - [-] The 3 unstaged files and the 2 staged files would have all their changes undone.
   - [-] Nothing would happen because none of those files are untracked.
   - [-] The 3 unstaged files will have all their changes undone, the 2 staged files will be left untouched.
   - [-] The 3 unstaged files will be now be flagged as 'untracked'

2. For the above output, if I were to run the command `git reset .` which of the following would happen?

   - [_] The 3 unstaged files and the 2 staged files would have all their changes undone.
   - [_] Nothing would happen because none of those files are untracked.
   - [_] The 3 unstaged files will have all their changes undone, the 2 staged files will be left untouched.
   - [_] The 2 staged files will now show as unstaged meaning that all 5 files will be flagged as unstaged.
