# Before / after

The same idea, written by a generic AI and then in Sam's voice (see
`profile.example.md`), with the tells called out. Use this to calibrate.

## The prompt

> Write a short post about adding a caching layer to a side project.

## Before: generic AI

> I'm thrilled to share a recent improvement to my side project! 🚀
>
> I added a caching layer, and the results have been nothing short of transformative.
> It's not just about speed — it's about delivering a seamless, robust experience for
> users. By leveraging a tailored caching strategy, I was able to make the app faster,
> cleaner, and more reliable.
>
> So was it worth the effort? Absolutely. Because at the end of the day, the real work
> isn't in writing the code. It's in making it feel effortless.

What's wrong with it:

- "I'm thrilled to share" + 🚀: announcement boilerplate.
- "nothing short of transformative": empty intensifier.
- "It's not just about speed — it's about…": antithesis **and** an em-dash.
- "leveraging", "seamless", "robust", "tailored": ban-list words.
- "faster, cleaner, and more reliable": rule of three.
- "So was it worth the effort? Absolutely. Because…": tidy both-sides bow.
- "the real work isn't in writing the code. It's in…": antithesis plus a
  manufactured-profound kicker to close.

## After: in Sam's voice

> Added caching to the side project this weekend.
>
> The annoying part wasn't the cache itself, it was figuring out when to throw it away.
> Got it wrong twice and served stale data to myself for an hour before I noticed.
>
> Anyway, pages that took 800ms are under 50 now. Good enough.

Why it lands:

- Opens cold with what happened.
- Real number (800ms to 50). No intensifiers.
- The mistake is the story, told dry, no setup.
- Just stops. No kicker, no bow, no triple.
- "the annoying part wasn't the cache, it was…" reads as natural speech because it names
  a real, specific thing. It's how Sam actually talks. When in doubt, cut even this.

## A second prompt: a comment

> Reply to a post claiming "AI will replace junior developers this year."

This pair shows the two tells that survive after the obvious ones are gone: **relentless
punch** (every line built to land) and **engineered structure** (reads outlined, not typed).

### Before: technically clean, obviously AI

> This take misses what juniors actually do.
>
> Juniors aren't there to write code. They're there to learn judgment. And judgment is the
> one thing a model can't hand you.
>
> Replace the typing, sure. But the typing was never the job. The job was learning what to
> build and why. That doesn't go away. It gets more valuable.

Why it reads as AI, even with no em-dash or ban-list word:

- Every sentence lands a hit. There's no slack, no throwaway line, nothing just carrying
  information. Three paragraphs, each a clean point, building to a mic-drop ("It gets more
  valuable").
- "Replace the typing, sure. But the typing was never the job." is the antithesis tell again,
  dressed up.
- It reads like it came from an outline, not like someone typed it because a post annoyed them.

### After: one messy thought, typed

> eh, juniors don't really get hired to type though. half the value is they ask the dumb
> questions that make you realize the spec is wrong. a model won't push back on you like that,
> it just does what you said. anyway we still hire them so

Why it lands:

- Starts in the middle, lowercase, a real "eh".
- One point (juniors push back), not a complete argument. Doesn't cover every base.
- Has slack: "anyway we still hire them so" just trails off. Not quotable, and that's the point.
