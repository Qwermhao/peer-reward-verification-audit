# Supplementary material

Download **[PEG_Code_and_Evidence_v6.zip](PEG_Code_and_Evidence_v6.zip)**, the complete public code-and-evidence bundle accompanying **What Peer Rewards Amplify: Theory and a Zero-Reward Audit of AI Verification**, by Jiahao Chen.

The report PDF is submitted separately.

| Evidence | Location inside the ZIP |
|---|---|
| Scientific overview and reproducibility commands | `README.md`, `SUPPLEMENTARY_MATERIAL.md` |
| DMI theory and exact verification | `theory/`, `exact/` |
| Original PEG replay and reward controls | `native/` |
| Complete order comparisons and coverage decomposition | `revision/order_coverage/` |
| Added datasets and alternative model trio | `revision/external/` |
| Finite-batch study and oracle-centering control | `revision/stochastic/` |
| Independent computational and label checks | `validation/`, `revision/validation/` |
| Current public-file checksums | `MANIFEST.json` |
| Authorship and upstream provenance | `NOTICE.md`, input manifests |

The archive contains 182 files. Its checksum manifest covers every other payload file and can be verified with `python tools/verify_manifest.py` after extraction. The archive's file SHA-256 is `59c5b3260f5e6fa3bbfa97ae11244455c2a7be1369eb6e9dc08725abfb0f9f74`.

Upstream probability CSVs/notebooks, question text, report PDFs, internal editorial reviews, and working logs are excluded. Hash-verifying downloaders recover the upstream files needed for replay. No API key or new model inference is required.
