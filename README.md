# Root My Galaxy payload mirror

This repository is the payload source used by the Root My Galaxy build for
the device selector. The application pins every download to a verified
commit on the **main** branch before fetching the manifest or an artifact.

## Contents

- **support/targets-v3.json** — the selector manifest;
- **artifacts/** — native payloads;
- **kernelsu/** — matching KernelSU loaders.

## SM-S948B / m3q AZG5

The **m3q-S948BXXS4AZG5** entry is enabled only for the exact SM-S948B EU AZG5
fingerprint and Android 16 kernel release. It requires an authorized Shizuku
shell. Its native payload and KernelSU loader were hardware-validated on that
exact device; the old oracle experiment is intentionally not part of this
repository.

Do not add a target by model name alone: every new profile must pin its kernel
release and, where applicable, its Android build fingerprint.
