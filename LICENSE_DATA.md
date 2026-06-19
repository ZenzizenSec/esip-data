# ESIP Data License
> Version 1.2 — 2026-04-08
> Issued by: ZenzizenSec Inc. — Ontario, Canada
> Governing Law: Province of Ontario, Canada
> Supersedes: ESIP Data License v1.1 (2026-04-08)

---

## Plain-Language Summary

This license governs your use of data published by the Exposure Signal Intelligence Platform (ESIP) through its free public surfaces (GitHub daily snapshot and free public API).

**Short version:**
- You can use ESIP free data for most purposes (research, tools, integrations, commercial work) as long as you credit us.
- You cannot build a competing signal intelligence product using our free data without our written permission.
- You cannot redistribute the dataset as a standalone product without our written permission.
- You cannot benchmark or publish accuracy comparisons of ESIP data without our written permission.
- You cannot use it if you are on a Canadian government sanctions list.
- The data comes with no warranty. Use it at your own risk.

The full terms below govern. The summary is for convenience only and does not constitute legal advice.

---

## 1. Definitions

**"ESIP"** means the Exposure Signal Intelligence Platform, operated by ZenzizenSec Inc.

**"ZenzizenSec"** means ZenzizenSec Inc., a company incorporated in Ontario, Canada.

**"Licensed Data"** means any data published by ESIP through its free public surfaces, including the GitHub daily snapshot and the free public API at public.exposuresignal.io.

**"You"** means the individual, organization, or automated system accessing or using the Licensed Data.

**"Attribution"** means the credit statement required under Section 4 of this license.

**"Competing Product"** means any commercial product or service that provides CVE risk intelligence, vulnerability signal scoring, exploitation likelihood assessment, or materially similar signal intelligence capability, where ESIP Licensed Data is used as a foundational input. A product may be considered a Competing Product even if signal intelligence is not its sole or primary function, where ESIP Licensed Data materially enables, differentiates, or constitutes a significant portion of the product's intelligence capability.

**"Redistribution"** means making the Licensed Data or a derivative of it available to third parties as a standalone dataset, data feed, or data product, whether for free or for payment.

**"Derived Intelligence"** means any data element produced through interpretation, correlation, scoring, or prioritization of raw observations. Examples include but are not limited to: risk scores, signal states, exploitation maturity classifications, remediation urgency ratings, and threat posture assessments. Raw observation events (exploit publication, KEV inclusion, PoC availability) are not Derived Intelligence. The boundary between raw observation and Derived Intelligence is defined in the ESIP Data Publication Boundary document.

---

## 2. Grant of License

Subject to the terms of this license, ZenzizenSec grants You a non-exclusive, worldwide, royalty-free license to:

**a) Use** the Licensed Data for any lawful purpose, including personal, academic, research, non-profit, open-source, and commercial purposes, except as restricted in Section 3.

**b) Copy and store** the Licensed Data for internal use.

**c) Create derivative works** from the Licensed Data, including processing, transforming, combining with other data, or embedding in tools and applications, subject to Attribution requirements in Section 4.

**d) Display** the Licensed Data or derivatives publicly, subject to Attribution requirements in Section 4.

This license does not grant any rights to ESIP's commercial data, Derived Intelligence, scoring methodology, signal weighting logic, or any data element not included in the defined free public surfaces.

---

## 3. Restrictions

### 3.1 Competing Products

Use of Licensed Data as a foundational input to a Competing Product requires explicit written permission from ZenzizenSec.

To request permission: legal@zenzizensec.com. ZenzizenSec will respond to permission requests within 30 business days. Absence of a response does not constitute permission.

This restriction applies regardless of whether the Competing Product is commercial or free.

This restriction does **not** apply to:
- Security tools that use ESIP data as one input among many (scanners, SIEMs, dashboards, vulnerability management platforms) where ESIP signal intelligence does not materially enable or differentiate the product
- Research tools that analyze or visualize ESIP data without replicating or competing with the ESIP signal intelligence function

