# SnakePitPredict data · V1

Private evidence and result snapshots for [SnakePitPredict](https://github.com/snakepitpicks-source/SnakePitPredict).

`LATEST` identifies the current snapshot. Each snapshot contains `evidence/`, `results/` and a checksum manifest. JSON files are gzip compressed; read with Python `gzip.open(path, "rt")` or `gzip -dc path.json.gz`.

Exports exclude API keys, authorization, private dashboard responses, local feedback ledgers and SQLite databases. Original local evidence is untouched. Manifest checksums refer to sanitized export bytes; model input hashes retain original provenance and are not checksums of the sanitized files.

The initial snapshot covers 2026 Week 5: 14 games and 616 player-market assessments. Calls are conditional scenarios, not priced bets or calibrated probabilities. Source gaps remain visible in the evidence and dashboard.

Code release: v1.0.3. Full design, operations and storage limitations live in the code repository's docs/DATA_REPOSITORY.md and docs/V1_REBUILD.md.

Git archives persist; the five-cycle active-player cache policy applies to the local working store, not immutable Git history. Future snapshot storage should prioritize deltas and deduplicated history.
