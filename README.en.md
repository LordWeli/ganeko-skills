# ganeko-skills

[Português](README.md)

Claude Code skills I actually use. Atomic: each one does one thing, so you can slot it into your own workflow and adapt it. Open and free.

> **Everything here is beta.** I use it and it works for me, but it still changes every week. It may break or be renamed. Use it, complain, open issues.

## Skills

| Skill | What it does |
|---|---|
| [`lesson`](skills/beta/lesson) | `/lesson <concept>` → one HTML lesson: a map up top, from the real problem to the technical name, terms, questions and primary sources. |
| [`video-lesson`](skills/beta/video-lesson) | `/video-lesson <slug>` → turns the lesson into a ~4 min narrated, animated video with a player page. Local voice (Kokoro) by default. |

Each skill ships a `STYLE.md` with my style as the default. Edit it to make it yours.

## Install

```bash
git clone https://github.com/YudiG12/ganeko-skills
cp -R ganeko-skills/skills/beta/lesson ~/.claude/skills/
cp -R ganeko-skills/skills/beta/video-lesson ~/.claude/skills/
~/.claude/skills/video-lesson/scripts/setup.sh   # once: Python (Kokoro, faster-whisper) and Node (Remotion)
```

Needs `python3`, `node` 18+ and `ffmpeg`.

## Licenses

- Code: MIT.
- `video-lesson` renders with [Remotion](https://www.remotion.dev/license), which is **not open source**: free for individuals and companies up to 3 people; larger companies need their license.
- M PLUS fonts: SIL Open Font License 1.1 (`skills/beta/video-lesson/engine/public/OFL.txt`).
- Default narrator: [Kokoro-82M](https://huggingface.co/hexgrad/Kokoro-82M) (Apache 2.0).
