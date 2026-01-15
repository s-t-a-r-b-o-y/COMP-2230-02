# Creating a Personal Repository from Course Materials (Without Forking)

This guide explains how to create your own independent repository on GitHub using the course materials, without forking the original repository.

## Method 1: Clone and Push to New Repository

### Step 1: Clone the Course Repository Locally

Open your terminal and run:

```bash
git clone https://github.com/ShivaniTyagiCS2026/COMP-2230-02.git
cd COMP-2230-02
```

This downloads all the course materials to your local machine.

### Step 2: Create a New Repository on GitHub

1. Go to [GitHub.com](https://github.com) and sign in to your account
2. Click the **"+"** icon in the top-right corner
3. Select **"New repository"**
4. Give your repository a name (e.g., `COMP-2230-02-my-work`)
5. Make sure it's set to **Public** or **Private** as needed
6. **Do NOT** initialize with README, .gitignore, or license (since we're copying existing content)
7. Click **"Create repository"**

### Step 3: Connect Local Repository to Your New GitHub Repository

After creating the repository, GitHub will show you commands. Copy the repository URL (it will look like `https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git`).

In your terminal, run:

```bash
git remote set-url origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
```

### Step 4: Push the Code to Your Repository

```bash
git push -u origin main
```

This uploads all the course materials to your new repository.

## Method 2: Download ZIP and Upload to New Repository

### Step 1: Download the Course Materials

1. Go to the course repository: [COMP-2230-02](https://github.com/ShivaniTyagiCS2026/COMP-2230-02)
2. Click the **"Code"** button
3. Select **"Download ZIP"**
4. Save the ZIP file to your computer and extract it

### Step 2: Create a New Repository on GitHub

Follow the same steps as in Method 1, Step 2 above.

### Step 3: Upload Files to Your Repository

1. On your new repository page, click **"uploading an existing file"** (or drag and drop)
2. Drag all the extracted files into the upload area
3. Add a commit message like "Initial commit with course materials"
4. Click **"Commit changes"**

## Method 3: Using GitHub CLI (Advanced)

If you have GitHub CLI installed:

```bash
# Clone the repo
gh repo clone ShivaniTyagiCS2026/COMP-2230-02

# Create your own repo
gh repo create YOUR_REPO_NAME --public --source=. --push
```

## Important Notes

- **Choose a descriptive name** for your repository (e.g., `java-programming-course`, `comp2230-assignments`)
- **This creates an independent copy** - changes you make won't affect the original course repository
- **You can modify freely** - add your own code, notes, and assignments
- **Keep it organized** - consider creating branches for different assignments or labs

## Troubleshooting

- If you get permission errors, make sure you're signed in to GitHub
- If the push fails, try `git push --force origin main` (but be careful, this overwrites any existing content)
- Make sure you're using the correct repository URL from your new repo

## Next Steps

Once you have your personal repository:
1. Open it in GitHub Codespaces (see `github_codespaces_setup.md`)
2. Or clone it locally and work in your preferred IDE
3. Start working on the labs and assignments!

## Why Not Fork?

Forking creates a connection to the original repository, which is great for contributing back changes. However, for personal coursework where you want complete independence, creating a new repository gives you full control without the fork relationship.