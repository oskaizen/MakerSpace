# 🤝 Assignment: Multi-Agent Development Workflow
We’ll be demoing this assignment during class, and you’re encouraged to test it out at home using your own use cases.

## 📚 Table of Contents

- [Overview](#overview)
- [Step 1: Set Up Your Development Environment 🏗️](#step-1-set-up-your-development-environment-️)
- [Step 2: Create Feature Branches 🌿](#step-2-create-feature-branches-)
- [Step 3: Multi-Agent Workflow in Cursor 🤖](#step-3-multi-agent-workflow-in-cursor-)
- [Step 4: View Branches on GitHub 🌐](#step-4-view-branches-on-github-)
- [Step 5: Merge Branches Using Best Practices 🔀](#step-5-merge-branches-using-best-practices-)
- [Step 6: Clean Up Branches 🧹](#step-6-clean-up-branches-)
- [Step 7: View Result in Vercel 🌐](#step-7-view-result-in-vercel-)
- [🏗️ Activity #2: Advanced Multi-Agent Challenge](#️-activity-2-advanced-multi-agent-challenge)
- [💅 Example: "Hot Mess Tracker" App](#-example-hot-mess-tracker-app)
- [🎓 Tips for Success](#-tips-for-success)

---

## Overview

In this demo, we'll:
1. **Use the downloaded frontend in Cursor**
2. **Show multi-agent flow** - demonstrate how we can multitask and make different changes simultaneously
3. **Use branch development and best practices** - work with feature branches
4. **Show on GitHub branches** - visualize the branching structure
5. **Demonstrate merging** - merge branches using best practices
6. **Show the final result in Vercel** - see how changes propagate to production

---

## Step 1: Set Up Your Development Environment 🏗️

1. Open the downloaded frontend project in Cursor
2. Ensure you have the latest code from GitHub:
   ```bash
   git pull origin main
   ```
3. Verify your app still runs locally:
   ```bash
   npm run dev
   ```

---

## Step 2: Create Feature Branches 🌿

We'll create multiple branches to work on different features simultaneously, demonstrating multi-agent workflow.

### 2.1 Create Branch for Feature 1

```bash
git switch -c feature/add-new-component
git push -u origin feature/add-new-component
```

### 2.2 Create Branch for Feature 2

```bash
git switch -c feature/improve-styling
git push -u origin feature/improve-styling
```

### 2.3 Create Branch for Feature 3

```bash
git switch -c feature/add-animations
git push -u origin feature/add-animations
```

**Tip:** Each branch represents work that can be done in parallel, simulating a multi-agent workflow where different tasks are handled simultaneously.

---

## Step 3: Multi-Agent Workflow in Cursor 🤖

### 3.1 Work on Feature 1

1. Switch to `feature/add-new-component`:
   ```bash
   git switch feature/add-new-component
   ```

2. In Cursor, use AI to add a new component:
   - Ask Cursor: *"Add a new [component name] component with [specific features]"*
   - Cursor will generate the code following your cursor rules
   - Review and commit:
     ```bash
     git add .
     git commit -m "feat: add new component"
     git push origin feature/add-new-component
     ```

### 3.2 Work on Feature 2 (Parallel)

1. Switch to `feature/improve-styling`:
   ```bash
   git switch feature/improve-styling
   ```

2. In Cursor, improve styling:
   - Ask Cursor: *"Update the styling for [component/page] to match [design requirements]"*
   - Cursor will apply changes following your coding standards
   - Review and commit:
     ```bash
     git add .
     git commit -m "style: improve component styling"
     git push origin feature/improve-styling
     ```

### 3.3 Work on Feature 3 (Parallel)

1. Switch to `feature/add-animations`:
   ```bash
   git switch feature/add-animations
   ```

2. In Cursor, add animations:
   - Ask Cursor: *"Add smooth animations to [components] using [animation library]"*
   - Cursor will implement animations
   - Review and commit:
     ```bash
     git add .
     git commit -m "feat: add animations"
     git push origin feature/add-animations
     ```

**This demonstrates multi-agent workflow:** Different features are being developed simultaneously on separate branches, just like multiple developers working in parallel!

---

## Step 4: View Branches on GitHub 🌐

1. Go to your GitHub repository
2. Click on the **"branches"** dropdown
3. You'll see all your feature branches:
   - `main`
   - `feature/add-new-component`
   - `feature/improve-styling`
   - `feature/add-animations`

4. Click on each branch to see:
   - The commits made on that branch
   - The files changed
   - The diff view showing what was modified

**This visualizes the branching structure and shows how work is organized.**

---

## Step 5: Merge Branches Using Best Practices 🔀

### 5.1 Merge Feature 1

1. Switch to main and pull latest:
   ```bash
   git switch main
   git pull origin main
   ```

2. Merge feature branch:
   ```bash
   git merge --no-ff feature/add-new-component -m "Merge feature: add new component"
   ```

3. Push to main:
   ```bash
   git push origin main
   ```

### 5.2 Merge Feature 2

1. Ensure main is up to date:
   ```bash
   git switch main
   git pull origin main
   ```

2. Merge feature branch:
   ```bash
   git merge --no-ff feature/improve-styling -m "Merge feature: improve styling"
   ```

3. Push to main:
   ```bash
   git push origin main
   ```

### 5.3 Merge Feature 3

1. Ensure main is up to date:
   ```bash
   git switch main
   git pull origin main
   ```

2. Merge feature branch:
   ```bash
   git merge --no-ff feature/add-animations -m "Merge feature: add animations"
   ```

3. Push to main:
   ```bash
   git push origin main
   ```

**Best Practices Demonstrated:**
- Using `--no-ff` to preserve branch history
- Meaningful commit messages
- Merging one feature at a time
- Pulling latest changes before merging

---

## Step 6: Clean Up Branches 🧹

After merging, clean up local and remote branches:

```bash
# Delete local branches
git branch -d feature/add-new-component
git branch -d feature/improve-styling
git branch -d feature/add-animations

# Delete remote branches
git push origin --delete feature/add-new-component
git push origin --delete feature/improve-styling
git push origin --delete feature/add-animations
```

---

## Step 7: View Result in Vercel 🌐

1. Go to your Vercel dashboard
2. Vercel automatically detects the new commits on `main`
3. A new deployment will be triggered automatically
4. Wait for the deployment to complete
5. Visit your live site - you'll see all the merged features!

**This demonstrates:**
- How changes flow from development → GitHub → Vercel
- Automatic deployments on merge to main
- The complete CI/CD workflow

---

## 🏗️ Activity #2: Advanced Multi-Agent Challenge

Now it's time to put your multi-agent workflow skills into practice! This activity simulates real-world development where multiple team members work on different parts of an application simultaneously.

### Your Mission:

Create and merge at least **3 different feature branches**, each implementing a distinct improvement to your app:

**Suggested Features (choose 3 or create your own):**

1. **Dark Mode Toggle** 🌙
   - Create a branch: `feature/dark-mode`
   - Add a toggle button to switch between light and dark themes
   - Use Cursor to implement theme switching with CSS variables or Tailwind classes

2. **Animation Enhancements** ✨
   - Create a branch: `feature/animations`
   - Add smooth transitions to existing elements
   - Implement hover effects, loading animations, or page transitions

3. **Responsive Design** 📱
   - Create a branch: `feature/responsive`
   - Improve mobile responsiveness
   - Add breakpoints and adjust layouts for different screen sizes

4. **New Component** 🧩
   - Create a branch: `feature/new-component`
   - Add a completely new section or feature to your app
   - Examples: footer, testimonials section, contact form, data visualization

5. **Performance Optimization** ⚡
   - Create a branch: `feature/performance`
   - Optimize images, implement lazy loading
   - Add code splitting or minimize bundle size

### Requirements:

✅ Create at least 3 feature branches  
✅ Make meaningful commits with clear messages  
✅ Push all branches to GitHub  
✅ View your branch network on GitHub  
✅ Merge branches one at a time following best practices  
✅ Resolve any merge conflicts if they arise  
✅ Clean up branches after merging  
✅ Verify deployment on Vercel  

---
## 🎓 Tips for Success

- **Take your time** with each step - don't rush!
- **Experiment** with different designs and components
- **Ask questions** if you get stuck
- **Save your work** frequently (git commits!)
- **Use branches** for every feature - it's a best practice!
- **Review code** before merging
- **Have fun** - this is your chance to be creative!

---