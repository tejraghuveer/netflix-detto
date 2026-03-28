# Netflix Clone

A Netflix clone built with HTML, CSS, JavaScript, and Firebase Authentication.

## Features

- Firebase Authentication (Login/Signup)
- Netflix-style UI with movie rows
- Responsive design
- Hero banner with featured content
- Horizontal scrolling movie categories

## Live Demo

**Website:** https://netflix-clone-8c661.web.app

## Project Structure

```
netflix-clone/
├── index.html              # Main HTML file
├── css/
│   └── style.css          # Netflix-style styling
├── js/
│   ├── firebase-config.js # Firebase configuration
│   ├── auth-compat.js     # Authentication logic
│   ├── app.js             # Main app logic
│   └── movies.js          # Movie data
├── .github/
│   └── workflows/
│       └── deploy.yml     # GitHub Actions deployment
├── firebase.json          # Firebase hosting config
└── .firebaserc            # Firebase project settings
```

## Setup Instructions

### 1. Clone and Push to GitHub

```bash
# Navigate to your project
cd netflix-clone

# Initialize git (if not already)
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit"

# Create GitHub repo and push
git remote add origin https://github.com/YOUR_USERNAME/netflix-clone.git
git branch -M main
git push -u origin main
```

### 2. Setup GitHub Secrets for Firebase

You need to add a Firebase service account key to GitHub Secrets:

1. Go to [Firebase Console](https://console.firebase.google.com/project/netflix-clone-8c661/settings/serviceaccounts)
2. Click **"Generate new private key"**
3. Download the JSON file
4. Open it and copy the entire contents
5. Go to your GitHub repo → **Settings** → **Secrets and variables** → **Actions**
6. Click **"New repository secret"**
7. Name: `FIREBASE_SERVICE_ACCOUNT`
8. Paste the JSON content and save

### 3. Enable GitHub Actions

1. Go to your GitHub repo → **Actions** tab
2. Click **"I understand my workflows, go ahead and enable them"**

### 4. Deploy

Every time you push to `main`, it will automatically deploy to Firebase Hosting!

## Manual Deploy (Alternative)

If you prefer manual deployment:

```bash
# Install Firebase CLI
npm install -g firebase-tools

# Login
firebase login

# Deploy
cd netflix-clone
firebase deploy --only hosting
```

## Firebase Configuration

Your Firebase project is already configured with:
- **Project ID:** netflix-clone-8c661
- **Authentication:** Email/Password enabled
- **Hosting:** Configured for single-page app

## Troubleshooting

### Login not working?
- Check Firebase Console → Authentication → Sign-in method → Email/Password is enabled
- Check that your domain is in Authorized domains

### Deployment failed?
- Make sure `FIREBASE_SERVICE_ACCOUNT` secret is set correctly
- Check GitHub Actions logs for errors

## Technologies Used

- HTML5
- CSS3
- JavaScript (ES6)
- Firebase Authentication
- Firebase Hosting
- Font Awesome Icons

## License

MIT
