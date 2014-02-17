# GIT MERGE MASTER (on production)

simo@topa: ~/Projects/testing-git-repos2 on production
$ git merge master
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.

simo@topa: ~/Projects/testing-git-repos2 on production [+!]
$ git st
# On branch production
# You have unmerged paths.
#   (fix conflicts and run "git commit")
#
# Unmerged paths:
#   (use "git add <file>..." to mark resolution)
#
# both modified:      README.md
#
no changes added to commit (use "git add" and/or "git commit -a")

simo@topa: ~/Projects/testing-git-repos2 on production [+!]
$ git diff
diff --cc README.md
index 2f17f0f,b345af7..0000000
--- a/README.md
+++ b/README.md
@@@ -1,3 -1,3 +1,7 @@@
  Hello World
  
++<<<<<<< HEAD
 +This creates prodestruction
++=======
+ This creates good stuff!
++>>>>>>> master


---


# GIT MERGE PRODUCTION (on master)

simo@topa: ~/Projects/testing-git-repos2 on master
$ git merge production
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.

simo@topa: ~/Projects/testing-git-repos2 on master [+!]
$ git st
# On branch master
# You have unmerged paths.
#   (fix conflicts and run "git commit")
#
# Unmerged paths:
#   (use "git add <file>..." to mark resolution)
#
# both modified:      README.md
#
no changes added to commit (use "git add" and/or "git commit -a")

simo@topa: ~/Projects/testing-git-repos2 on master [+!]
$ git diff
diff --cc README.md
index b345af7,2f17f0f..0000000
--- a/README.md
+++ b/README.md
@@@ -1,3 -1,3 +1,7 @@@
  Hello World
  
++<<<<<<< HEAD
 +This creates good stuff!
++=======
+ This creates prodestruction
++>>>>>>> production

