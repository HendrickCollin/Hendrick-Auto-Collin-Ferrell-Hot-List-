# Hendrick BMW Hot List — Deploy Instructions

## What you have

A complete, ready-to-deploy web app. When live, it'll work on your phone exactly like a native app — bookmark it on your home screen and it opens fullscreen.

## Step-by-step deploy (Vercel drag-and-drop)

You'll do this once. Total time: about 5 minutes.

### 1. Delete the broken project on Vercel

- Go to vercel.com and log in
- Open your "hot-l-ist" project
- Click **Settings** (top right of the project page)
- Scroll to the bottom — there's a red "Delete Project" button
- Confirm the delete

(You're not deleting your account — just this one broken project so we can replace it cleanly.)

### 2. Create a new project — drag-and-drop method

- From your Vercel dashboard, click **Add New** → **Project**
- Look for the option that says something like **"Deploy Without Git"** or **"Browse all templates"** — there should be a way to upload a folder directly
- If you can't find it, the easier alternative is in Step 2B below

### 2B. Easier alternative if Step 2 looks confusing

Vercel sometimes hides the upload option. The reliable path:

- Go to **vercel.com/new**
- Look for a button that says **"Browse"** or **"Upload"** — it lets you upload a folder
- If you genuinely can't find it (Vercel's UI changes), just message me back with a screenshot and I'll tell you the current button location

### 3. Upload this folder

- Select the **entire folder** (the one called `hot-list-project`) — not just the files inside it
- Vercel will see `package.json` and automatically know what to do
- It'll detect "Vite" as the framework — leave all defaults alone
- Click **Deploy**

### 4. Wait ~60 seconds

You'll see logs scrolling by. Vercel is:
- Installing the React libraries
- Compiling the JSX into a real website
- Putting it live on a URL

When it finishes, you'll see a **"Visit"** or "Open Site" button.

### 5. Bookmark it on your phone

- Open the URL on your phone (Safari on iPhone, Chrome on Android)
- iPhone: tap the share icon → **"Add to Home Screen"**
- Android: tap the menu → **"Add to Home screen"**
- It'll now have a 🔥 icon and open fullscreen, just like a real app

## How it saves your data

This version uses **browser storage** — your leads, scores, and activity all save to your device automatically. You don't have to push a save button. Don't clear your browser data without exporting first.

**Important:** because data is stored on the device, your leads on your phone won't sync to your laptop or vice-versa. If you want to use this on multiple devices, you'd need to export the CSV from one device and import it on the other. (Or we can build cloud sync later — but that requires a database and is a bigger lift.)

## If something breaks

- Screenshot whatever you're seeing
- Tell me what you tried
- I'll fix it

## What to do after it's live

The first time you open the live app, it'll be empty (it's not connected to the version you've been using in Claude — different storage). To bring your leads in:

1. In Claude, open the hot list, tap ⋮ → Export CSV (downloads to your computer)
2. Open the live app, tap ⋮ → Import CSV → upload that file
3. Done — every lead with their full activity history carries over

That's also how you'd back up data on the live version going forward — just hit Export every week or two.
