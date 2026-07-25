# Snailpocalypse website

The public site for Snailpocalypse, an iPhone game where an immortal snail (Toby)
chases your real daily step count. The game itself lives in a separate private
repo — nothing here talks to it, and no code is shared.

Four pages of hand-written static HTML over one stylesheet. No build step, no
dependencies, no framework, no JS. Open `index.html` in a browser to see changes.
Pushing to `main` republishes via GitHub Pages in a minute or two, so `main` is
production.

```
index.html      landing page
privacy/        privacy policy
support/        support page
terms/          terms of use
styles.css      every page's styles
toby.svg        the snail; also the favicon
```

## Things that aren't obvious from the files

**The three legal pages exist because App Store Connect requires them**, and
their URLs are filed in the app's listing — the paths are load-bearing, and a
broken one can hold up review. They also make specific factual claims: no
servers, no ads, no analytics, no accounts, cosmetics never affect the race,
and step data stays on the device unless the player switches on one of the
sharing features (friends, leaderboard, guilds, raids, yards), which publish a
step total to other players through a shared CloudKit database. Those claims
describe how the app actually works, so treat them as reporting rather than
copy. If a change would make one of them untrue, that's a question for the
user, not an edit.

The health claim used to read "HealthKit data never leaves the device," which
was wrong — the app published a step total whether or not the player had asked.
Don't restore that wording; the qualified version above is the accurate one.

**The header nav is duplicated in all four pages** and paths differ by depth
(`toby.svg` and `privacy/` at the root, `../toby.svg` and `../privacy/` inside a
subdirectory), with the current page linking to `./`. Adding a page means
touching the nav and footer everywhere.

**Colors and shadows come from the `:root` custom properties in `styles.css`**,
and they're deliberately matched to the in-app design language — the rounded
system font stack, the warm pastel palette. Pages are built from what the
stylesheet already covers rather than per-page CSS — the bare `article` and
`details` elements are styled directly, alongside the `.card` and `.tldr`
classes.

**Toby's voice is patient and faintly ominous** ("I don't rush. I arrive."). The
copy is written, not generated — match the register of what's around it.

**The legal pages carry effective dates.** Substantive changes to those pages
mean the date changes too; typo fixes don't.
