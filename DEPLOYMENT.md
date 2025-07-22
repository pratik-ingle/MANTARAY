# 🚀 GitHub Pages Deployment Guide

Follow these steps to deploy your MANTA-RAY research webpage to GitHub Pages:

## Prerequisites

- GitHub account
- Git installed on your computer
- All files ready in your local repository

## Step 1: Create GitHub Repository

1. Go to [GitHub.com](https://github.com) and sign in
2. Click the "+" icon in the top right → "New repository"
3. Repository name: `manta-ray-research` (or your preferred name)
4. Description: "MANTA-RAY: Advanced Soft Surface Manipulation System"
5. Make it **Public** (required for free GitHub Pages)
6. **DO NOT** initialize with README (we already have one)
7. Click "Create repository"

## Step 2: Add Large Files to Git LFS (Important!)

Since your videos and PDFs are large files, you need Git LFS:

```bash
# Install Git LFS (if not already installed)
# On macOS with Homebrew:
brew install git-lfs

# On Ubuntu/Debian:
sudo apt-get install git-lfs

# Initialize Git LFS in your repository
git lfs install

# Add large files to LFS tracking
git lfs track "*.mp4"
git lfs track "*.pdf"

# Add and commit the LFS configuration
git add .gitattributes
git commit -m "Configure Git LFS for large files"
```

## Step 3: Add Your Large Files

```bash
# Add the PDF files
git add "Case 2025 Arxiv (1).pdf"
git add "Soft Surface Manipulation Sub (5).pdf"

# Add the video files
git add case25.mp4
git add robosoft25.mp4

# Commit the large files
git commit -m "Add research papers and demonstration videos"
```

## Step 4: Connect to GitHub

```bash
# Add your GitHub repository as remote (replace with your actual repository URL)
git remote add origin https://github.com/YOUR_USERNAME/manta-ray-research.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Step 5: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings** tab
3. Scroll down to **Pages** in the left sidebar
4. Under "Source", select **Deploy from a branch**
5. Choose **main** branch
6. Choose **/ (root)** folder
7. Click **Save**

## Step 6: Wait for Deployment

- GitHub will build and deploy your site
- This usually takes 1-5 minutes
- You'll see a green checkmark when it's ready
- Your site will be available at: `https://YOUR_USERNAME.github.io/manta-ray-research`

## Step 7: Update Content (Important!)

After deployment, update the placeholders in `index.html`:

1. Replace `[Author Names]` with actual author names
2. Replace `[University/Institution Names]` with real affiliations
3. Update the abstract with content from your PDFs
4. Update results with actual data from your research
5. Add contact email address
6. Update citation information

## 📋 Checklist

- [ ] Repository created on GitHub
- [ ] Git LFS configured for large files
- [ ] All files committed and pushed
- [ ] GitHub Pages enabled
- [ ] Website accessible via GitHub Pages URL
- [ ] Content updated with real information
- [ ] Videos playing correctly
- [ ] PDF downloads working
- [ ] Mobile responsiveness tested

## 🔧 Troubleshooting

### Large File Issues

If you get errors about large files:

- Ensure Git LFS is properly configured
- Check that `.gitattributes` includes your file types
- Use `git lfs push origin main` for LFS files

### Videos Not Playing

- Ensure video files are properly committed with LFS
- Check browser compatibility (MP4 should work in all modern browsers)
- Verify file paths in HTML are correct

### CSS/Styling Issues

- Hard refresh the page (Ctrl+F5 or Cmd+Shift+R)
- Check browser developer tools for any errors
- Ensure all CSS is inline (no external dependencies except Font Awesome)

## 🎯 Next Steps

1. Share your GitHub Pages URL with colleagues
2. Consider adding Google Analytics for visitor tracking
3. Set up a custom domain if desired
4. Add more interactive features if needed

## 📞 Support

If you encounter issues:

1. Check GitHub Pages documentation
2. Verify all files are properly committed
3. Test the website locally by opening `index.html` in a browser
4. Check the Actions tab in your GitHub repository for build errors

---

**Your website will be live at:** `https://YOUR_USERNAME.github.io/REPOSITORY_NAME`
