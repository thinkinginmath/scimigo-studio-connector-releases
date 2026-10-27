# SciMigo Studio connector releases

This repository is reserved for **signed release assets** of the SciMigo Studio
connector. Its source, prompts and working files remain in the private connector
repository. The v0.4.0 stable release was withdrawn on 2026-10-27 after its archive
was found to include non-runtime test fixtures and reference solutions. Do not
use v0.4.0. Fresh Studio connector installs are paused by owner decision
`d-f32082d0ccb8`. The stable manifest and bundle are absent from the current
branch. Existing locally verified cached connectors may still work through the
app's fallback. Read `LICENSE` before using any future connector release. The
source remains in the private connector repository.

The distribution layout is:

- `releases/stable/manifest.json`: a signed pointer to the current version.
- `releases/vX.Y.Z/bundle.json`: the exact versioned archive named by the manifest.

The SciMigo app pins the Ed25519 public key and checks the manifest signature,
archive size, SHA-256 digest, plugin contract and installed files before enabling
the connector. The private signing key never belongs in this repository.
The public SPKI key is in `signing-key.spki.b64`; the private key is held as a
GitHub Actions secret in the private source repository.

## Release status

- v0.4.0: withdrawn; source commit `thinkinginmath/scimigo-course-skills@6c30459`.
- Withdrawn bundle SHA-256: `c0c1e72e241743c5a596db59415473ac49c2ab855d7cccd9f4ca822f70758e5c`.
- No corrected release or stable manifest will be published until the owner makes
  a new decision to resume installs.
