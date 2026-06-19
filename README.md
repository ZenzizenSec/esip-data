<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/5fd38838-7754-483b-a1eb-c88ac774dc26" />

---

## 📥 Download Current Snapshot

[![Download Latest Snapshot](https://img.shields.io/badge/Download-Latest%20Snapshot-blue?style=for-the-badge)](https://github.com/ZenzizenSec/esip-data/releases/latest/download/ESIP-daily.json)

---
# ESIP Public Dataset

This repository carries the public, daily-refreshed snapshot of the
**Exposure Signal Intelligence Platform (ESIP)** signal feed, together
with the data license, schema documentation, and integration guidance
needed to consume it.

It is intended for security teams, developers, researchers, and
vendors who want to combine exposure intelligence signals with their
own asset and business context.

---

## What is ESIP?

**ESIP (Exposure Signal Intelligence Platform)** is a global exposure
intelligence service that tracks changes in the threat landscape for
known vulnerabilities.

ESIP does **not** scan assets and does **not** manage vulnerabilities.

Instead, ESIP answers a different question:

> *What is changing in the threat landscape for this vulnerability,
> and how dangerous is it becoming?*

Organizations combine ESIP signals with their own asset and business
context to support better prioritization and decision-making.

---

## What's in this repository

| File | Purpose |
|---|---|
| `ESIP-daily.json` (Release asset) | The current daily snapshot of the public dataset. Replaced on every publication cycle. Served under the rolling `daily-latest` release. |
| `LICENSE_DATA.md` | The data license that governs use of the snapshot. Read this before integrating. |
| `README.md` | This file. |

The snapshot file is **never committed** to the repository. It lives
only as a GitHub Release asset, replaced each publication cycle. There
is no per-day history on this repo. If you need historical snapshots,
see the commercial product.

---

## How to consume

There are two access paths. Pick whichever fits your workflow.

### Option 1. Daily snapshot file (no key required)

A single stable URL always points at today's snapshot:

```
https://github.com/zenzizensec/esip-data/releases/latest/download/ESIP-daily.json
```

Fetch it once per day, after the daily publication cycle completes:

```bash
curl -L -o esip-daily.json \
  https://github.com/zenzizensec/esip-data/releases/latest/download/ESIP-daily.json
```

The file is a JSON document with a top-level snapshot envelope and a
`data` array of CVE records. See the snapshot shape sample below for
the field list, and [exposuresignal.io/docs](https://www.exposuresignal.io/docs/)
for the full field reference, allowed values, and boundary
documentation.

### Option 2. Live free-tier API (key required)

For point lookups by CVE ID, the free-tier API serves the same dataset
on demand:

```
GET https://public.exposuresignal.io/v1/cves/CVE-2023-22527
X-API-Key: YOUR_API_KEY
```

The list endpoint returns paginated bare metadata (CVE ID + exposure
class) for the whole snapshot:

```
GET https://public.exposuresignal.io/v1/cves?page=1
X-API-Key: YOUR_API_KEY
```

Page size is fixed at 100. Both endpoints return the same
`schema_version: "1.0"` payload as the snapshot file.

---

## Snapshot shape (summary)

```json
{
  "snapshot_generated_at": "2026-06-18T03:00:00Z",
  "schema_version": "1.0",
  "cve_count": 27074,
  "dataset_scope": "signal_set_only",
  "dataset_type": "public_snapshot",
  "record_definition": "CVE with at least one observable signal",
  "attribution": "Data provided by ESIP / ZenzizenSec ...",
  "license_url": "https://github.com/zenzizensec/esip-data/blob/main/LICENSE_DATA.md",
  "data": [
    {
      "cve_id": "CVE-2023-22527",
      "exposure_class_id": "CVE-2023-22527",
      "attack_techniques": [
        { "technique_id": "T1190", "technique_name": "...", "mapping_confidence": "high", "mapping_source": "esip" }
      ],
      "observation_events": [
        { "observation_type": "kev_inclusion", "source_name": "CISA Known Exploited Vulnerabilities", "observed_at": "2026-04-30T18:58:53.831062Z" }
      ],
      "detection_capability": null
    }
  ]
}
```

The dataset includes only CVEs with at least one observable signal
(KEV inclusion, public PoC, exploit module reference, etc.). It is
intentionally narrower than the full CVE corpus.

The full field reference, enumerations (allowed values for
`observation_type`, supported `source_name` values, `mapping_confidence`
levels, etc.), and the data-publication boundary documentation (what
ships, what is intentionally stripped, and why) live at
[exposuresignal.io/docs](https://www.exposuresignal.io/docs/).

---

## Getting an API key

The free-tier API requires an API key in the `X-API-Key` header.

Email signup is at [https://www.exposuresignal.io](https://www.exposuresignal.io).
During the early-access period, keys are issued manually by the
ZenzizenSec team after signup. You do not need a key to use the daily
snapshot file (Option 1 above).

If a key already exists for your email, requesting a new one will
rotate the old key (the previous key is invalidated).

---

## License and acceptable use

Use of the snapshot file and the free-tier API is governed by
[`LICENSE_DATA.md`](./LICENSE_DATA.md) in this repository (ESIP Data
License v1.2 or later).

In short:

- Use the data for research, tools, integrations, and most commercial
  work, with attribution.
- Do not build a competing signal intelligence product with our free
  data, redistribute the dataset as a standalone product, or publish
  accuracy benchmarks of ESIP without written permission.
- The data is provided with no warranty.

Read the license file for the binding terms. The summary above is for
convenience only.

---

## Versioning

The snapshot envelope carries a top-level `schema_version` field
(currently `"1.0"`). Field additions are backward-compatible. Any
breaking change to a published field name, type, or semantic increments
the major component and is announced in advance.

Field-level definitions, the supported value ranges, and the change log
across versions live at
[exposuresignal.io/docs](https://www.exposuresignal.io/docs/).

---

## Further documentation

Detailed reference material lives at
[exposuresignal.io](https://www.exposuresignal.io):

- **API reference** for the live free-tier endpoints, including
  request/response examples and rate limits.
- **Schema reference** with the full field-by-field definition of the
  snapshot envelope and CVE records.
- **Data publication boundary** documentation describing what ships in
  the public dataset, what is intentionally stripped, and the
  reasoning for each decision.
- **Status and announcements** for snapshot publication issues, schema
  changes, and rolling-key rotations.

This repository keeps a deliberately small surface (snapshot file +
license + this README). The detail lives on the product site so that
both consumption paths (file and API) share one source of truth.

---

## Contact

**ZenzizenSec Inc.**

- Website: [https://www.zenzizensec.com](https://www.zenzizensec.com)
- Product: [https://www.exposuresignal.io](https://www.exposuresignal.io)

For enterprise access (richer signal data, historical replay,
ATT&CK mapping, programmatic onboarding) reach out via the website.
