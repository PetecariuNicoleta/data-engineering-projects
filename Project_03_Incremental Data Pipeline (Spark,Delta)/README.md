# Incremental Data Pipeline

## Overview
This project implements an incremental batch data pipeline using Apache Spark
and Delta Lake concepts.

The goal is to demonstrate how to efficiently process only new or changed data
instead of performing full reloads on every run.

---

## Business Context
A company receives daily updates to transactional data.
Reprocessing all historical data every day is inefficient and costly,
so an incremental approach is required.

---

## Pipeline Design
The pipeline processes data incrementally using:
- Watermark-based filtering
- Deduplication logic
- Delta Lake MERGE operations

This ensures the pipeline is:
- Idempotent
- Scalable
- Production-ready

---

## Incremental Strategy
- Track the last processed timestamp (watermark)
- Read only records newer than the watermark
- Deduplicate incoming data
- Upsert records into a Delta table using `MERGE INTO`

---