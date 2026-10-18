# Legal Documents for ReadAloud: Text to Speech

This repository contains the official legal documents for the **ReadAloud: Text to Speech** mobile application.

- [Privacy Policy](privacy.html)
- [Terms of Service](terms.html)

---

## Live URLs

The documents are hosted on **Cloudflare Pages** and are referenced directly by the mobile application.

| Document             | Live URL                                          |
| :------------------- | :------------------------------------------------ |
| **Privacy Policy**   | `https://read-aloud-legal.pages.dev/privacy.html` |
| **Terms of Service** | `https://read-aloud-legal.pages.dev/terms.html`   |

> **Important for Developers:**  
> The URLs above are hardcoded in `SettingsModal.js` inside the main app repository.  
> If the project name or domain ever changes, update those constants accordingly.

---

## How to Update the Documents

Because the documents are hosted on Cloudflare Pages using **Direct Upload** (not Git integration), updating them requires a manual drag-and-drop step.

### Step-by-Step Workflow

1. **Edit the files locally**  
   Open `privacy.html` or `terms.html` in your code editor and make the necessary changes.

2. **Deploy the files to Cloudflare Pages**  
   Drag and drop the folder that contains the 2 HTML files to :
   https://dash.cloudflare.com/8ddc6c1bb11af205493610e837f71934/pages/view/read-aloud-legal/deployments/new

**Bump the version query string** (optional but recommended)  
 To ensure the mobile app's WebView does not serve a cached copy, append a version query parameter to the URLs in the app's `SettingsModal.js`:

```javascript
const PRIVACY_POLICY_URL =
  "https://read-aloud-legal.pages.dev/privacy.html?v=2";
const TERMS_OF_SERVICE_URL =
  "https://read-aloud-legal.pages.dev/terms.html?v=2";
```
