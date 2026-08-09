# ASD-STE100 skill

This repository contains a skill that writes and rewrites technical prose in ASD-STE100 Simplified Technical English (STE), Issue 9.

The skill follows the Agent Skills format. The skill file is `skills/asd-ste100/SKILL.md`.

ASD-STE100 is a standard of the ASD (Aerospace, Security and Defence Industries Association of Europe). This skill is an implementation guide. It does not include the full STE dictionary.

## Install

```sh
gh skill install nithitsuki/asd-ste100-skill asd-ste100 --agent opencode --scope user
gh skill install nithitsuki/asd-ste100-skill asd-ste100 --agent pi --scope user
```

Use the same command for other agents that the GitHub CLI supports.

## Use

Ask the agent to write or rewrite technical text in STE. The agent applies the rules in `skills/asd-ste100/SKILL.md`.

## License

MIT. See [LICENSE](LICENSE).
