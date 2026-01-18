# GitHub Pages Deployment Guide

## Step-by-Step Instructions to Upload to GitHub

### 1. Create a GitHub Repository

1. Go to [GitHub](https://github.com) and log in
2. Click the **"+"** icon in the top right corner
3. Select **"New repository"**
4. Fill in the details:
   - **Repository name**: `Malaysia_IAU` (or any name you prefer)
   - **Description**: "IAU Symposium 377 Monsoon School Website"
   - **Visibility**: Select **Public** (required for free GitHub Pages)
   - **DO NOT** initialize with README, .gitignore, or license (we already have these)
5. Click **"Create repository"**

### 2. Push Your Local Repository to GitHub

After creating the repository, GitHub will show you commands. Use these commands in your terminal:

```bash
cd /Users/yting/Malaysia_IAU

# Add the GitHub repository as remote
git remote add origin https://github.com/YOUR_USERNAME/Malaysia_IAU.git

# Push to GitHub
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username.

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (in the repository menu)
3. Scroll down and click **Pages** (in the left sidebar)
4. Under "Build and deployment":
   - **Source**: Select "Deploy from a branch"
   - **Branch**: Select `main` and `/ (root)`
   - Click **Save**
5. Wait a few minutes for deployment

### 4. Access Your Website

Your website will be available at:
```
https://YOUR_USERNAME.github.io/Malaysia_IAU/
```

The main pages:
- Main conference: `https://YOUR_USERNAME.github.io/Malaysia_IAU/index.html`
- Monsoon school: `https://YOUR_USERNAME.github.io/Malaysia_IAU/monsoon_school.html`

---

## What Was Optimized

### ✅ Repository Size Reduction: 79% (545MB → 113MB)

1. **Videos Compressed** (115MB → 40MB):
   - `icube.mp4`: 50MB → 2.7MB
   - `kuala_lumpur.mp4`: 55MB → 34MB
   - `auditorium_dk_f.mp4`: 10MB → 2.6MB

2. **Images Optimized**:
   - Converted TIF files to JPG (venue_17.tif, venue_18.tif)
   - Compressed all images >1MB to 85% quality
   - Resized images to max 1920px width/height
   - All large images reduced significantly

3. **Files Removed**:
   - `Template.zip` (unnecessary)
   - `css/main.styl` (source file, not needed)

4. **Files Added**:
   - `README.md` - Documentation
   - `.gitignore` - Git configuration
   - `DEPLOYMENT.md` - This file

### ✅ All Functionality Preserved

- ✓ All HTML pages work correctly
- ✓ All CSS and JavaScript intact
- ✓ All images display properly
- ✓ All videos playable
- ✓ All navigation and interactive features functional
- ✓ Photo galleries work
- ✓ Responsive design maintained

---

## Troubleshooting

### If the website doesn't load:
1. Make sure GitHub Pages is enabled (Settings → Pages)
2. Wait 2-5 minutes after first deployment
3. Check that the branch is set to `main` (or `master`)
4. Ensure repository is **Public**

### If videos don't play:
- Videos are compressed but should play in all modern browsers
- If quality is an issue, you can re-compress with higher quality (lower CRF value)

### If you need to update the website:
```bash
# Make your changes, then:
git add -A
git commit -m "Description of changes"
git push origin main
```

GitHub Pages will automatically rebuild (takes 1-2 minutes).

---

## Repository Structure

```
Malaysia_IAU/
├── index.html              # Main conference page
├── monsoon_school.html     # Monsoon school page
├── README.md               # Project documentation
├── DEPLOYMENT.md           # This file
├── .gitignore             # Git ignore rules
├── css/                   # Stylesheets
├── js/                    # JavaScript files
├── img/                   # Images and media
│   ├── gallery/           # Photo gallery
│   ├── speakers/          # Speaker photos
│   ├── sponsors/          # Sponsor logos
│   ├── IAUS_2023/        # Conference photos
│   ├── IAUS_Monsoon_School_2023/  # School photos
│   └── ...
└── video/                 # Video files (compressed)
```

---

## Next Steps

1. **Push to GitHub** using the commands above
2. **Enable GitHub Pages** in repository settings
3. **Share your link**: `https://YOUR_USERNAME.github.io/Malaysia_IAU/`
4. **Optional**: Set up a custom domain (see GitHub Pages docs)

---

## Questions?

Contact the website maintainer or refer to:
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Git Documentation](https://git-scm.com/doc)
