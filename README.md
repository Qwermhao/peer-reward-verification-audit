# What Peer Rewards Amplify

**Theory and a Zero-Reward Audit of AI Verification**  
Jiahao Chen, independent researcher. Apart Research AI × Epistemics Research Sprint, November 2026.

The complete program and supplementary reproducibility evidence are in **[PEG_Code_and_Evidence_v6.zip](PEG_Code_and_Evidence_v6.zip)**. Open the ZIP file page and choose **Download raw file** to download it. The report PDF is submitted separately.

## Main results

- Exact orientation-basin and Nash-limit analysis for a specified binary DMI entropy learner, checked in 2,500 expected-payment cases and eight latent enumerations spanning 401,408 paths.
- An executable zero-reward certificate explains how selected-answer normalization in the released PEG update can copy its fixed generator.
- Native rewards, zero rewards, and the generator give identical original-order majority answers on all 1,616 GPQA and ARC-Challenge questions. Only 13 of 32,320 comparisons differ across twenty regroupings.
- Additional validation adds 16,232 MMLU and ARC-Easy questions plus an alternative-model ARC cohort, with 99.23–99.92% original-order native–zero agreement.
- A 120-configuration finite-batch study covers 2.4 million sampled batches and an oracle-centering control.

## Use the code

Unzip the archive. It creates a folder named `peer-reward-verification-audit` containing 182 files, including the complete scientific code, recorded numeric outputs, a supplementary index, source-provenance manifests, and a checksum manifest.

```sh
unzip PEG_Code_and_Evidence_v6.zip
cd peer-reward-verification-audit
python3 -m venv .venv
. .venv/bin/activate
python -m pip install -r requirements.txt
python tools/verify_manifest.py
python tools/reproduce.py exact --output ../peg-exact-reproduction
```

The full README inside the archive documents native replay, added datasets, complete order/coverage analysis, stochastic checks, and independent validation. The reproduction helper creates a new working copy and preserves the published outputs.

No API keys, model inference, weights, GPU, or paid services are needed. Replay uses hash-pinned released probability files. Downloaders retrieve these public originals on demand; upstream CSVs/notebooks and benchmark question text are not mirrored in the archive. PDF reports, internal editorial reviews, working logs, old drafts, local environments, and caches are omitted.

See [SUPPLEMENTARY_MATERIAL.md](SUPPLEMENTARY_MATERIAL.md) for the archive's evidence map. Authorship and third-party provenance are documented in `NOTICE.md` inside the ZIP. No additional software license is asserted by this publication.
