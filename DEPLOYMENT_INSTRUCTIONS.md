# Deploying to GitHub Pages

## Step 1: Create a GitHub Repository

1. Go to https://github.com and log in
2. Click the "+" icon in the top right, select "New repository"
3. Name it: `usda-loan-guide` (or any name you prefer)
4. Make it **Public** (required for free GitHub Pages)
5. Don't initialize with README (we have our own)
6. Click "Create repository"

## Step 2: Upload Your Files

### Option A: Using Git (Command Line)

```bash
# Navigate to the outputs folder
cd /mnt/user-data/outputs

# Initialize git repository
git init

# Add all files
git add README.md index.html USDA_Loan_Guide_Presentation.html USDA_Guaranteed_Loan_Complete_Guide.pdf USDA_Guaranteed_Loan_Complete_Guide.md

# Commit the files
git commit -m "Initial commit: USDA Loan Guide"

# Add your GitHub repository as remote
git remote add origin https://github.com/remmylee/usda-loan-guide.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Option B: Using GitHub Web Interface (Easier)

1. On your new repository page, click "uploading an existing file"
2. Drag and drop these files:
   - `index.html`
   - `USDA_Loan_Guide_Presentation.html`
   - `USDA_Guaranteed_Loan_Complete_Guide.pdf`
   - `USDA_Guaranteed_Loan_Complete_Guide.md`
   - `README.md`
3. Click "Commit changes"

## Step 3: Enable GitHub Pages

1. In your repository, click "Settings" (top menu)
2. Click "Pages" in the left sidebar
3. Under "Source", select:
   - Branch: `main`
   - Folder: `/ (root)`
4. Click "Save"
5. Wait 1-2 minutes for deployment

## Step 4: Access Your Site

Your site will be available at:
```
https://remmylee.github.io/usda-loan-guide/
```

## File Structure

```
usda-loan-guide/
├── index.html                                    # Landing page
├── USDA_Loan_Guide_Presentation.html            # Interactive presentation
├── USDA_Guaranteed_Loan_Complete_Guide.pdf      # PDF guide
├── USDA_Guaranteed_Loan_Complete_Guide.md       # Markdown source
└── README.md                                     # Repository info
```

## URLs After Deployment

- **Landing Page**: `https://remmylee.github.io/usda-loan-guide/`
- **Presentation**: `https://remmylee.github.io/usda-loan-guide/USDA_Loan_Guide_Presentation.html`
- **PDF Download**: `https://remmylee.github.io/usda-loan-guide/USDA_Guaranteed_Loan_Complete_Guide.pdf`

## Updating Content

To update the site:

### Using Git:
```bash
# Make your changes to files
# Then:
git add .
git commit -m "Updated content"
git push
```

### Using Web Interface:
1. Navigate to the file in your repository
2. Click the pencil icon to edit
3. Make changes
4. Scroll down and click "Commit changes"

Changes go live in 1-2 minutes.

## Custom Domain (Optional)

To use a custom domain like `usdaloan.yourdomain.com`:

1. In repository Settings → Pages
2. Enter your custom domain
3. Add a CNAME record in your domain's DNS settings pointing to:
   ```
   remmylee.github.io
   ```

## Troubleshooting

### Site Not Loading?
- Wait 2-3 minutes after enabling Pages
- Check Settings → Pages for deployment status
- Ensure repository is Public

### 404 Error?
- Verify file names match exactly (case-sensitive)
- Check that `index.html` exists in root
- Confirm GitHub Pages is enabled

### Fonts Not Loading?
- The presentation uses Google Fonts (requires internet)
- Fonts load automatically when viewing online

## Security Note

GitHub Pages is:
- ✅ Free for public repositories
- ✅ Automatically SSL/HTTPS enabled
- ✅ Fast CDN delivery worldwide
- ✅ No server maintenance required

Your site is static HTML (no backend), so it's inherently secure.

---

**Your guide will be live and accessible to anyone worldwide!**
