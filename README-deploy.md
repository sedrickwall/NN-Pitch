Deploying NN-Pitch
===================

This file contains quick, copy-paste steps to deploy your static `sales_pitch.html` to Netlify, Vercel, or Surge.

Netlify (recommended for easy GitHub integration)
------------------------------------------------
1. Go to https://app.netlify.com and sign up / log in.
2. Click "Add new site" → "Import from Git" → connect GitHub and authorize.
3. Pick repository: `sedrickwall/NN-Pitch`.
4. Build settings:
   - Build command: (leave blank)
   - Publish directory: `/` (root)
5. Click "Deploy site". After deploy you'll get a public URL. Use the site settings to set a custom domain if desired.

Netlify manual (drag & drop)
1. Go to https://app.netlify.com/drop
2. Drag the project folder (or just `sales_pitch.html` plus assets), and deploy.

Vercel (recommended for instant previews)
-----------------------------------------
1. Sign in to https://vercel.com with GitHub.
2. Import Project → choose `sedrickwall/NN-Pitch`.
3. Framework Preset: "Other" / Static.
4. Output Directory: `/`.
5. Deploy. The `vercel.json` in the repo will route `/` to `/sales_pitch.html`.

Surge (one-liner)
------------------
Install and publish from your machine:

```bash
npm install -g surge
cd '/Users/sedrickw/Desktop/Personal Apps/NN-Pitch'
surge .
```

Firebase notes
--------------
- Your `sales_pitch.html` conditionally imports Firebase and expects a `firebaseConfig` object in `localStorage` or injected as `__firebase_config`. If you need Firebase features publicly accessible, set up a Firebase Web app and paste the config into the page or inject it on the server.
- If you use Firebase Authentication / Database, double-check security rules before making the site public.

Verification checklist
----------------------
- [ ] Visit the deployed URL and confirm the redirect to `sales_pitch.html` works.
- [ ] Test any interactive features (AI demo, Firebase calls).
- [ ] If something breaks, check the browser console for errors and confirm external resources (fonts, CDN) are reachable.