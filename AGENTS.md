<!-- BEGIN nicegram-dataroom-protocol v1 -->
## Nicegram dataroom: before and after every task

This repository is part of the Nicegram system. Its map, the feature knowledge base, the OKR and the work log live
in the private repository `nicegram/dataroom` (https://github.com/nicegram/dataroom). Every agent (Claude Code,
Codex, Cursor or any other) follows these steps for every task that changes this repository. The full rule is
`docs/operations/agent-work-protocol.md` in the dataroom.

Before the task:
1. Update your checkout of the dataroom and read its `README.md`, this repository's profile under
   `docs/repositories/` and, for a feature, `docs/kb/README.md`. Keep the dataroom commit you read.
2. Find the task's OKR id in `docs/okr/governance.json` and its Jira key (`NCG-<number>`), when it has them. Never
   invent either.
3. No access to the dataroom: say so in your first reply, do the task, and record the gap in the work log entry.

After the task:
4. A user-visible feature appeared, changed or was removed: update its record under `docs/kb/` in the dataroom.
5. Add one work log entry to the dataroom: a new file `docs/work-log/<yyyy>/<mm>/<id>.json` naming this repository,
   the commit or pull request, the dataroom commit you read, the OKR ids, the Jira keys and the features changed.
   An entry is never edited or deleted; a correction is a new entry.
6. Run `python3 scripts/agentops/worklog.py --check` in the dataroom, then merge the entry.

Every night the dataroom lists the commits on this repository's default branch that no work log entry names.
<!-- END nicegram-dataroom-protocol v1 -->
