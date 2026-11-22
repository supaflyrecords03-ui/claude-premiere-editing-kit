# Claude Premiere Editing Kit

A Claude skill that makes AI editing in Adobe Premiere Pro safe for working editors and agencies.

Claude can already cut, trim and rearrange a Premiere timeline through MCP. What it lacks out of the box are the habits
a professional editor relies on: never losing the original, pointing at problems where the editor actually looks,
and not touching creative decisions like music. This kit adds those habits.

## What it does

- **Works on a copy.** Duplicates the sequence before any change; the original stays as the backup until the client approves.
- **Talks through markers.** Leaves sequence markers with short comments (`DONE`, `FIX`, `CHECK`, `MUSIC`, `QUESTION`) instead of listing timecodes in chat.
- **Protects the music.** Keeps the music track whole when cutting down, adds a fade out before the end, and flags music changes instead of making them.
- **Runs revision rounds.** Turns client notes into a numbered checklist, works through it, and marks each note as done or open.
- **Checks its work.** Re-reads the timeline, checks length, gaps and orphaned audio, and reports what changed.

## Who it's for

Video editors, content teams and agencies who edit with Claude and Premiere Pro and want AI help without risking
client work.

## Install

See [docs/setup.md](docs/setup.md). In short: connect Claude to Premiere Pro with an MCP server, then add the
`skill/premiere-editor` folder as a skill.

## Contents

```
skill/premiere-editor/SKILL.md   the rules Claude follows
templates/revision-round.md      checklist for each round of client notes
templates/marker-legend.md       marker prefixes and examples
docs/setup.md                    installation
docs/examples.md                 example prompts
```

## Contributing

Ideas, issues and pull requests are welcome, especially support for DaVinci Resolve and Final Cut Pro, and new
workflows (captions, social cut-downs, versioning).

## License

MIT, see [LICENSE](LICENSE).
