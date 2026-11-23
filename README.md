# ganeko-skills

[English](README.en.md)

Skills do Claude Code que eu uso de verdade. Atômicas: cada uma faz uma coisa, pra você encaixar e adaptar no seu fluxo. Tudo aberto e grátis.

> **Tudo aqui está em beta.** Eu uso, funciona pra mim, mas ainda muda toda semana. Pode quebrar, pode mudar de nome. Use, reclame e abra issue.

## Skills

| Skill | O que faz |
|---|---|
| [`lesson`](skills/beta/lesson) | `/lesson <conceito>` → uma aula em HTML: mapa no topo, do problema real até o nome técnico, termos, perguntas e fontes primárias. |
| [`video-lesson`](skills/beta/video-lesson) | `/video-lesson <slug>` → transforma a aula num vídeo narrado e animado de ~4 min, com página de player. Voz local (Kokoro) por padrão. |

Cada skill traz um `STYLE.md` com o meu estilo como padrão. Edite pra ficar com a sua cara.

## Instalar

```bash
git clone https://github.com/YudiG12/ganeko-skills
cp -R ganeko-skills/skills/beta/lesson ~/.claude/skills/
cp -R ganeko-skills/skills/beta/video-lesson ~/.claude/skills/
~/.claude/skills/video-lesson/scripts/setup.sh   # uma vez: Python (Kokoro, faster-whisper) e Node (Remotion)
```

Precisa de `python3`, `node` 18+ e `ffmpeg`.

## Estrutura

```
skills/
  beta/     # uso, funciona pra mim, ainda mexendo
```

Uma skill sai do beta quando roda em 3+ projetos diferentes e passa 2 semanas sem mudança grande.

## Licenças

- Código: MIT.
- `video-lesson` renderiza com [Remotion](https://www.remotion.dev/license), que **não é open source**: grátis pra pessoa física e empresas de até 3 pessoas; empresas maiores precisam de licença deles.
- Fontes M PLUS: SIL Open Font License 1.1 (`skills/beta/video-lesson/engine/public/OFL.txt`).
- Narração padrão: [Kokoro-82M](https://huggingface.co/hexgrad/Kokoro-82M) (Apache 2.0).
