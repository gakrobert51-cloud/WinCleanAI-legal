# WinCleanAI legal site

This folder is the complete public package for the WinCleanAI Privacy Policy and
End User License Agreement. It contains **only** legal text, static HTML, CSS,
and deployment instructions. It contains no application source code, binaries,
secrets, or build scripts.

The application source repository stays private. Only the contents of this
folder are published.

## Files

| File | Purpose |
|---|---|
| `index.html` | Legal landing page with links and publisher details |
| `privacy.html` | Published Privacy Policy |
| `eula.html` | Published End User License Agreement |
| `privacy.md` | Markdown source/mirror for records and Store submission text |
| `eula.md` | Markdown source/mirror for records and Store submission text |
| `styles.css` | Shared stylesheet; no external fonts, scripts, or resources |
| `.nojekyll` | Tells GitHub Pages to serve the static files as-is |
| `README.md` | This deployment guide |

The website uses no cookies, analytics, JavaScript, or third-party requests.

## Planned public URL

The recommended zero-cost setup is a separate public repository under the same
GitHub account:

- Repository: `https://github.com/gakrobert51-cloud/WinCleanAI-legal`
- Site: `https://gakrobert51-cloud.github.io/WinCleanAI-legal/`
- Privacy Policy: `https://gakrobert51-cloud.github.io/WinCleanAI-legal/privacy.html`
- EULA: `https://gakrobert51-cloud.github.io/WinCleanAI-legal/eula.html`

Internal links are relative, so the pages work under any repository name. If the
public repository or account name differs, only the absolute URLs entered in
Partner Center need to change.

## Publish (one time)

Use a directory **outside** the private application repository, so the public
repository has no Git history or source code from WinCleanAI:

```powershell
$destination = Join-Path $env:USERPROFILE 'src\WinCleanAI-legal'
New-Item -ItemType Directory -Path $destination -Force | Out-Null
Copy-Item -Path 'C:\App5\WinCleanAI\legal-site\*' -Destination $destination -Recurse -Force
Set-Location $destination
git init -b main
git add .
git commit -m "Publish WinCleanAI privacy policy and EULA"
gh repo create WinCleanAI-legal --public --source . --remote origin --push
```

Then enable GitHub Pages:

1. Open the public repository on GitHub.
2. **Settings → Pages**.
3. **Source:** *Deploy from a branch*.
4. **Branch:** `main`, **Folder:** `/ (root)`.
5. Save and wait for the deployment to finish.
6. Open the site and both documents in a private browser window. Confirm HTTP
   200, valid HTTPS, and that no login is required.

GitHub Pages issues a publicly trusted certificate automatically. No domain,
paid certificate, or additional hosting is required.

## Partner Center fields

Enter these absolute URLs after GitHub Pages is live:

| Field | URL |
|---|---|
| Privacy policy URL | `https://gakrobert51-cloud.github.io/WinCleanAI-legal/privacy.html` |
| EULA / license terms URL | `https://gakrobert51-cloud.github.io/WinCleanAI-legal/eula.html` |
| Support URL (optional) | `https://gakrobert51-cloud.github.io/WinCleanAI-legal/` |

If the repository name changes, replace `WinCleanAI-legal` in the URLs above.
The page bodies do not need to change.

## Updating the documents

1. Edit `privacy.md` or `eula.md` first and update the **Last updated** date.
2. Mirror the same changes in the corresponding HTML file.
3. Bump the effective date only when the legal terms change materially.
4. Copy the folder to the public repository, commit, and push.
5. Verify the live pages and, if the document structure changed, re-check the
   Partner Center submission.

## Privacy properties of this site

- No cookies, `localStorage`, or `sessionStorage`.
- No analytics, tracking pixels, or advertising.
- No JavaScript.
- No external fonts, CDNs, images, or stylesheets.
- Only the pages and `styles.css` are served.
