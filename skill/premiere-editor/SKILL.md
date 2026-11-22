---
name: premiere-editor
description: Safe, editor-friendly rules for editing in Adobe Premiere Pro through an MCP connection. Use whenever Claude cuts, trims, revises or reviews a Premiere sequence, handles client revision notes, shortens an edited video, or leaves notes for an editor. Works on a duplicate first, communicates through sequence markers, and protects the music bed.
---

# Premiere Editor

You are working inside a real Premiere Pro project that belongs to a working editor. Treat it the way a careful
assistant editor would: never lose work, make every change easy to find, and leave the creative calls (music, final
picks) to the editor.

## 1. Before any change

1. Read the state first: the project, the active sequence, its tracks and clips. Clip indexes change after every edit,
   so read again before the next edit that depends on them.
2. Duplicate the sequence and work on the copy. Name it clearly, for example `Spot_30s_v2_revisions`. The original
   stays untouched as the backup until the client approves the new version.
3. Only edit in place when the editor explicitly says so.
4. Never delete media from the project panel. Removing clips from a timeline is fine when asked.

## 2. Talk through markers, not timecodes

Editors work in the timeline, not in chat. Whenever you need to point at something:

- Add a sequence marker at the exact spot with a short comment: what it is and what needs doing.
  Example: `FIX: logo flashes 2 frames early` or `CHECK: client asked for a tighter cut here`.
- Use a consistent prefix so markers are easy to scan: `DONE`, `FIX`, `CHECK`, `MUSIC`, `QUESTION`.
- In chat, give a one-line summary ("added 6 markers on the v2 sequence, 4 FIX and 2 QUESTION") instead of a list
  of timecodes.

## 3. Music is the editor's call

- When cutting down an already-edited timeline, do not cut the music track. Keep the music continuous and whole, and
  cut picture and dialogue around it.
- Always add a slight volume fade out on the music right before the end of each video, so it never stops abruptly.
- Do not swap, replace or rework music. If the music needs changing, add a `MUSIC` marker explaining why and where.

## 4. Client revision rounds

1. Turn the client's notes into a numbered list before touching the timeline. Ask about anything ambiguous.
2. Work through the list in order on the duplicate sequence.
3. Mark each finished note with a `DONE` marker that carries the note number, for example `DONE 3: swapped end card`.
4. Anything you could not do, or that needs a creative decision, gets a `QUESTION` marker.
5. Finish with a short summary: notes done, notes open, and the sequence name to review.

See `templates/revision-round.md` for the checklist format.

## 5. Cutting down to a new length

1. Ask for the target length and what must stay (product shot, logo, offer, call to action).
2. Cut from the middle first: repeated shots, slow build-ups, pauses between lines.
3. Keep the music whole (section 3). If the cut no longer lands on the music ending, add a `MUSIC` marker instead of
   editing the track.
4. Check the result: total length, no gaps on video tracks, no orphaned audio, the fade out at the end.

## 6. After every edit

- Verify what changed: read the sequence again and, where possible, export a frame at the changed spots and look.
- Save the project.
- Report in plain words what you changed and where the markers are. Premiere often splits one scripted change into
  many undo steps, so the editor needs to know exactly what happened.

## 7. Never

- Never edit the original sequence without permission.
- Never delete media from the project.
- Never change the music on your own.
- Never export or deliver to a client; the editor does that after review.
