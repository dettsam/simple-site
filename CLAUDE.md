# simple-site

A practice website for learning the GitHub → Cloudflare workflow.

## How this site works

- The website files live in `public/`. Only edit files there unless asked otherwise.
- `wrangler.jsonc` tells Cloudflare how to deploy. Don't change it unless asked.
- Cloudflare (Workers Builds) deploys automatically:
  - Every pushed branch gets a preview build, reported as a check on the PR.
  - Every merge into `main` updates the live site.

## How to make changes

- Never push directly to `main`. Always:
  1. Start a new branch from the latest `main`
  2. Make the change and commit with a clear message
  3. Push the branch and open a pull request
- Keep each PR to one change. Don't fix or tidy unrelated things along the way.
- After pushing, tell Ted the PR link and what changed, in plain language.

## When to merge on your own

**Small text fixes**: typos, a date, a phone number, a broken link.
Open the PR, wait for the Cloudflare check to pass, then merge it, delete the
branch, and tell Ted it's live.

**Everything else**: layout, colors, fonts, new pages, rates, or legal and
compliance wording. Open the PR and wait for Ted to review and merge.

**If the Cloudflare check fails**: never merge. Read the build log, fix it on
the same branch, and push again. If you can't fix it, tell Ted what the error says.

If you're unsure which category a change falls into, treat it as "everything else."
