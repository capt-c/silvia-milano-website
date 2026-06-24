# Deploying your website — step-by-step guide

**You only need to do this once. It takes about 20 minutes.**
No coding required — just clicking through web interfaces.

---

## What you'll set up

| Service | What it does | Cost |
|---|---|---|
| **GitHub** | Stores your website files | Free |
| **Netlify** | Builds and hosts the site | Free |
| **Your domain registrar** | Points your domain to Netlify | You already pay for this |
| **Decap CMS** (/admin) | Lets you edit content visually | Free |

---

## Step 1 — Create a GitHub account

1. Go to [github.com](https://github.com) and click **Sign up**
2. Choose a username (e.g. `silvia-milano`) and create your account
3. Verify your email

---

## Step 2 — Upload your site to GitHub

1. After logging in to GitHub, click the **+** icon (top right) → **New repository**
2. Name it `silvia-milano-website` (or anything you like)
3. Set it to **Private** (recommended) and click **Create repository**
4. On the next screen, click **uploading an existing file**
5. Drag the entire `silvia-milano-site` folder contents into the upload area
6. Click **Commit changes**

---

## Step 3 — Connect Netlify

1. Go to [netlify.com](https://netlify.com) and click **Sign up** → choose **Sign up with GitHub**
2. Click **Add new site** → **Import an existing project** → **GitHub**
3. Authorise Netlify and select your `silvia-milano-website` repository
4. Netlify will auto-detect the settings from `netlify.toml`. Click **Deploy site**
5. In ~1 minute your site will be live at a temporary URL like `https://random-name-123.netlify.app`

---

## Step 4 — Connect your domain

1. In Netlify, go to **Site settings** → **Domain management** → **Add custom domain**
2. Enter `silvia-milano.com` (or your actual domain)
3. Netlify will show you **DNS records** to add
4. Log in to your domain registrar and update the DNS settings to point to Netlify
   - Usually you add two records: an `A` record and a `CNAME` for `www`
   - Netlify provides the exact values
5. DNS propagation takes 1–24 hours, then your site is live at your domain with a free SSL certificate

---

## Step 5 — Enable the visual editor (/admin)

This gives you a login page at `yoursite.com/admin` where you can edit content without touching code.

1. In Netlify, go to **Site configuration** → **Identity** → **Enable Identity**
2. Under Identity settings → **Registration** → set to **Invite only** (so only you can log in)
3. Go to **Identity** → **Services** → **Git Gateway** → click **Enable Git Gateway**
4. Under **Identity**, click **Invite users** and invite yourself using your email
5. You'll receive an email — click the link to set your password
6. Done! Visit `yoursite.com/admin` to log in and edit your content

---

## Adding your photo

1. Save your photo as `silvia-milano.jpg` (or any name)
2. In the `/admin` editor, go to **Site settings → About & Bio**
3. Upload your photo using the photo field
4. Alternatively, put the file in `assets/img/` via GitHub and update `_data/about.yml`

---

## Updating content after setup

**Option A — Visual editor (recommended):** Go to `yoursite.com/admin`, log in, and edit.

**Option B — Ask Claude:** Open Cowork, describe what you want to change, and I'll update the files for you.

---

## Adding your CV PDF

Drop your CV as `cv.pdf` into the `assets/` folder. The "CV" link in the navigation will point to it automatically.

---

## Questions?

If anything doesn't work, come back to Cowork and describe the problem — I'll help you sort it out.
