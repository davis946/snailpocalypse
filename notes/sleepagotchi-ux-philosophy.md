# Design note: the sleepagotchi post, and hiding the complexity

*August 28, 2026. Game-design brainstorming, parked in the site repo for lack
of a better shared home. Nothing in this note changes the site, and nothing in
it is committed work — it's a note.*

A post about @sleepagotchi worth keeping. The short version:

> Health technology compounds — sleep stages, recovery, heart rate, routines,
> mood, AI recommendations — until improving your health starts feeling like
> homework. Sleepagotchi's answer is to keep the complicated intelligence
> underneath (an AI Sleep Coach owns the deep sleep context) and put a world on
> top: Dino progresses, new areas unlock, and this week the Darklings take over
> Robbery Road, travellers lose supplies, and Dino gets another mission. The
> game turns participation into progression and gives you a reason to care
> without requiring you to become obsessed with health statistics. "Sometimes
> making health technology better isn't about showing users more — it's about
> hiding the complexity without hiding the value."

Advanced technology underneath, simple experience on top. Two products, same
religion. Worth writing down what transfers to Snailpocalypse and what doesn't.

## What we already believe

- **The interface is one image.** A snail, a road, your lead. The gap between
  you and Toby *is* the dashboard — you glance at it and feel it, you don't
  read it. Sleepagotchi had to build a world to stand in front of its charts;
  we never had charts.
- **One number in the whole game.** Daily steps, and even that number matters
  mostly as distance Toby has to cover. Nothing else is measured.
- **Our "intelligence underneath" isn't data science — it's psychology
  compressed into fiction.** No servers, no analytics, no model. Loss aversion
  isn't a streak widget; it's Toby, closer than yesterday. The snail is the
  recommendation engine: his position says "walk" better than any coaching
  notification could.
- **Participation is already progression.** Guilds and raids are collective
  fiction over summed steps. Yards and gifts are expression with zero
  mechanical weight — and the site promises cosmetics never affect the race,
  so that stays true.

## Where the premise differs

Sleep data is illegible without interpretation — nobody can act on a raw
hypnogram, so sleepagotchi *must* translate complexity and needs a Sleep Coach
underneath. Steps are already legible; a seven-year-old understands 8,000
steps. So our risk runs the other way: **we don't have complexity to hide, we
have simplicity to protect.** For them the sin is showing the machinery. For
us the sin is building machinery. The test for any proposed feature: does this
add a second number that competes with the road?

## What their playbook still teaches us

1. **Change the world, not the scoreboard.** Robbery Road is a content update
   delivered as fiction: same inputs, new reason to show up. Our freshness
   should be roads, weather, seasons, landmarks, a rival — never new metrics,
   multipliers, or a second currency of effort. A mission should always
   resolve to the same verb: walk.
2. **Milestone geography.** "New areas unlock" maps cleanly onto lifetime
   distance: places the road has passed, rather than a lifetime-steps counter.
   The road remembers so the number doesn't have to appear.
3. **Translate signals, never display them.** If the game ever reads more than
   steps from HealthKit (distance, flights climbed, workouts), it should
   become terrain — a hilly day becomes hills — not a stat panel. And any new
   signal is a privacy-policy event: the site's claims are reporting, not
   copy, so design and policy move together or not at all.
4. **Their coach is a feature; ours is a character.** If we ever want adaptive
   behavior — Toby pacing himself to the shape of someone's actual life — it
   stays on-device and invisible, felt as fairness rather than shown as a
   model. Toby already delivers the entire coaching message in five words:
   "I don't rush. I arrive."
5. **Audit every raw number.** Each place a literal step count appears in the
   app should justify itself; most could be a picture of a snail instead.
   Notifications especially: fiction ("I passed the bakery."), never
   arithmetic ("You're 2,300 steps behind!").

## Guardrails, unchanged by any of this

- One number. Nothing competes with steps.
- Cosmetics never affect the race. If terrain ever gets mechanics (salt flats
  are *right there*), it applies to everyone identically or it's scenery.
- No servers, no ads, no analytics, no accounts. A design that needs a
  dashboard's worth of collection is a different game — and it would break
  promises the site makes in writing.

Their maxim localizes cleanly: hide the complexity without hiding the value.
Ours is shorter — never build the complexity, and the value walks toward you
on its own.
