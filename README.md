# claude-status-bar

My Claude Code status line. Shows: `user@cwd` · `model/effort` · `git-branch` · `tokens (compact %)` · `Usage: 5h%/week%`.

## Install (point Claude Code here and say "set this up")

```bash
cp statusline-command.sh ~/.claude/statusline-command.sh
```

Then add to `~/.claude/settings.json`:

```json
"statusLine": {
  "type": "command",
  "command": "bash /home/gara/.claude/statusline-command.sh"
}
```

Requires `jq`, `awk`, `git`. Adjust `compact_threshold` (default 140000) in the script if your context window differs.

## Update

Edit `statusline-command.sh` here, commit, then re-run the install copy. This repo is the source of truth.
