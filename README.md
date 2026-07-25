# Snailpocalypse website

The public website for **Snailpocalypse**, the iPhone game where an immortal
snail (Toby) chases your real daily steps. This repo holds only the website —
the game itself lives in a separate private repo.

Live at: https://davis946.github.io/snailpocalypse/

| Page | Purpose |
| --- | --- |
| `index.html` | Landing page |
| `privacy/` | Privacy policy (required by App Store Connect; the app uses HealthKit) |
| `support/` | Support page (required by App Store Connect) |
| `terms/` | Terms of Use (required for the Shell Club subscription) |

Plain static HTML + one stylesheet. No build step, no dependencies. Pushing to
`main` republishes the site via GitHub Pages within a minute or two.
