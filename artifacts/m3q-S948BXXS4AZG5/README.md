# Galaxy S26 Ultra SM-S948B / S948BXXS4AZG5

Experimental payload profile for the `m3q` device family.

- Model: `SM-S948B`
- Device: `m3q`
- Product: `m3qxeea`
- Build fingerprint: `samsung/m3qxeea/m3q:16/BP4A.251205.006/S948BXXS4AZG5_OXM4AZG5:user/release-keys`
- Kernel: `6.12.30-android16-5-pd30ff70-abogkiS948BXXS4AZG5-4k`

The binaries in this profile were extracted byte-for-byte from the supplied
`M3QRoot-EU.apk` and are published with their SHA-256 values in
`support/targets-v3.json`. They are not source-built here and have not been
hardware-validated by this repository. Treat this profile as experimental and
keep a recovery path available when testing.

## M3Q adapter contract

The Root My Galaxy M3Q adapter must first pass the `m3q-oracle.so` preflight,
accept exactly one internally consistent verdict, and use a fresh boot session.
It must not substitute the generic cached-P0 or Shizuku route. The main payload
and the matching KernelSU loader may run only after that gate succeeds.

### `m3q-oracle.so`

- Size: 124,136 bytes
- SHA-256: `14c59d9acf5ce5d6c7399a2a28af97adf84eb882f855368febdc645cb074fbbe`
