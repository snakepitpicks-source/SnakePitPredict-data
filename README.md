# SnakePitPredict data · V1

Private evidence and result snapshots for [SnakePitPredict](https://github.com/snakepitpicks-source/SnakePitPredict).

`LATEST` identifies the current snapshot. Each snapshot contains `evidence/`, `results/` and a checksum manifest. JSON files are gzip compressed; read with Python `gzip.open(path, "rt")` or `gzip -dc path.json.gz`.

Exports exclude API keys, authorization, private dashboard responses, local feedback ledgers and SQLite databases. Original local evidence is untouched. Manifest checksums refer to sanitized export bytes; model input hashes retain original provenance and are not checksums of the sanitized files.

The initial snapshot covers 2026 Week 5. The current Saturday refresh contains 14 games, 614 player-market assessments, 6 stretch calls, 28 everyday takes and 18 conversation drafts. YouTube transcripts remain unavailable; official depth-chart coverage is partial. Calls are conditional scenarios, not priced bets or calibrated probabilities. Source gaps remain visible in the evidence and dashboard.

Code release: v1.1.0. Forecasts, everyday milestones and moderate positive/negative stretch calls are included. Full design, operations and storage limitations live in the code repository's docs/DATA_REPOSITORY.md and docs/V1_REBUILD.md.

Git archives persist; the five-cycle active-player cache policy applies to the local working store, not immutable Git history. Future snapshot storage should prioritize deltas and deduplicated history.
