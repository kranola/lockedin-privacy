# Locked In — Privacy Policy

Public privacy policy for the **Locked In** iOS app, hosted with GitHub Pages.

**Live URL:** https://kranola.github.io/lockedin-privacy/

## Publishing steps

1. Create a **public** repo named `lockedin-privacy` under the `kranola` account.
   (Public matters — GitHub Pages on a private repo requires a paid plan.)

2. From this folder:

   ```bash
   git init
   git add index.html README.md
   git commit -m "Add Locked In privacy policy"
   git branch -M main
   git remote add origin https://github.com/kranola/lockedin-privacy.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Source = Deploy from a branch → `main` / `root` → Save.**

4. Wait ~1 minute, then open https://kranola.github.io/lockedin-privacy/ in a
   private browsing window to confirm it loads **without a login**.

## Where this URL must be set

- `LockedIn/PaywallView.swift` → `Self.privacyURL` (already updated)
- App Store Connect → App Information → Privacy Policy URL

Both must match, and the link must resolve before submitting for review.

## Keeping it accurate

The policy claims the app collects nothing and makes no network requests. That is
true as of v0.3 — there are no third-party SDKs, no Swift package dependencies, and
no `URLSession` usage anywhere in the codebase.

**If you ever add analytics, a crash reporter, or any networking, update this policy
before that build ships,** and update the App Privacy nutrition label in App Store
Connect to match.
