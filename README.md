# SciMigo Studio connector releases

This repository is reserved for **signed release assets** of the SciMigo Studio
connector. Its source, prompts and working files remain in the private connector
repository. The v0.4.0 stable release was withdrawn on 2026-10-27 after its archive
was found to include non-runtime test fixtures and reference solutions. Do not
use v0.4.0. Installs resumed on 2026-11-01 with v0.4.3 by owner decision `d-4b381ea565fd`
(the earlier pause was `d-f32082d0ccb8`). Read `LICENSE` before using any future connector release. The
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
- **v0.4.3: previous stable.** Source `thinkinginmath/scimigo-course-skills@38f6660`, signed by its
  `studio-connector-release` workflow (run 41324077186). Bundle SHA-256
  `6cb542e4b9a52ec1082affaf34da1d372e6769d2f3a8d38df2a5fb27fc759cd5`, 69 runtime files from the
  builder's explicit allow-list: no tests, fixtures or solutions. Adds the PowerPoint Studio starter
  and the `scimigo-presentation` skill.

- **v0.5.0: stable.** Owner approved publication and Mac activation on 2026-11-02,
  from source `thinkinginmath/scimigo-course-skills@6d5c6cc9e2ab13f8c3d27733a43d27c79f2f1ff0`
  (PR #35 remains unmerged), signed by workflow run 41328027490. Bundle SHA-256
  `4858417fb2e58821f965360e6de6ae801092972d413c485089d06e0bf35679b7`.
  Contains 72 explicitly allow-listed runtime files; no tests, fixtures, solutions
  or UI design documents. Defaults ordinary creation to the local Claude/Codex
  agent and skills, adds local visuals, and requires consent for hosted generation.
  The pinned key, license and existing signature/tamper checks are unchanged.
