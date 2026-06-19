<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/5fd38838-7754-483b-a1eb-c88ac774dc26" />

# ESIP API -- Community Repository

Welcome to the public repository for the **Exposure Signal Intelligence
Platform (ESIP)**.

This repository provides documentation, examples, and integration
guidance for the ESIP public API.\
It is intended for security teams, developers, researchers, and vendors
who want to consume exposure intelligence signals and integrate them
into their own workflows, platforms, or analysis pipelines.

------------------------------------------------------------------------

## What is ESIP?

**ESIP (Exposure Signal Intelligence Platform)** is a global exposure
intelligence service that tracks changes in the threat landscape for
known vulnerabilities.

ESIP does **not** scan assets and does **not** manage vulnerabilities.

Instead, ESIP answers a different question:

> *What is changing in the threat landscape for this vulnerability, and
> how dangerous is it becoming?*

Organizations combine ESIP signals with their own asset and business
context to support better prioritization and decision-making.

------------------------------------------------------------------------

## What This Repository Contains

-   Public API documentation
-   Example API queries
-   Sample response formats
-   Integration guidance
-   Usage policies and rate limits
-   Changelog and versioning notes

This repository does **not** contain production service code.

------------------------------------------------------------------------

## Getting an API Key

To obtain an API key:

1.  Visit the ESIP registration page.
2.  Enter your email address.
3.  Confirm ownership of the email.
4.  Receive and copy your API key.

If a key already exists for your email address, a new key will be issued
and the previous key will be invalidated.

------------------------------------------------------------------------

## Example API Request

GET /api/v1/exposures/CVE-2023-22527\
Authorization: Bearer YOUR_API_KEY

------------------------------------------------------------------------

## Usage Expectations

This public API is designed to:

-   Support research and defensive security work
-   Enable integration into vulnerability management workflows
-   Provide transparent exposure intelligence signals

It is **not** intended for:

-   High-volume scraping
-   Resale of raw data
-   Unauthorized redistribution

------------------------------------------------------------------------

## Versioning

The API follows semantic versioning principles.

Breaking changes will only occur in new major versions.

------------------------------------------------------------------------

## Contact

For questions, support, or enterprise access:

**ZenzizenSec Inc.**\
https://zenzizensec.com or https://www.exposuresignal.io 
