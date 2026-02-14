# Content Ops Data Architecture

## System Overview
This repository contains the data schema for a Human-in-the-Loop (HITL) content orchestration engine. The system utilizes React and TypeScript to ingest this structured data and programmatically generate SEO-aligned educational content.

## The Schema (`contentops_data_schema.json`)
The included JSON file demonstrates the strict typing used to govern the generative AI process. It acts as the "Single Source of Truth" for the application state.

### Key Structural Components:
* **Nodes Array:** Defines individual content assets with unique UUIDs.
* **Cluster Taxonomy:** Assigns semantic grouping for topical authority mapping.
* **Interlinking Logic:** The `internal_links` array enforces bidirectional navigation paths between "Pillar" and "Cluster" content, preventing orphan pages.
* **Offer Mapping:** The `coreOfferId` field programmatically binds content nodes to specific conversion assets (e.g., PDFs, Courses), ensuring logical user journeys.

## Usage
This data layer feeds into a custom "Judge" module (Audit System) that verifies generated HTML against the defined constraints in this schema, ensuring structural integrity before publication.
