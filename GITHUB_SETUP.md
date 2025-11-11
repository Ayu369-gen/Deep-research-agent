# GitHub Repository Setup Guide

Your local repository is ready! Follow these steps to push it to GitHub.

## Step 1: Create Repository on GitHub

1. Go to [GitHub.com](https://github.com) and sign in
2. Click the **"+"** icon in the top right corner
3. Select **"New repository"**
4. Fill in the details:
   - **Repository name**: `Deep-research-agent`
   - **Description**: "An AI-powered research agent that performs comprehensive web research"
   - **Visibility**: Choose Public or Private
   - **DO NOT** initialize with README, .gitignore, or license (we already have these)
5. Click **"Create repository"**

## Step 2: Connect Local Repository to GitHub

After creating the repository, GitHub will show you commands. Use these commands in your terminal:

```powershell
# Navigate to your project directory (if not already there)
cd "C:\Users\nlohi\OneDrive\movie\Documents\GitHub\Deep-research-agent"

# Add the remote repository (replace with your actual GitHub username if different)
git remote add origin https://github.com/Ayu369-gen/Deep-research-agent.git

# Verify the remote was added
git remote -v

# Push your code to GitHub
git branch -M main
git push -u origin main
```

## Alternative: Using SSH (if you have SSH keys set up)

If you prefer SSH instead of HTTPS:

```powershell
git remote add origin git@github.com:Ayu369-gen/Deep-research-agent.git
git branch -M main
git push -u origin main
```

## Step 3: Verify

1. Go to your repository on GitHub: `https://github.com/Ayu369-gen/Deep-research-agent`
2. You should see all your files:
   - `agent.py`
   - `README.md`
   - `requirements.txt`
   - `.gitignore`

## Troubleshooting

### If you get authentication errors:
- For HTTPS: GitHub may prompt for credentials. Use a Personal Access Token instead of password
- Create a token: GitHub Settings → Developer settings → Personal access tokens → Tokens (classic)
- Or use GitHub Desktop for easier authentication

### If the repository already exists:
```powershell
git remote set-url origin https://github.com/Ayu369-gen/Deep-research-agent.git
git push -u origin main
```

### If you need to rename the branch:
```powershell
git branch -M main  # Renames master to main (if needed)
```

## Next Steps

After pushing:
- ✅ Your repository is live on GitHub
- ✅ Others can clone it using: `git clone https://github.com/Ayu369-gen/Deep-research-agent.git`
- ✅ You can continue making changes and pushing updates

## Future Updates

When you make changes to your code:

```powershell
git add .
git commit -m "Your commit message"
git push
```

