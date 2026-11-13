## James Amalfitano

I build web apps in TypeScript and Postgres. Most of my repositories are
private; **[PukaGolf](https://github.com/JimmyA1400/pukagolf)** is the one I've
opened up to be read.

---

### [PukaGolf](https://github.com/JimmyA1400/pukagolf) · [live](https://pukagolf.vercel.app)

Live scoring for golf clubs and their leagues, in use by a club league.

**Next.js 16 (App Router) · React 19 · TypeScript · Tailwind 4 · Supabase (Postgres, row level security, realtime) · Vitest · Playwright**

- **The rules live in the database, not the app.** Row level security plus
  `security definer` functions that check the caller themselves, so a page
  hiding a button is a courtesy and never the lock.
- **Built for the conditions it runs in.** A score tapped in with no signal is
  queued, marked as held, and sent as one batch when the phone comes back —
  the far corner of a course usually has nothing. Score entry is one-handed,
  because the alternative is a number field in bright sun with a glove on.
- **Eleven game formats from one system.** A format is described by five facts
  and everything downstream reads those instead of branching on its name. Team
  size deliberately isn't one of them, which collapses nineteen named
  combinations into eleven specs and makes adding a twentieth a single new entry.
- **Tested.** 750 unit tests and 20 browser suites, including a parity test
  that scores the same field through both storage paths — the only thing
  stopping a scoring rule from being written into one adapter instead of the
  shared code.
