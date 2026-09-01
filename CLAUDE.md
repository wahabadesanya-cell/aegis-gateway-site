# aegis-gateway-site — THIS IS THE LIVE SITE

**A push to `main` in this repo publishes https://gateway.adesanyaaiadvisory.com.
Nothing else publishes it.**

Before editing anything here, read the operating notes in the engineering repo
(`wahabadesanya-cell/aegis-guard-gateway`), which is the source of truth and
carries the tests. That repo publishes nothing; this one publishes everything.

Two rules that are cheap to state and expensive to rediscover:

1. **Never copy the engineering repo wholesale into this one.** This repo holds
   only the public site files. Pages here carry patches that a bulk copy
   destroys.
2. **`index.html` here is a renamed copy of a file in the engineering repo.**
   Nothing syncs them automatically. Diff before editing either, and apply the
   change to both.

Everything served from this repo is world-readable at the domain above — this
file included. Keep it that way on purpose: nothing internal, no credentials,
no notes you would not hand a visitor.
