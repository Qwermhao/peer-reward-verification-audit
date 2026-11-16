# What Peer Rewards Amplify

**Theory and a Zero-Reward Audit of AI Verification**  
Jiahao Chen, independent researcher. Apart Research AI × Epistemics Research Sprint, November 2026.

**[Download the complete code and evidence (5.31 MB)](https://raw.githubusercontent.com/Qwermhao/peer-reward-verification-audit/abc77e264b01952bb02f44fba5d390a1930e1730/PEG_Code_and_Evidence_v6.zip)** · [Evidence map](SUPPLEMENTARY_MATERIAL.md) · [Download checksum](SHA256SUMS)

The archive contains the complete program and supplementary reproducibility evidence. The report PDF was submitted separately to Apart Research. The download above is pinned to the submitted v6 snapshot.

## Main results

**A zero-reward intervention exposes what drives the released verifier's decisions.** Removing every peer reward leaves every original-order majority answer unchanged on 1,616 GPQA and ARC-Challenge questions. Those answers also match the fixed generator. For this released system and these cohorts, a reward-based explanation of the final majority decisions must account for a control that reaches exactly the same answers without rewards.

**We explain the effect mathematically and reproduce it in code.** An executable certificate shows how selected-answer normalization can make the PEG update copy its generator even when all rewards are zero. The project identifies a concrete computation behind the result and supplies a control that other researchers can run.

**The theory identifies when informative incentives amplify incorrect judgments.** For the specified binary DMI entropy learner, we completely characterize orientation basins and Nash limits. A full-support example proves that expected reward can rise while factual accuracy falls. This gives a precise reason to distinguish rising peer rewards from improving judgment.

**The finding survives changes in task grouping and broader validation.** Native and zero rewards differ on only 13 of 32,320 question-order comparisons across twenty regroupings. Validation adds 16,232 MMLU and ARC-Easy questions and an alternative-model ARC cohort, with 99.23–99.92% original-order native–zero agreement. A separate 120-configuration study tests finite-batch behavior with 2.4 million sampled batches.

Together, the proofs and matched interventions provide a practical audit method for determining which part of a self-verification pipeline changes its decisions. Coverage-aware scoring also separates answering more questions from improving accuracy on questions already answered. The exact learner and the released per-question program are analyzed separately, with assumptions and question-level evidence retained in the package.

## Use the code

Use **Python 3.12 or later** for the pinned dependencies and the quickstart below. The recorded analysis environment is Python 3.14.5, NumPy 2.5.4, and Matplotlib 3.11.2. The standard-library exact checks can be run separately on older Python versions as described inside the archive.

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

No API keys, model inference, weights, GPU, or paid services are needed. Exact verification runs offline. Native, order, and external replays first retrieve hash-pinned public inputs; subsequent analysis runs offline. The stochastic component repeats 2.4 million sampled batches and takes longer than the exact checks.

### Verify the download

Download [SHA256SUMS](https://raw.githubusercontent.com/Qwermhao/peer-reward-verification-audit/main/SHA256SUMS) into the same directory as the ZIP, then run one of these commands before extracting it:

```sh
# macOS
shasum -a 256 -c SHA256SUMS
# Linux
sha256sum -c SHA256SUMS
```

The expected archive SHA-256 is `59c5b3260f5e6fa3bbfa97ae11244455c2a7be1369eb6e9dc08725abfb0f9f74`.

### macOS certificate setup

Some python.org macOS installations need their certificate setup completed before Python can download HTTPS inputs. If native or order reproduction raises `CERTIFICATE_VERIFY_FAILED`, complete the installer's certificate setup. When `/etc/ssl/cert.pem` exists and is the trusted system certificate bundle, it can also be selected for that command:

```sh
SSL_CERT_FILE=/etc/ssl/cert.pem python tools/reproduce.py native --output ../peg-native-reproduction
```

Certificate verification and the downloaders' input-hash checks remain enabled.

## Package validation

Preparation checks on 16 November 2026 verified the public download against the local archive, all 181 payload-file checksums, ZIP integrity, all 29 Python files, and 135,744 saved prediction rows. A fresh exact reproduction passed all 20 primary checks and the addendum, covering 2,500 expected-payment cases and eight latent enumerations spanning 401,408 paths. The downloadable snapshot remains the submitted v6 artifact.

## Contents and provenance

Replay uses hash-pinned released probability files. Downloaders retrieve these public originals on demand; upstream CSVs/notebooks and benchmark question text are not mirrored in the archive. PDF reports, internal editorial reviews, working logs, old drafts, local environments, and caches are omitted.

See [SUPPLEMENTARY_MATERIAL.md](SUPPLEMENTARY_MATERIAL.md) for the archive's evidence map. Authorship and third-party provenance are documented in `NOTICE.md` inside the ZIP. No additional software license is asserted by this publication.
