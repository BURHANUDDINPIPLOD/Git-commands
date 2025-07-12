# Git-commands
Celebal Technologies - Week 8


# 1. Stage all changes and commit with a message
git add .
git commit -m "Your meaningful commit message"

# 2. Move commits to correct branch (from wrong-branch to correct-branch)
git checkout -b temp-branch        # create temp branch from wrong-branch
git checkout correct-branch
git merge temp-branch              # bring changes into correct-branch
git branch -d temp-branch          # delete temp branch

# 3. Create a new branch, make changes, and push to GitHub
git checkout -b new-feature-branch
# (Make your code changes here before continuing)
git add .
git commit -m "Added feature XYZ"
git push -u origin new-feature-branch

# 4. Contribute to open-source project via fork (after cloning forked repo)
git checkout -b your-feature-branch
# (Make your changes here)
git add .
git commit -m "Contributed feature or fix"
git push origin your-feature-branch
# Then open a pull request on GitHub manually

# 5. Resolve merge conflicts between your branch and main
git fetch origin
git checkout your-branch
git merge origin/main
# (If conflicts appear, manually resolve them in the files)
# After resolution:
git add .
git commit -m "Resolved merge conflicts"

# 6. Create feature branch from updated main
git checkout main
git pull origin main
git checkout -b new-feature-branch

# 7. Revert to a specific commit (replace <commit-hash> with actual hash)
git reset --hard <commit-hash>
# If pushed already:
git push origin HEAD --force

# 8. Restore deleted file from last commit (replace with actual file path)
git checkout HEAD^ -- path/to/deleted-file
git add path/to/deleted-file
git commit -m "Restored deleted file"
