### Cherry-Pick : Manual [URL](https://www.ruanyifeng.com/blog/2020/04/git-cherry-pick.html)

1. Cherry-pick:
   1.  git log --oneline ->copy commit number
   2.  git checkout branck_name
   3.  git cherry-pick commit_number
   4.  done
2. Conflict:
   1.  change conflict section
   2.  git add .
   3.  git cherry-pick --continue