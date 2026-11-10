# Project notes for Claude

## Writing: always run the text-cleaning skill

Run the `clean-user-facing-text` skill (in `.claude/skills/`) on any reader-facing prose you write or edit in this repo: page copy, bios, project descriptions, and similar.

- Before finishing, run the Unicode pass on every file you changed:
  `python3 .claude/skills/clean-user-facing-text/scripts/inspect_text.py --stylometry FILE`
  `python3 .claude/skills/clean-user-facing-text/scripts/clean_text.py FILE -o FILE --stats --no-normalize-spaces`
- Change prose only. Leave HTML tags, attributes, URLs, and file names as they are.
- Keep every fact the same. Don't invent details.

The skill comes from github.com/guillaumemeyer/watermarks-remover (MIT, commit 5a62be6).
