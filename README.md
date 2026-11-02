# Evopix website

Download page for the Evopix Android photo editor, hosted at https://evopix.in with GitHub Pages.

## Files
- `index.html`: the page
- `CNAME`: points GitHub Pages at evopix.in
- `.nojekyll`: tells GitHub to serve the files as they are
- `evopix.apk`: **add your APK here** (the Download button links to this name)

## Publish on GitHub Pages
1. Create a new **public** repository on GitHub (for example `evopix-site`).
2. Click **Add file → Upload files**, drag in everything from this folder plus your `evopix.apk`, then **Commit changes**.
3. Go to **Settings → Pages**. Under *Build and deployment*, choose **Deploy from a branch**, branch **main**, folder **/ (root)**, and **Save**.
4. In the same Pages screen, the custom domain should show **evopix.in**. Tick **Enforce HTTPS** once it becomes available.

## Point evopix.in to GitHub (GoDaddy → My Products → evopix.in → DNS)
Delete any existing **A** record for `@` (and GoDaddy's "Parked" record), then add:

| Type  | Name | Value                  |
|-------|------|------------------------|
| A     | @    | 185.199.108.153        |
| A     | @    | 185.199.109.153        |
| A     | @    | 185.199.110.153        |
| A     | @    | 185.199.111.153        |
| CNAME | www  | YOUR-USERNAME.github.io |

DNS changes can take from a few minutes up to 24 hours.

## Updating the app
Upload the new APK with the same name `evopix.apk` (it replaces the old one), and edit the version number in `index.html`.
GitHub blocks files over 100 MB; if your APK is bigger, attach it to a GitHub Release instead and change the two `href="evopix.apk"` links to the release download link.
