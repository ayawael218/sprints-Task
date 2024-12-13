commit history starting with resolving a conflict merge and then the 3 commits(because I encountered an error while working on conflict merge) :
ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git push
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 662 bytes | 662.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ayawael218/sprints-Task.git
   288c6ca..9536708  main -> main

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git pull
Already up to date.
g
ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git checkout branch2_test
Switched to branch 'branch2_test'
Your branch is up to date with 'origin/branch2_test'.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch2_test)
$ git merge main
Auto-merging file2.html
CONFLICT (content): Merge conflict in file2.html
Automatic merge failed; fix conflicts and then commit the result.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch2_test|MERGING)
$ git status
On branch branch2_test
Your branch is up to date with 'origin/branch2_test'.

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   file2.html

no changes added to commit (use "git add" and/or "git commit -a")

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch2_test|MERGING)
$ git add .

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch2_test|MERGING)
$ git commit -m "conflict solved"
[branch2_test bcfd937] conflict solved

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch2_test)
$ git merge main
Already up to date.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch2_test)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git merge branch2_test
Updating 9536708..bcfd937
Fast-forward
 file2.html | 6 +++++-
 1 file changed, 5 insertions(+), 1 deletion(-)

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 380 bytes | 380.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/ayawael218/sprints-Task.git
   9536708..bcfd937  main -> main

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git checkout branch1_test
Switched to branch 'branch1_test'

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git status
On branch branch1_test
nothing to commit, working tree clean

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git log
commit 20d65adba4a483b38e7b4f223d8be23a911a0fd7 (HEAD -> branch1_test)
Author: AyaSaad <ayasaad1712@gmail.com>
Date:   Fri Dec 13 23:50:02 2024 +0200

    second commit in file1

commit 90f445d15bb765b89740c11d81678036e02b04aa
Author: AyaSaad <ayasaad1712@gmail.com>
Date:   Fri Dec 13 23:46:23 2024 +0200

    first commit to file1

commit 9d4ddac0a9b4b02bd950d3593ab56e3e66d1b4eb
Author: ayawael218 <98208434+ayawael218@users.noreply.github.com>
Date:   Fri Dec 13 23:28:40 2024 +0200

    Create file2.html

commit 4ce07244f94ec628bf549330c708fa9166badff6
Author: ayawael218 <98208434+ayawael218@users.noreply.github.com>
Date:   Fri Dec 13 23:25:23 2024 +0200

    Create file1.html


ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git status
On branch branch1_test
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   file1.html

no changes added to commit (use "git add" and/or "git commit -a")

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git add .

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git commit -m "first change in file1 after encountering an error"
[branch1_test cb8598f] first change in file1 after encountering an error
 1 file changed, 1 insertion(+), 1 deletion(-)

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git push --set-upstream origin branch1_test
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 8 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 1024 bytes | 1024.00 KiB/s, done.
Total 9 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'branch1_test' on GitHub by visiting:
remote:      https://github.com/ayawael218/sprints-Task/pull/new/branch1_test
remote:
To https://github.com/ayawael218/sprints-Task.git
 * [new branch]      branch1_test -> branch1_test
branch 'branch1_test' set up to track 'origin/branch1_test'.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git pull origin main
From https://github.com/ayawael218/sprints-Task
 * branch            main       -> FETCH_HEAD
hint: Waiting for your editor to close the file... error: There was a problem with the editor 'vi'.
Not committing merge; use 'git commit' to complete the merge.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test|MERGING)
$ git add .

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test|MERGING)
$ git commit -m "commit after second error"
[branch1_test 03ea381] commit after second error

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git merge main
Already up to date.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git merge branch1_test
Updating bcfd937..03ea381
Fast-forward
 file1.html | 4 ++--
 1 file changed, 2 insertions(+), 2 deletions(-)

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 295 bytes | 295.00 KiB/s, done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/ayawael218/sprints-Task.git
   bcfd937..03ea381  main -> main

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git checkout branch1_test
Switched to branch 'branch1_test'
Your branch is ahead of 'origin/branch1_test' by 8 commits.
  (use "git push" to publish your local commits)

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git push
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/ayawael218/sprints-Task.git
   cb8598f..03ea381  branch1_test -> branch1_test

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git status
On branch branch1_test
Your branch is up to date with 'origin/branch1_test'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   file1.html

no changes added to commit (use "git add" and/or "git commit -a")

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git add .

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git commit -m "second change in file1 after error"
[branch1_test ed92a68] second change in file1 after error
 1 file changed, 1 insertion(+)

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git merge main
Already up to date.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git merge branch1_test
Updating 03ea381..ed92a68
Fast-forward
 file1.html | 1 +
 1 file changed, 1 insertion(+)

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git checkout branch1_test
Switched to branch 'branch1_test'
Your branch is ahead of 'origin/branch1_test' by 1 commit.
  (use "git push" to publish your local commits)

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 385 bytes | 385.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/ayawael218/sprints-Task.git
   03ea381..ed92a68  branch1_test -> branch1_test

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git merge main
Already up to date.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git push
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/ayawael218/sprints-Task.git
   03ea381..ed92a68  main -> main

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git merge branch1_test
Already up to date.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git checkout branch1_test
Switched to branch 'branch1_test'
Your branch is up to date with 'origin/branch1_test'.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git status
On branch branch1_test
Your branch is up to date with 'origin/branch1_test'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   file1.html

no changes added to commit (use "git add" and/or "git commit -a")

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git log
commit ed92a68d4a5f9b8c2b7ac202887e3afdd48a08f8 (HEAD -> branch1_test, origin/main, origin/branch1_test, origin/HEAD, main)
Author: AyaSaad <ayasaad1712@gmail.com>
Date:   Sat Dec 14 01:02:03 2024 +0200

    second change in file1 after error

commit 03ea38178f11a04908fbcb6d60a0ef6edb13c569
Merge: cb8598f bcfd937
Author: AyaSaad <ayasaad1712@gmail.com>
Date:   Sat Dec 14 00:55:20 2024 +0200

    commit after second error

commit cb8598fc83599c6b4ee4c889adc5ce75f324812c
Author: AyaSaad <ayasaad1712@gmail.com>
Date:   Sat Dec 14 00:52:04 2024 +0200

    first change in file1 after encountering an error

commit bcfd9372a915018b6741abff3b91f7dc1f7e25ec (branch2_test)
Merge: 44642a9 9536708
Author: AyaSaad <ayasaad1712@gmail.com>


ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git add .

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git commit -m "third change in file1"
[branch1_test e8525f9] third change in file1
 1 file changed, 1 insertion(+)

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 315 bytes | 315.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/ayawael218/sprints-Task.git
   ed92a68..e8525f9  branch1_test -> branch1_test

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git merge main
Already up to date.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (branch1_test)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git merge branch1_test
Updating ed92a68..e8525f9
Fast-forward
 file1.html | 1 +
 1 file changed, 1 insertion(+)

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$ git push
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/ayawael218/sprints-Task.git
   ed92a68..e8525f9  main -> main

ayawa@LAPTOP-T24TRRQT MINGW64 /d/Sprints-Git/sprints-Task (main)
$
