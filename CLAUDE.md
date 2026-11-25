# Rules for Claude in mbf-ops-backups

Private. Nightly backups of what people save in The Box (Mike Bass Ford's board hub), written by the scheduled task "The Box backup" (runbook 36 in mickeymann/mbf-ops). Holds customer and staff data: keep this repo private and never copy its files into mbf-ops.

- `box/box-backup-YYYY-MM-DD.json` – one verified copy per day, newest 30 kept. Shape: `{exportedAt, box_url, manifest: {collection: count}, docs: {collection: {doc_id: doc}}}`.
- Restore: `claude/thebox/backup/box_backup.py plan` in mbf-ops (runbook 36, "Restore").

Created Nov 25 2026 at Mickey's request, modeled on Edge Ledger's backups.

Only the nightly backup task (runbook 36) writes here, to `box/` on main. Do not edit or delete backup files by hand unless Mickey asks.
