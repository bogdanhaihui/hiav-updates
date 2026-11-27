# HiAV 2.5.95 — development preview

Validated Windows x64 development build. Local test signing only; not a production-certified release.

- Faster complete rule matching without truncating inspection or reusing stale execution verdicts.
- Bounded asynchronous admission for 8 execution workers, 2 pre-write workers and 64 captured messages.
- Kernel activation/deactivation persists across service restarts and Windows reboots.
- Identity-checked image leases remain pinned through analysis and the native reply.
- Rollback captures are staged and adopted only after acknowledged pre-write replies.
- Post-write observers no longer manufacture original-file baselines. Legacy manifests are retained for review.

Validation: 1,302 release checks passed; production-ACL groups passed separately; two actual VM reboots;
20/20 concurrent clean launches; synthetic ransomware recovery with 12/12 original document hashes;
full host rebuild with the driver connected. One observed Codex launch fell from 9.2 s to 5.5 s;
this is a local measurement, not a general performance guarantee.

Use the manual installer and README-TESTING.md in an approved Windows lab. The kernel driver is a separate
test-signed asset. No Defender exclusions or disabling are required or included. Automatic client upgrade,
general DLL/pre-existing-section coverage, production signing and independent efficacy certification remain open.

The stable update feed is not promoted by this preview release.