### 3.2 Redistribution

Redistribution of the Licensed Data as a standalone dataset, data feed, or data product requires explicit written permission from ZenzizenSec. This applies whether or not You charge for the redistribution.

This restriction does **not** apply to:
- Sharing individual data points or small excerpts with Attribution (e.g., citing a CVE classification in a blog post, report, or tool output)
- Including ESIP data as embedded output within a tool or application (e.g., a scanner that shows ESIP exposure class alongside its own findings)

### 3.3 Benchmarking and Comparative Analysis

You may not publish performance benchmarks, accuracy comparisons, coverage evaluations, or competitive assessments of ESIP Licensed Data without prior written permission from ZenzizenSec. This includes comparisons against other CVE intelligence sources, vulnerability databases, or signal intelligence platforms.

This restriction does not apply to internal evaluations conducted solely for Your own procurement decisions, provided the results are not published or shared externally.

### 3.4 Prohibited Parties

You may not use Licensed Data if You are:
- An entity listed on a Canadian government sanctions list or restricted party list
- An entity subject to Canadian export control restrictions that would prohibit receipt of this data
- Acting on behalf of any such entity

### 3.5 Attribution Removal

You may not remove, obscure, replace, or misrepresent the Attribution required under Section 4.

### 3.6 Misrepresentation

You may not represent ESIP Licensed Data as your own original data, claim authorship of the Licensed Data, or remove or alter any metadata indicating ESIP as the source.

### 3.7 Website Scraping

Automated scraping of the ESIP website CVE query tool beyond reasonable personal research use is prohibited. The GitHub daily snapshot and free public API exist for programmatic access. Use them.

---

## 4. Attribution Requirements

When You use, display, embed, or publish Licensed Data or derivatives in any context accessible to others, You must include the following Attribution:

