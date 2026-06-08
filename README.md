# Sound Like You

A skill that makes your AI sound like you, not like an AI.

It does two things every time it writes or edits something. It matches your voice from a
profile built out of your own writing, and it strips the constructions that make text read
as machine-written: the "X, not Y" antithesis, the em-dash drama, the little profound line
bolted onto the end, the rule of three, the GPT-ese vocabulary.

It's an [Agent Skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills). Drop
it in and Claude picks it up whenever you ask it to draft or rewrite something you'll send.

## Why

AI writing has a sound. Once you notice the tells you can't unsee them, and they quietly
cost you credibility: a post that reads as generated, a DM that sounds like a template.
This skill is the system I run on my own writing, packaged so anyone can use it. The tell
list is general. The voice profile is yours.

## Install

Copy the folder into your skills directory:

```bash
# For one project
cp -r sound-like-you /path/to/your/project/.claude/skills/

# Or for everything, user-wide
cp -r sound-like-you ~/.claude/skills/
```

Then just ask, in plain language:

> Write a reply to this email so it sounds like me.

The first time, it has no profile, so it asks for a few samples of your own writing and
builds one. After that it uses the profile every time.

## How it works

Three passes, run in order (see `SKILL.md`):

1. **Load your voice profile** (`references/voice-profile.md`). If it's empty, build it
   from a few real samples first.
2. **Write in that voice**: your vocabulary, your rhythm, your dialect.
3. **Strip the AI tells**: check the draft against `references/ai-tells.md` and remove
   every one.

## Build your profile

Give the skill a handful of things you actually wrote: a message, a post, an email. It
reads them for patterns, not topics, fills in the profile, and shows it to you to correct.
The schema and procedure are in `references/voice-profile.template.md`, and there's a filled
example in `examples/profile.example.md`.

## What's in here

| Path | What it is |
| --- | --- |
| `SKILL.md` | The skill. The three-pass instructions Claude follows. |
| `references/ai-tells.md` | The detector. The full list of tells with fixes, useful on its own. |
| `references/voice-profile.md` | Your profile. Starts blank; the skill fills it. |
| `references/voice-profile.template.md` | The profile schema and how to build one. |
| `examples/` | A filled profile and a before/after, so you can see the shape. |

## License

MIT. Built by [Henning Sandtorv](https://henningsandtorv.dev).
