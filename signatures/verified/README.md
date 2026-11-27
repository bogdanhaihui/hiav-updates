# Verified HiAV bootstrap feed

`feed.json` contains one SHA-256 indicator: the exact 68-byte EICAR anti-malware test file. It is a transport and verification canary, not a general malware intelligence feed. The source is EICAR's published test string; the hash is calculated from those ASCII bytes.

`feed.json.sig` is a 64-byte ECDSA P-256/SHA-256 signature over the exact bytes of `feed.json`, verified against the public key pinned by HiAV. The original `signatures/feed.json` remains untouched because its provenance is unreviewed.

Do not add indicators here from public Firestore reports or crawler candidates without source validation and a separate signing review.
