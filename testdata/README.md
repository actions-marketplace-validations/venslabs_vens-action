# Test fixtures

- `config.yaml` — minimal project context (`exposure`, `data_sensitivity`,
  `business_criticality`) required by `vens generate`.

Scan reports are generated on the fly in CI by running real Trivy and Grype
against a pinned image — see `.github/workflows/test-action.yml`. The matrix
covers the two latest releases of each scanner so we catch JSON schema drift
as soon as it ships.
