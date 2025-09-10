# Devops-documentation


---

### 🧱 Step-by-Step: Clone and Push to Your Own GitHub Repo

1. **Clone the Original Repo Locally**
   ```bash
   git clone https://github.com/username/original-repo.git
   cd original-repo
   ```

2. **Remove the Existing Git Remote**
   ```bash
   git remote remove origin
   ```

3. **Create a New Repo on Your GitHub Account**
   - Go to [GitHub New Repo](https://github.com/new)
   - Name it whatever you like (e.g., `my-rebranded-project`)
   - Do **not** initialize with README or license

4. **Add Your New Repo as Remote**
   ```bash
   git remote add origin https://github.com/yourusername/my-rebranded-project.git
   ```

5. **Push the Code to Your Repo**
   ```bash
   git push -u origin main
   ```
   > If the original repo uses `master`, replace `main` with `master`.

---
=================================================================================
 **start fresh without showing any of the original commits**, here’s how to do it:

---

### 🧹 Create a Clean Repo Without Previous Commits

1. **Clone the original repo**
   ```bash
   git clone https://github.com/username/original-repo.git
   cd original-repo
   ```

2. **Remove Git history**
   ```bash
   rm -rf .git
   ```

3. **Reinitialize Git**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   ```

4. **Create a new repo on your GitHub account**, then:
   ```bash
   git remote add origin https://github.com/yourusername/new-repo.git
   git push -u origin main
   ```

---

### ✅ Result:
- The code will be the same.
- The commit history will start from your own initial commit.
- No trace of the original author or repo will be visible in Git logs.

---

Let me know if you want to automate this process with a shell script or integrate it into a CI/CD pipeline. I can help you make it modular and reusable for future repo sanitization.
