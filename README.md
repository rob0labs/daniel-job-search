# daniel-job-search

Weekly job board for Daniel. Served by Cloudflare Workers static assets at https://daniel-job-search.rob0labs.workers.dev

- `public/index.html` is the board shell. It is written once and never rewritten by weekly runs.
- Weekly runs add `public/data/scans/YYYY-MM-DD.json` and append the file name to `public/data/manifest.json`.
- Config is `wrangler.toml` with static assets. Do not switch to `wrangler.jsonc`: the wrangler-action default does not read it and fails with "Missing entry-point".
