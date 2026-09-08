# New Bern Collection — Placeholder Site

A clean, responsive placeholder site for **newberncollection.com**.

## Quick Links
- **Domain**: [newberncollection.com](https://newberncollection.com)
- **Contact Email**: `team@newberncollection.com`

---

## Deployment & Hosting Workflow (GitHub Pages + Squarespace)

### 1. Push to GitHub
Repository: `https://github.com/allenmask/new-bern-collection.git`

```bash
cd /Users/allenmask/newberncollection-site
git add .
git commit -m "Update placeholder site"
git push origin main
```

### 2. Enable GitHub Pages
1. Go to your repository settings: `https://github.com/allenmask/new-bern-collection/settings/pages`
2. Under **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: `main` / `/ (root)`
   - Click **Save**
3. Under **Custom domain**:
   - Enter: `newberncollection.com`
   - Click **Save** (this will verify the `CNAME` file in this repo)
   - Check **Enforce HTTPS** (once DNS has propagated)

---

## Squarespace DNS Configuration

In your Squarespace account:
1. Navigate to **Domains** -> click `newberncollection.com` -> **DNS Settings**.
2. Add the **4 GitHub Pages Apex A Records**:
   - **Type**: `A` | **Host**: `@` | **Data**: `185.199.108.153`
   - **Type**: `A` | **Host**: `@` | **Data**: `185.199.109.153`
   - **Type**: `A` | **Host**: `@` | **Data**: `185.199.110.153`
   - **Type**: `A` | **Host**: `@` | **Data**: `185.199.111.153`
3. Add the **CNAME Record**:
   - **Type**: `CNAME` | **Host**: `www` | **Data**: `allenmask.github.io.`

---

## Email Forwarding Setup (team@newberncollection.com -> Gmail)

Squarespace Domains includes free email forwarding:
1. In Squarespace, go to **Domains** -> select `newberncollection.com`.
2. Click **Email** (or **Email Forwarding** in the left sidebar).
3. Click **Add Rule** (or **Add Forward**):
   - **Alias / Forward from**: `team` (making it `team@newberncollection.com`)
   - **Forward to**: your personal `@gmail.com` address.
4. Squarespace will send a verification email to your Gmail address.
5. Open your Gmail, click the **Verify** confirmation link, and forwarding will be active immediately.
