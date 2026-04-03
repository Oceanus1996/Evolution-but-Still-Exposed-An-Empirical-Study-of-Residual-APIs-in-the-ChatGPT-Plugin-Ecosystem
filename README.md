# Evolution but Still Exposed: An Empirical Study of Residual APIs in the ChatGPT Plugin Ecosystem

FSE Companion '26, July 5–9, 2026, Montreal, QC, Canada

## Repository Structure

```
├── data/
│   ├── baseline/
│   │   ├── Plugin inconsistency and security.xlsx   # 2024 baseline: 1030 plugins with historical manifest/auth/spec
│   │   └── plugin_categories.xlsx                   # Plugin category labels
│   ├── rq1/
│   │   ├── backend_probe_results.xlsx     # 4-layer probe results for 1030 plugins (Tables 1–2)
│   │   └── rq1_before_after.xlsx          # 2024→2026 status transitions
│   └── rq2/
│       ├── rq2_endpoint_classification.xlsx   # 173 endpoint capability classification (Table 3)
│       ├── rq2_table4_hidden_endpoints.xlsx   # 38 hidden backend endpoints returning HTTP 200 (Table 4)
│       └── rq2_case_studies.xlsx              # Case study test records (Figures 2 & 3)
├── src/
│   ├── rq1/
│   │   ├── backend_probe.py         # Layered probe: domain → manifest → spec → endpoints
│   │   └── rq1_before_after.py      # Compare 2024 baseline with 2026 probe results
│   └── rq2/
│       ├── rq2_attack_surface.py    # Classify endpoint capabilities (write/PII/proxy) from OpenAPI specs
│       └── rq2_historical_probe.py  # Probe hidden backends using historical API spec URLs
└── README.md
```
