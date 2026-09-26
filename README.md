# unraid-templates

Unraid Community Applications template repository for [@FugginOld](https://github.com/FugginOld).

## Layout

| Path | Purpose |
| --- | --- |
| `ca_profile.xml` | Repo metadata shown in CA. Must stay in the root. |
| `templates/` | One XML file per Docker app. |
| `plugins/` | One XML wrapper per plugin. |

## Contents

- `templates/topographer.xml` — [topographer](https://github.com/FugginOld/topographer)
- `plugins/hbaviewer.xml` — [Unraid-HBAviewer](https://github.com/FugginOld/Unraid-HBAviewer)
- `plugins/unraid-balance.xml` — [Unraid-Rebalance](https://github.com/FugginOld/Unraid-Rebalance)

## Adding an app

1. Add `templates/<app-name>.xml` as a v2 `<Container>`.
2. Set `<Repository>` to the Docker image and point `<TemplateURL>` at the raw
   GitHub URL of that exact file *in this repo*.
3. Fill in `<Overview>`, `<Category>`, `<Support>` or `<Project>`, and the
   `<Config>` entries for ports/paths/variables.

Plugins are the same, but need `<PluginURL>` matching the `.plg` file exactly.

## Submitting

Run Validate, then Scan, in the Community Apps submit flow (Apps → `/submit`).

Licensed MIT (OSI-approved, required for submission).
