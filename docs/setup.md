# Setup

## 1. Connect Claude to Premiere Pro

This kit needs an MCP server that lets Claude control Premiere Pro. Several community servers exist; install one
following its own instructions, then check that Claude can read your open project (for example, ask Claude
"what sequences are in my Premiere project?").

## 2. Install the skill

**Claude Code:** copy the `skill/premiere-editor` folder to `~/.claude/skills/premiere-editor`.

**Claude app:** add the `skill/premiere-editor` folder as a skill in your settings.

## 3. Try it

Open a project in Premiere, then ask Claude something like:

- "Make a 15 second version of the 30 second spot. Keep the logo and the offer."
- "Here are the client notes for round 2: ... Work through them."
- "Review this sequence and mark anything that looks off."

Claude should duplicate the sequence first, leave markers for everything it touches, and leave the music alone.
