# SM-S948B S948BXXS4AZG5

Native Root My Galaxy payload for the European Galaxy S26 Ultra. It requires
an authorized Shizuku shell and refuses every non-exact device, fingerprint,
or kernel release.

## Exact identity

- Model: `SM-S948B` (`SM-S948B/DS` is reported as `SM-S948B` by Android)
- Device: `m3q`
- Fingerprint:
  `samsung/m3qxeea/m3q:16/BP4A.251205.006/S948BXXS4AZG5_OXM4AZG5:user/release-keys`
- Kernel:
  `6.12.30-android16-5-pd30ff70-abogkiS948BXXS4AZG5-4k`

## Validation

This native integration was validated once on that exact device. The tracefs
KASLR gate passed, the root daemon reported `uid=0`, and KernelSU 3.2.5 was
late-loaded successfully. SELinux returned to Enforcing after late-load.
The test staging files in `/data/local/tmp` were removed.

## Files

| File | Size | SHA-256 | Role |
| --- | ---: | --- | --- |
| `cve-2026-43499-app.so` | 235928 | `cfa90151022fba917f1b6bbd172110c74382812a40324452c35c60545034fd67` | native m3q AZG5 payload |
| `../../kernelsu/ksud-m3q-S948BXXS4AZG5-kdp` | 4894816 | `3ce5753203c93f4d733fbc10eebd7a69152189afb1d2a15bfd855bd6b5d4f622` | KernelSU 3.2.5 late-load binary |

## Provenance

The engine is vendored from `Anajrim01/s26u-m3q-temp-root` commit `ad7e4fe`
under Apache-2.0; see `vendor/s26u-m3q-temp-root/README.md`. The integration
uses Root My Galaxy's bundled helper and standard success markers, so the
manifest needs no custom helper, staging path, environment map, or separate
user-facing profile.
