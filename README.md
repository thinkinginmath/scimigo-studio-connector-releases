# SciMigo Studio connector releases

This repository is reserved for **signed release assets** of the SciMigo Studio
connector. Its source, prompts and working files remain in the private connector
repository. No connector archive is published here until the SciMigo use license
has been approved and included in that archive.

The distribution layout is:

- `releases/stable/manifest.json`: a signed pointer to the current version.
- `releases/vX.Y.Z/bundle.json`: the exact versioned archive named by the manifest.

The SciMigo app pins the Ed25519 public key and checks the manifest signature,
archive size, SHA-256 digest, plugin contract and installed files before enabling
the connector. The private signing key never belongs in this repository.
The public SPKI key is in `signing-key.spki.b64`; the private key is held as a
GitHub Actions secret in the private source repository.
