# Claude Skills

Personal Claude Code skill library.

## Structure

```
skills/
  skill-name/
    SKILL.md        # Main skill file (loaded by Claude Code)
    supporting.*    # Additional files if needed
```

## Skills

| Skill | Description |
|-------|-------------|
| [prd-writer](skills/prd-writer/SKILL.md) | PRD(기획서) 작성 워크플로우 가이드 |
| [strategy-writer](skills/strategy-writer/SKILL.md) | B2B SaaS GTM·시장 진입·사업 확장 전략 문서 작성 가이드 |

## Usage

Skills are loaded from `~/.claude/skills/`. To use these skills locally:

```bash
# Symlink or copy skills to your Claude skills directory
ln -s ~/claude-skills/skills ~/.claude/skills
```

Or copy individual skills:
```bash
cp -r ~/claude-skills/skills/prd-writer ~/.claude/skills/
```
