# Verified HiAV bootstrap feed

`feed.json` contains 3,181 SHA-256 indicators from positive daily MalwareBazaar sample-extraction CSV rows that also appear in HiAV's staged SHA-256 list, plus the SHA-256 of the exact 68-byte EICAR anti-malware test file. The EICAR entry is a transport and verification canary. `provenance.json` records the input CSV digests, matching-row counts, and final feed digest. Eleven distributed samples were confirmed by MalwareBazaar's `get_info` API; 236 signed Windows reference files had no matching hash.

`feed.json.sig` is a 64-byte ECDSA P-256/SHA-256 signature over the exact bytes of `feed.json`, verified against the public key pinned by HiAV. The original `signatures/feed.json` remains untouched because its provenance is unreviewed. A match to the CSVs is evidence of sample extraction, not a guarantee that each record is perfectly labeled; additions require the same review process.

Do not add indicators here from public Firestore reports or crawler candidates without source validation and a separate signing review.
