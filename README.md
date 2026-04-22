# ISC Grant Proposal: Evolving `mmints` from Citizen Science to Cyborg Science

[![build-status](https://github.com/mightymetrika/mmints_iscgrant_0426/actions/workflows/publish-proposal.yaml/badge.svg)](https://github.com/mightymetrika/mmints_iscgrant_0426/actions/workflows/publish-proposal.yaml)

This repository contains the R Consortium Infrastructure Steering Committee (ISC) grant proposal for updating the `mmints` R package. 

## Project Overview

In statistical methods research, a common anti-pattern exists: applied researchers frequently cite simulation results from original methods papers to justify their use of a statistical method, even when the original simulation parameters do not match their new study's specific context. The rigorous response is to run a **REPLEXT (replication and extension)** to re-test the simulation under the new parameters, but this is often prohibitive due to time, unreproducible code, or technical constraints.

While the `mmints` package currently powers web-based Shiny applications that crowdsource statistical exploration (citizen science), this relies entirely on human curiosity, leaving blind spots in the parameter space and a gap between web exploration and formal, research-grade publication.

This proposal seeks funding to transition `mmints` into a **"cyborg science"** environment by integrating two native AI Shiny modules:
1. **Intelligent Parameter Exploration:** A module where users can donate LLM API credits, allowing an AI to ingest research, analyze the open database, and intelligently search the parameter space to discover and save interesting edge cases.
2. **AI Reporting Module:** A conversational assistant that analyzes the database to draft comprehensive reports and generate the exact R code needed to run a full-scale, 10,000+ iteration REPLEXT on a server.

## Proof of Concept

This project is highly de-risked and builds upon existing infrastructure:
* **Deployed Apps:** `mmints` currently powers live citizen science apps (e.g., `npbreplext032`, `mmirreplext031`).
* **`shinypup` Prototype:** In September 2024, we successfully built and [live-streamed](https://www.youtube.com/watch?v=_KuTATJK7MA) a prototype AI agent called `shinypup` that interacted with our parameter spaces. This grant will fund the translation of that external browser-automation concept into stable, native R modules within `mmints`.

## The Team

**Mackson Ncube** (Principal Investigator)  
Statistician, Data Scientist, and Founder of Mightymetrika. 

## Building and Viewing the Proposal

This proposal is built using Quarto. To render the proposal locally:

1. Clone this repository.
2. Open the `isc-proposal.Rproj` file in RStudio.
3. Open `isc-proposal.qmd` and click **Render** to generate the PDF and HTML outputs.

### Automatically Generate the Proposal

This repository comes with a GitHub Actions setup to automatically render the proposal to HTML and PDF formats. To take advantage of it, you must publish the proposal to GitHub Pages interactively the first time.

From the command line, run `quarto publish gh-pages isc-proposal.qmd`. After this, the GitHub action will run every time you push a commit to the main branch. Your rendered proposal can then be viewed at `https://mightymetrika.github.io/mmints_iscgrant_0426/`.

## License

This proposal template is based on the [ISC Boilerplate](https://github.com/RConsortium/isc-proposal) and is licensed under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).