# Deployment Guide

Quick steps to get SnapID Studio live on the internet.

## Prerequisites

1. **GitHub Account** — [github.com/signup](https://github.com/signup)
2. **Vercel Account** (Free) — [vercel.com](https://vercel.com)
3. **Domain Name** (Optional) — Namecheap, Google Domains, etc. (~$10–15/year)

---

## Step 1: Create a GitHub Repository

### A. Create on GitHub.com

1. Go to [github.com/new](https://github.com/new)
2. **Repository name:** `snapid-studio`
3. **Description:** "AI-powered document photo resizer"
4. **Public** (so others can discover it)
5. Click **Create Repository**
6. You'll see a setup screen with your repo URL

### B. Push Files to GitHub

Once you have the repo URL (e.g., `https://github.com/yourusername/snapid-studio.git`):

```bash
cd /home/claude/snapid-studio

# Add the remote repository
git remote add origin https://github.com/yourusername/snapid-studio.git

# Verify it's added
git remote -v

# Add all files
git add .

# Create first commit
git commit -m "Initial commit: SnapID Studio v1.0"

# Push to GitHub
git branch -M main
git push -u origin main
```

**Done!** Your code is now on GitHub.

---

## Step 2: Deploy to Vercel

### A. Connect Vercel to GitHub

1. Go to [vercel.com](https://vercel.com)
2. Click **Sign Up** and choose **Continue with GitHub**
3. Authorize Vercel to access your GitHub account
4. Click **Add New Project**
5. Find `snapid-studio` in the list and click **Import**

### B. Configure (Keep Defaults)

Vercel will auto-detect settings:
- **Framework Preset:** None (static site)
- **Root Directory:** `.`
- **Build Command:** (empty)
- **Output Directory:** (empty)

Click **Deploy** — it will build and deploy in ~30 seconds.

### C. Get Your Live URL

After deployment, you'll see:
- **Live URL:** `https://snapid-studio.vercel.app`
- Share this link! It's live now.

---

## Step 3: Add Custom Domain (Optional)

If you bought a domain (e.g., `snapid.app`):

### A. In Vercel Dashboard

1. Open your SnapID Studio project
2. Go to **Settings** → **Domains**
3. Add your domain name (e.g., `snapid.app`)
4. Vercel shows you **DNS records** to add

### B. Update DNS at Your Registrar

1. Log into your domain registrar (Namecheap, Google Domains, etc.)
2. Find **DNS Settings** or **Nameservers**
3. Add the records Vercel provided
4. Wait 24–48 hours for DNS to propagate

**Done!** Your app is now at `https://snapid.app` (or your domain).

---

## Step 4: Updates & Maintenance

From now on, updates are automatic:

```bash
# Make changes to index.html locally
# Test in browser

# Commit and push
git add .
git commit -m "Update: Add new countries"
git push origin main

# Vercel auto-deploys! ✨
# Your live site updates in ~1 minute
```

---

## Troubleshooting

### "git: command not found"
Install Git from [git-scm.com](https://git-scm.com)

### "Permission denied" when pushing
1. Check you're using HTTPS clone URL (not SSH)
2. Use a Personal Access Token instead of password:
   - [github.com/settings/tokens](https://github.com/settings/tokens)
   - Generate "repo" token
   - Use token as password when prompted

### "Deployment failed" on Vercel
1. Check Vercel build logs (red error message)
2. Common fix: Ensure `index.html` exists in root
3. Reload project or re-import from GitHub

### Custom domain not resolving
1. Verify DNS records were added correctly
2. Use [dns-lookup.com](https://dns-lookup.com) to check
3. Wait 24–48 hours; DNS caches globally

---

## Next Steps

After launch:

1. **Tell people** — Share on Twitter, Reddit, Product Hunt, etc.
2. **Collect feedback** — Add GitHub Issues for bug reports
3. **Monitor usage** — Check Vercel Analytics dashboard
4. **Add binaries** — Create & host desktop .exe and .dmg files
5. **Update specs** — Add new countries based on user requests

---

## Deployment Checklist

- [ ] Create GitHub account
- [ ] Create repository `snapid-studio`
- [ ] Push files with `git push`
- [ ] Connect Vercel to GitHub
- [ ] Deploy to Vercel
- [ ] Get live URL (`https://snapid-studio.vercel.app`)
- [ ] (Optional) Buy domain name
- [ ] (Optional) Update DNS records in domain registrar
- [ ] (Optional) Add custom domain to Vercel
- [ ] Test live app in browser
- [ ] Share link with others

---

**Need help?** See the main [README.md](README.md) or open a GitHub issue.
