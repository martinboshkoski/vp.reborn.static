# Ваш Пријател - Production Deployment

This repository contains the **production build** of the Ваш Пријател (Your Friend) insurance website, ready for deployment to cPanel shared hosting.

## 🎯 Purpose

This is a deployment-only repository containing static files built from the main project. It contains:
- Production-optimized JavaScript, CSS, and HTML
- `.htaccess` file for Apache/cPanel SPA routing
- Static assets (images, fonts, etc.)

## 📁 Contents

```
vp-deploy/
├── .htaccess           # Apache rewrite rules for React Router
├── index.html          # Main HTML file
├── assets/             # Compiled JS, CSS, images
├── favicon.ico
└── robots.txt
```

## 🚀 Deployment to cPanel

### Initial Setup

1. **Create GitHub repository** for this deployment folder:
   ```bash
   git remote add origin https://github.com/YOUR-USERNAME/vp-deploy.git
   git push -u origin main
   ```

2. **Connect to cPanel Git™ Version Control**:
   - Login to cPanel
   - Navigate to **Git™ Version Control**
   - Click **Create**
   - Clone URL: `https://github.com/YOUR-USERNAME/vp-deploy.git`
   - Repository Path: `public_html` (or subdirectory for staging)
   - Enable **Pull or Deploy**

3. **Deploy**: In cPanel Git™, click **Pull or Deploy**

### Updating Deployment

From the main project directory (`vash-prijatel-reborn/`):

```bash
# Run the automated deployment script
./deploy.sh

# Then push to GitHub
cd ../vp-deploy
git push

# Pull in cPanel Git™ Version Control
```

## ⚠️ Important Notes

- **Do NOT edit files directly** in this repository
- All changes must be made in the main project (`vash-prijatel-reborn`)
- This repo is auto-generated from `npm run build`
- The `.htaccess` file is critical for SPA routing - do not remove

## 🔗 Main Project

Source code: [vash-prijatel-reborn](../vash-prijatel-reborn/)

## 📋 Requirements

- Apache web server (cPanel shared hosting)
- mod_rewrite enabled (for `.htaccess`)
- No Node.js or build tools required on server

## 🌐 Live Site

After deployment, the site will be available at your configured domain.
