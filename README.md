# SciMigo Studio connector releases

This repository is reserved for **signed release assets** of the SciMigo Studio
connector. Its source, prompts and working files remain in the private connector
repository. Release v0.4.0 is published here under the approved SciMigo Studio Connector
Use License. Read `LICENSE` before downloading or using the connector. The
source remains in the private connector repository.

The distribution layout is:

- `releases/stable/manifest.json`: a signed pointer to the current version.
- `releases/vX.Y.Z/bundle.json`: the exact versioned archive named by the manifest.

The SciMigo app pins the Ed25519 public key and checks the manifest signature,
archive size, SHA-256 digest, plugin contract and installed files before enabling
the connector. The private signing key never belongs in this repository.
The public SPKI key is in `signing-key.spki.b64`; the private key is held as a
GitHub Actions secret in the private source repository.

## Current release

- Version: `0.4.0`
- Source commit: `thinkinginmath/scimigo-course-skills@6c30459`
- Bundle SHA-256: `c0c1e72e241743c5a596db59415473ac49c2ab855d7cccd9f4ca822f70758e5c`
- The signed stable manifest points to the exact versioned bundle.
