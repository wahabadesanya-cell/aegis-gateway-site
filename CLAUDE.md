# aegis-gateway-site — THIS IS THE LIVE SITE

**This repo serves https://gateway.adesanyaaiadvisory.com via GitHub Pages.**
A push to `main` here is a publish. Nothing else publishes this site.

| | |
|---|---|
| Serving | GitHub Pages, branch `main`, Enforce HTTPS on |
| Domain | `CNAME` = gateway.adesanyaaiadvisory.com; Namecheap `gateway` CNAME → wahabadesanya-cell.github.io |
| Source repo | `wahabadesanya-cell/aegis-guard-gateway` (engineering — **publishes nothing**) |

## The page has two names

`index.html` here is `aegis_guard_landing_page.html` in the engineering repo. Same page, two
filenames, two repos, and **nothing syncs them**. They were byte-identical on 27 Aug 2026 —
diff before editing either, and apply a change to both.

```bash
diff <(git -C ~/Claude/Projects/aegis-guard-gateway show origin/master:aegis_guard_landing_page.html) index.html
```

## Working rules

- **Make the change in the engineering repo first** (it is the source of truth and carries the
  tests), then apply it here and push. This repo holds only public files — never copy the
  engineering repo wholesale into it.
- **The waitlist form on `pricing.html` is patched to FormSubmit here**, not Netlify Forms.
  Overwriting it with the engineering repo's copy silently breaks the form.
- **Verify in a real browser after every push.** `curl` and WebFetch return stale cached copies
  on this host; a green fetch is not proof.
- **Netlify is dormant.** `aegis-guard-gateway.netlify.app`, the engineering repo's `deploy`
  branch, and its `netlify.toml` are all leftovers from before 26 Aug 2026 and serve nothing.
  Never push `deploy`; never enable Netlify credit auto-recharge.

## Why this file exists

On 27 Aug 2026 the landing page advertised "253 passing tests" while the suite stood at 904 — a
three-week-old figure that understated the product. The correction had been made, but in the
engineering repo, which reaches no visitor. Claims on this page are checked against the running
system, so when the engine or the suite changes, **the change is not finished until it is pushed
here.**
