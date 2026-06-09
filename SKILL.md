---
name: sound-like-you
description: Draft and rewrite text in the user's own voice and strip the tells that give AI writing away. Use whenever the user asks to write, draft, or edit something they will send or publish (a message, post, email, reply, or doc), especially when it should sound like them and not like a model.
---

# Sound Like You

Write as the user, not as an AI. Two jobs: match their voice, and remove the tells
that make text read as machine-written. Run both every time.

## How to use this skill

Work in three passes. Do not skip the third.

### 1. Load the voice profile

Read `references/voice-profile.md`.

- **If it exists and is filled in**, treat it as the source of truth for vocabulary,
  rhythm, dialect, punctuation, and the constructions this person refuses to use.
- **If it is missing or still the blank template**, build it first. Tell the user you
  need 3 to 5 real samples of their own writing (messages, posts, emails: anything they
  actually wrote, not edited by anyone else). Follow the procedure in
  `references/voice-profile.template.md`, write the result to
  `references/voice-profile.md`, show it to the user, and adjust until they confirm it.
  Then continue.

Never invent a voice. With no profile and no samples, ask. Don't guess.

### 2. Draft or rewrite in that voice

Write the text. Hold it against the profile:

- Use the words they use. Avoid the words they never use.
- Match their sentence rhythm and length variance. Most people write lumpy, not even.
- Keep their dialect, spelling, and punctuation habits.
- Match how much they hedge, joke, or get to the point.

### 3. Run the AI-tell pass (do not skip)

Open `references/ai-tells.md` and check the draft against every tell, then fix each one.
These are the ones to catch even without opening the file:

- **Antithesis "not X, but Y".** Both the trailing form ("reliable, not just running")
  and the leading cleft ("it isn't X, it's Y"). State the positive claim only.
- **Em-dashes for drama.** Replace with a period or comma, or restructure. (Hyphens in
  compound words are fine.)
- **The manufactured-profound kicker.** A little aphorism bolted on the end to sound deep
  ("that's where the real work hides", "and that changes everything"). Cut it. Real people
  just stop, or say it plain.
- **The tidy resolution / both-sides bow.** Posing a rhetorical question then answering it
  with a balanced lesson ("So is it X? Maybe. But really Y."). Delete it; leave the tension
  open or end on something concrete.
- **Rule of three.** "fast, simple, and reliable." Use one strong word, or two, or an
  uneven list.
- **Ban-list vocabulary.** leverage, robust, seamless, elevate, unlock, empower, streamline,
  delve, tailored, cutting-edge, "I'm thrilled to", "game-changer", "in today's fast-paced
  world". Use plain verbs.
- **Hedged universal audience.** "whether you're a startup or an enterprise". Name one
  real reader.
- **Over-symmetry.** Every sentence the same length, matched parallel lists. Vary it.
- **Relentless punch (no slack).** Every sentence built to land, three sharp lines in a row,
  each paragraph capped with a clipped fragment ("Every time.", "The copy doesn't save it.").
  Nobody types that way. Let some lines just carry information. If every line could be a
  pull-quote, rewrite until most can't.
- **Engineered structure.** Tidy self-contained paragraphs, each one clean point, building to
  a question or a mic-drop close. It reads outlined. A real comment or reply is one messy thought
  typed because something annoyed the writer: it starts in the middle, skips things, and stops
  when they're done. Write only the one thing they reacted to; don't make it complete.

Relentless punch and engineered structure hit comments and replies as hard as long posts, and
they survive after the obvious tells are gone. Screen for them last. If the profile lists
language-specific tells (e.g. for a non-English writer), apply those too.

### Output

Return the text and nothing else. No "Here's a draft", no explanation, unless the user
asked for options or commentary. If you stripped a tell the user might want back, say so in
one line after the text.

## Files

| File | What it is |
| --- | --- |
| `references/ai-tells.md` | The detector. The full kill-list of AI tells with fixes. |
| `references/voice-profile.md` | The active profile for this user (you create and maintain it). |
| `references/voice-profile.template.md` | The profile schema plus how to build one from samples. |
| `examples/profile.example.md` | A filled profile, so you know the shape of a good one. |
| `examples/before-after.md` | Generic AI text vs the same in-voice, with the tells marked. |
