# supabase-keepalive

Private. A scheduled GitHub Action that sends one read-only request to each Supabase project every 3 days
so free-plan projects are not paused for inactivity.

Projects: sentinelos, northstar-site.

## Secrets (Settings, Secrets and variables, Actions, New repository secret)
Added by the owner only. Never put them in chat, code or issues.

| Name | Where to find it |
|---|---|
| SENTINELOS_URL | Supabase, sentinelos project, Project Settings, API, Project URL |
| SENTINELOS_ANON_KEY | same page, the public "anon" key |
| NORTHSTAR_URL | northstar-site project, same page |
| NORTHSTAR_ANON_KEY | northstar-site project, same page |

## Test
Actions tab, "Supabase keep-alive", Run workflow. A green check means both projects answered.
A red X means a project is down, paused, or a secret is missing; GitHub emails you.

## Notes
- GitHub turns off scheduled workflows after 60 days with no activity in the repo. Re-enable in the Actions tab if that happens.
- This is expected to keep projects awake but is not guaranteed; Supabase's pause rules can change.
