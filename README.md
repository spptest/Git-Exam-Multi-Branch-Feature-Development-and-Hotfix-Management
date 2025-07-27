### 🧭 Git Commit Graph

This section shows the visual commit history across all branches using:

```bash
* c31ddb0 (HEAD -> main, origin/main) feat: Added dashboard stats
* 90295ec feat: Added dashboard welcome
* 0dc9468 Added logout
* 6e479f3 feat: Added login
* b43a96b hotfix: Ghost security
* 07e4ea2 feat: Ghost sync
* 7ba3a87 Initial commit
```

![Screenshot-Reflog](https://aideck.eu/course-git/Git1.JPG)

## 📜 Git Reflog History

This section shows the recent history of changes and HEAD movements in the repository using `git reflog`.

```bash
c31ddb0 (HEAD -> main, origin/main) HEAD@{0}: merge feature-dashboard: Fast-forward
0dc9468 HEAD@{1}: checkout: moving from feature-dashboard to main
c31ddb0 (HEAD -> main, origin/main) HEAD@{2}: rebase (finish): returning to refs/heads/feature-dashboard
c31ddb0 (HEAD -> main, origin/main) HEAD@{3}: rebase (pick): feat: Added dashboard stats
90295ec HEAD@{4}: rebase (pick): feat: Added dashboard welcome
0dc9468 HEAD@{5}: rebase (start): checkout main
0ed3804 HEAD@{6}: checkout: moving from main to feature-dashboard
0dc9468 HEAD@{7}: merge feature-auth: Fast-forward
b43a96b HEAD@{8}: checkout: moving from feature-auth to main
0dc9468 HEAD@{9}: rebase (finish): returning to refs/heads/feature-auth
0dc9468 HEAD@{10}: rebase (pick): Added logout
6e479f3 HEAD@{11}: rebase (pick): feat: Added login
b43a96b HEAD@{12}: rebase (start): checkout main
322c7eb HEAD@{13}: checkout: moving from main to feature-auth
b43a96b HEAD@{14}: merge hotfix-security: Fast-forward
07e4ea2 HEAD@{15}: checkout: moving from hotfix-security to main
b43a96b HEAD@{16}: commit: hotfix: Ghost security
07e4ea2 HEAD@{17}: checkout: moving from main to hotfix-security
07e4ea2 HEAD@{18}: commit: feat: Ghost sync
7ba3a87 HEAD@{19}: checkout: moving from feature-dashboard to main
0ed3804 HEAD@{20}: commit: feat: Added dashboard stats
47a247c HEAD@{21}: commit: feat: Added dashboard welcome
7ba3a87 HEAD@{22}: checkout: moving from main to feature-dashboard
7ba3a87 HEAD@{23}: checkout: moving from feature-auth to main
322c7eb HEAD@{24}: commit: Added logout
4f01b66 HEAD@{25}: commit: feat: Added login
7ba3a87 HEAD@{26}: checkout: moving from main to feature-auth
7ba3a87 HEAD@{27}: commit (initial): Initial commit
```

![Screenshot-Reflog](https://aideck.eu/course-git/Git2.JPG)



# Git Workflow Example

This project demonstrates a standard Git workflow with multiple feature branches, a hotfix, and a clean commit history using interactive rebasing.

## Branches Created

- `main`: The main branch.
- `feature-auth`: For authentication-related features (login/logout).
- `feature-dashboard`: For UI improvements on the dashboard.
- `hotfix-security`: For resolving a critical security bug introduced in `main`.

## Workflow Steps

1. Initialized the repository with an initial commit.
2. Created `feature-auth` and `feature-dashboard` branches.
3. Made multiple commits to each feature branch:
   - `feature-auth`: login, logout features.
   - `feature-dashboard`: dashboard welcome, stats.
4. Switched to `main` and introduced a critical bug.
5. Created `hotfix-security`, fixed the bug, and merged it back into `main`.
6. Merged both feature branches into `main`, resolving conflicts as needed.
7. Used interactive rebase to ensure a clean and linear commit history.

## Notes

- This repo follows a structured Git strategy to support parallel development and quick bug fixing.
- Interactive rebase was used to tidy up the commit history before final merges.