> Data provided by ESIP / ZenzizenSec — [www.exposuresignal.io](https://www.exposuresignal.io)

**Where Attribution must appear:**
- In the user interface where ESIP data is displayed, if any
- In documentation, README files, or About sections of tools that use ESIP data
- In reports, publications, or papers that cite ESIP data
- In any marketing materials that reference ESIP data as an input

**Attribution format:**
- Both the text credit and the link are required
- The link must point to www.exposuresignal.io or a ZenzizenSec-operated page
- Attribution must be reasonably visible. It may not be hidden in a font size materially smaller than surrounding text or placed where a reasonable reader would not encounter it

**Upstream source attribution:**
ESIP Licensed Data is derived from open-source upstream sources with their own attribution expectations. Where Your use makes it appropriate, You should also credit:
- FIRST.org / EPSS team (for EPSS-derived data)
- CISA (for KEV-derived data)
- Offensive Security / ExploitDB (for exploit-derived data)
- Rapid7 / Metasploit contributors (for Metasploit-derived data)

This is a best-practice recommendation, not a requirement of this license. ESIP's Attribution requirement does not excuse You from any upstream attribution obligations that may arise independently.

---

## 5. No Warranty

THE LICENSED DATA IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED.

ZENZIZENSEC MAKES NO WARRANTIES REGARDING:
- Accuracy or completeness of the Licensed Data
- Fitness of the Licensed Data for any particular purpose
- Availability or continuity of the free data surfaces
- Timeliness or freshness of the Licensed Data
- Absence of errors, omissions, or data quality issues

THE LICENSED DATA IS NOT SECURITY ADVICE. It is threat landscape context intended to inform (not direct) security decisions. You are solely responsible for determining the fitness of the Licensed Data for your specific use case before relying on it in any operational context.

---

## 6. Limitation of Liability

TO THE MAXIMUM EXTENT PERMITTED BY ONTARIO LAW, ZENZIZENSEC IS NOT LIABLE FOR ANY DAMAGES ARISING FROM YOUR USE OF THE LICENSED DATA, INCLUDING BUT NOT LIMITED TO:

- Direct, indirect, incidental, special, or consequential damages
- Missed security patches or incorrect vulnerability prioritization
- Breach costs, regulatory penalties, or business losses
- Data inaccuracies or coverage gaps
- Service unavailability or publication schedule changes

YOUR USE OF THE LICENSED DATA IS ENTIRELY AT YOUR OWN RISK.

---

## 7. Schema and Data Changes

ZenzizenSec reserves the right to modify, add, remove, or restructure any data element in the Licensed Data at any time. ESIP will make best efforts to communicate material schema changes in advance through:
- [https://www.exposuresignal.io/docs/](https://www.exposuresignal.io/docs/)
- GitHub repository release notes

No minimum notice period is guaranteed. Consumers are responsible for monitoring these channels. You should not build critical production systems on Licensed Data without accepting that the schema and content may change without notice.

---

## 8. Data Publication Schedule

ZenzizenSec publishes the Licensed Data once every 24 hours on a schedule of its own choosing. The publication time may vary. Consumers receive the data as it exists at the time of publication. No real-time guarantee, intra-day freshness commitment, or fixed publication time is made. ZenzizenSec reserves the right to change the publication schedule at any time without notice.

The free-tier data surfaces are provided on a best-effort basis and are not subject to any service level agreement (SLA).

ZenzizenSec reserves the right to throttle, suspend, or block access to the free-tier data surfaces at its sole discretion, including in response to abusive usage, excessive automated access, or behavior that threatens the stability of the service.

---

## 9. Data Retention and Historical Data

The GitHub daily snapshot is published as a single replaceable release asset, `ESIP-daily.json`, attached to a rolling `daily-latest` release on the public ESIP data repository. The asset is overwritten in place with each publication cycle. The repository does not retain a commit history of the data file. The only addressable copy of the data is the current asset; prior cycles are not preserved on the publication surface. Consumers who require historical data must maintain their own archives by pulling the snapshot on their own schedule at their own infrastructure cost. ZenzizenSec is not responsible for data consumers fail to retrieve.

ZenzizenSec reserves the right to retain or remove any version of the Licensed Data at its sole discretion, and to move any data element from the free tier to the commercial tier or withdraw it from publication entirely. Best efforts will be made to communicate material changes through the channels in Section 7 in advance, but no minimum notice period is guaranteed.

---

## 10. Termination

### 10.1 By ZenzizenSec

ZenzizenSec may terminate Your license immediately and without notice if You:
- Violate any restriction in Section 3
- Fail to include Attribution as required by Section 4
- Use the Licensed Data in a manner that violates applicable law
- Are found to be a prohibited party under Section 3.4

### 10.2 Effect of Termination

Upon termination, You must cease all use of the Licensed Data and destroy any copies in Your possession, except for archival copies retained solely for legal, regulatory, or backup purposes, provided those copies are not actively used. Termination does not affect the rights of third parties who received Licensed Data from You in compliance with this license before termination.

### 10.3 By You

You may stop using the Licensed Data at any time. No notice to ZenzizenSec is required.

---

## 11. Severability

If any provision of this license is found to be unenforceable or invalid under applicable law, that provision shall be modified to the minimum extent necessary to make it enforceable, or severed if modification is not possible. The remaining provisions of this license shall continue in full force and effect.

---

## 12. Governing Law and Disputes

This license is governed by the laws of the Province of Ontario and the federal laws of Canada applicable therein, without regard to conflict of law principles.

Any dispute arising under this license will be resolved in the courts of the Province of Ontario, Canada. You consent to the personal jurisdiction of those courts.

---

## 13. Entire Agreement

This license, together with the ESIP Data Publication Boundary document, constitutes the entire agreement between You and ZenzizenSec regarding use of the Licensed Data. It supersedes any prior agreements or understandings on this subject.

---

## 14. Contact

For licensing permissions, attribution questions, benchmarking requests, or to report violations:

**ZenzizenSec Inc.**
Ontario, Canada
legal@zenzizensec.com
www.zenzizensec.com

---

*ESIP Data License v1.2 — ZenzizenSec Inc. — Ontario, Canada*
