# DesignSetGo community apps

A public list of WordPress apps people have built and deployed with [DesignSetGo Apps](https://designsetgo.dev). Apps listed here show up at https://designsetgo.dev/examples/ within ~one site rebuild after the PR merges.

## What this repo is

A directory of JSON files. One JSON file per listed app. Each JSON file describes a real, deployed app — what it does, where the source lives, where it's running. The website pulls this list at build time.

## What it isn't

- Not a package manager. We don't host code; the JSON points at your own GitHub repo.
- Not a marketplace. Free listings; no payment surface.
- Not a review system. We accept anything that meets the schema, is hosted on a real WP site, and isn't off-topic / abusive / malicious.

## Submit your app

Submit by opening a pull request that adds one file: `apps/<slug>.json`. See [`schema/app.schema.json`](schema/app.schema.json) for the format. Steps:

1. Fork this repo.
2. Add `apps/<your-slug>.json` matching the schema.
3. Open a PR. CI validates the schema, checks slug uniqueness, soft-checks that your `repo` / `screenshot` / `live_url` return 200, and flags any profanity for human review.
4. A maintainer reviews; merge is the activation event.

### Slug rules

- Lowercase letters, digits, hyphens only.
- Globally unique within `apps/` AND globally unique against official slugs at https://designsetgo.dev/examples/ (validated at website build time, not in this repo).
- The slug becomes your URL: `https://designsetgo.dev/examples/<slug>`. Pick something durable.

### Anchor

<a name="submit"></a>

You arrived here from the catalog. Read above and click the **green "Fork"** button to start your PR.

## Listing maintenance

If your app moves repos, changes name, or goes offline, open a PR editing or deleting your `apps/<slug>.json`.

## What "community" means

Listed apps live in their authors' own GitHub orgs. The repo URL in the JSON is the source of truth; this repo is just an index.
