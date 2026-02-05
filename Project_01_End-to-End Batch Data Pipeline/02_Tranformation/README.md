# Silver Layer – Data Cleaning and Standardization

## Overview
The Silver layer is responsible for transforming raw ingested data from the Bronze layer
into clean, standardized, and quality-checked datasets.

This layer applies schema enforcement, data quality rules, and normalization logic,
while preserving traceability back to the original source data.

---

## Purpose of the Silver Layer
The Silver layer prepares data for analytical modeling by:
- Enforcing correct data types
- Handling duplicates and invalid records
- Normalizing categorical values
- Applying basic business validation rules

Unlike the Bronze layer, the Silver layer is **not immutable** and reflects
controlled transformations required for analytics and downstream consumption.

---

## Input
- Source: Bronze layer datasets
- Format: CSV (batch processing)
- Data characteristics:
  - Minimal cleaning
  - Source-aligned schema
  - Ingestion metadata included

---

## Output
- Target: Silver layer datasets
- Format: CSV
- Characteristics:
  - Cleaned and standardized
  - Type-safe columns
  - Analytics-ready
  - Quality-validated

---

## Transformations Applied
Typical transformations include:
- Data type casting (string → numeric / timestamp)
- Trimming and standardizing text fields
- Normalizing categorical values (e.g. gender)
- Deduplication based on business keys
- Data quality validation (ranges, null checks)
- Metadata enrichment (Silver processing timestamp)

---

## Data Quality Principles
Before applying transformations, datasets are profiled to:
- Identify duplicate records
- Measure null values
- Detect invalid ranges
- Understand value distributions

All cleaning rules are applied **after profiling**, ensuring that
data transformations are intentional and explainable.

---

## Folder Structure
