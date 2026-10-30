Git BRANCH ---

git remote set-url origin https://BenBinhTran@github.com/BenBinhTran/BinhBenTran.github.io.git


git credential-manager github logout

===
# Clear old credentials if switching to a new VirtualCV GitHub account
git credential-manager github logout BenBinhTran
git credential-manager github list 2>&1

# Initialize and push to the new repository
git init
git add .
git commit -m "🎉 Initial commit: VirtualCV Hub setup and Ben's CV"
git branch -M main
git remote add origin https://github.com/VirtualCV/VirtualCV.github.io.git
git push -u origin main

=========
# Clear old credentials if switching to a new VirtualCV GitHub account
<!-- git credential-manager github logout BenBinhTran -->
git credential-manager github logout PhoenixWeaver
git credential-manager github list 2>&1

# 1. Start fresh on main and get latest updates
git checkout main
git pull origin main

# 2. Create and switch to your new feature branch
git checkout -b feature/V4

# 3. Add and commit your new CV files to the feature branch
git add .
git commit -m "✨ $(date +%d%m%y) $(date +%H%M) ✨ - Add CV builder Mobile US profile new image"

# 4. Push the feature branch to GitHub
git push -u origin feature/V4

# 5. Switch back to main, merge the feature, and push live
git checkout main
git merge feature/V4 --no-ff -m "🔀 Merge $(date +%d%m%y) $(date +%H%M) ✨ - Add CV builder Update ✨"
git push origin main