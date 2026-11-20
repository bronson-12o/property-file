# Property File

A document workspace for checking property financial information against its source pages.

I built Property File to keep a property question, extracted financial observations, and supporting document pages together. A figure needs its reporting period, basis, currency, scale, and review status before someone can use it confidently.

## What it does

- Ingests documents and extracts text and financial observations.
- Retrieves relevant passages for property questions.
- Opens the supporting page beside an observation.
- Keeps machine extraction and reviewer acceptance separate.
- Uses deterministic arithmetic for supported financial calculations and can abstain when the evidence is insufficient.

## Architecture

Document intake → Python extraction and observations → local Qdrant retrieval → FastAPI endpoints → React workspace and source-page review.

The local application uses Python, FastAPI, React, Qdrant, and PDF text retrieval. Original documents and persistent application data are kept out of this repository.

## Open the project

[Interactive fictional demo](https://bronsonhatch.com/property-file-demo) · [Case study](https://bronsonhatch.com/#work/propertyfile) · [Portfolio](https://bronsonhatch.com)

This repository is a public project overview. The application source is maintained privately, so cloning this showcase does not start a working server. The public demo uses a saved, verified extraction from a fictional statement. Visitors can select figures and inspect their source locations. It performs no uploads or live AI calls and does not connect to the private workspace. The full application runs locally.

## Evidence and limits

Property File is a local application with automated regression and selected real-source development checks. Nine selected account/month/value associations on three pages at one property pass on both Mac and Linux; this is a small development check, not a full ledger audit. Passing a known case verifies that case; it does not establish unfamiliar-document accuracy. The public-reference evaluation remains unsealed pending independent human source review. Machine-generated suggestions must not be labeled human verified.

Production multi-user authorization, hostile-document isolation, and broader independent evaluation remain release work. No production security certification, population accuracy percentage, or independently approved financial answer is claimed here.

## My work

Document ingestion, evidence-aware data structures, retrieval endpoints, source-page UI, financial validation, and regression checks.

[Use and attribution](USE-AND-ATTRIBUTION.md). Publisher source documents are not redistributed in this showcase.
