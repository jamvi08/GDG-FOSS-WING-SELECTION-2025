### Answer the following questions in you own words.

> It's not necessary that you havee to know and answer all the questions. Just answer the ones
> you know and write in your own words.

1. Give the difference between the remotes - upstream and origin - with an example.

You answer:
-origin: the default name given to the remote when you clone your fork. It usually points to your own copy of the repo.

-upstream: used to refer to the original repository from which you forked. This helps you keep your fork updated.

2. You have two branches A and B and you have currently made some changes in branch A.
   You want to move into branch B but do not want to commit the current changes in branch A.
   What will you do?

You answer:

- Use git stash. This saves your uncommitted changes in a temporary storage area without committing them. Later, you can apply them back with git stash apply

3. You were assigned a work to implement a feature and create a PR to your organization's remote repository.
   For this you made a branch (say A) and made some changes and commited them. Now you moved to some other branch
   (say B) to do some other assigned work. But later you realisd that have to complete the task assigned earlier
   first and commited some changes in branch B which are meant for branch A. How will you use git to bring the
   changes from branch B to branch A?

You answer:

- We can use git rebase. First, switch to branch A and then rebase branch B on top of it.

3. What is the difference between fetching changes and pulling changes?

Your answer:
-git fetch: Downloads changes from the remote to your local repo but does not update your working branch.

-git pull: Does fetch and merge and directly updates your working branch with remote changes.

4. What does -i flag stand for? What is it's significance in git?

You answer:

- basically, -i stands for interactive. It permits us to do things manually by our choice.

5. You are working in an organization that follows very strict guidelines for PRs and commits.
   You made three commits in your PR and the maintainer says you were supposed to make a single commit.
   What will you do in this case?

You answer:
-Git rebase -i HEAD~3 then squash is prefered to use when we want to merge the commits we did in our hist

6. Explain `git merge` and `git rebase` with example(s).

You answer:

- git merge preserves the history of past commits. It combines the changes of two branches together and creates a new merge commit.The old commit history is not changed, so it is safe when working in teams.

In git rebase we get several options like squash, drop, edit regarding the commits. But the problem with git rebase is that the commit history is not preserved, and the commit hash may also get changed during rebase.

Git rebase is preferred when we are working on our personal level project.

7. Write the flow how you create a repository and push changes to it. Also mention the commands used at each step.

You answer:

- go to new repository in your github and name it. here your new repo is created.
- copy repo link and use git clone command on your VSCode to work on it.
- also git checkout -b (branch-name) is used if you want to create a new branch on what you want to work.
  -then use git add . to add all the changes . this adds your all changes to the stagging area. also if you want to add the only particular file changes then use git add [file name].
- use Git commit "a msg in present tense what you have done".
- finally, git push.

8. How would you prevent a file or folder from getting tracked by git?

Your answer: 1. The way is we make a .gitignore file and put all the file names in it which we do not want to be tracked by Git.

9. You did not implement the step you mentioned in question 8 and now you have committed and pushed your database's
   secret key to the github. How will you remove the key from your git's commit history to avoid any misuse?

You answer:

- git reset --hard i will use. this will remove all the past commit and the changes i have made regarding the commit.

---
