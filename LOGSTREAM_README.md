# LOGSTREAM — Distributed Security Log Analytics Pipeline

A distributed log-ingestion and processing pipeline for collecting, parsing, and analyzing application, system, and security events at scale.

## Overview

LOGSTREAM collects events from multiple sources via Apache Kafka and processes them through Spark-based ETL to produce analytics-ready datasets for security monitoring, system trend analysis, and operational reporting.

## Features

- **Distributed ingestion** — collects application, system, and security events from multiple sources using Apache Kafka
- **Spark-based ETL** — parsing, normalization, enrichment, deduplication, and aggregation of large-scale log data
- **Analytics-ready storage** — processed data written to AWS S3 and PostgreSQL for querying security events and system trends
- **Scalable design** — built to handle high-volume, multi-source log streams

## Tech Stack

`Python` · `Apache Kafka` · `PySpark` · `PostgreSQL` · `AWS S3` · `Docker`

## Architecture

```
Log Sources (app / system / security events)
        │
        ▼
   Apache Kafka (distributed ingestion)
        │
        ▼
  Spark ETL (parse, normalize, enrich, dedupe, aggregate)
        │
        ▼
  AWS S3 + PostgreSQL (analytics-ready storage)
        │
        ▼
  Querying — security events, system trends, operational metrics
```

## Setup

```bash
# Clone the repo
git clone https://github.com/Sowjanya12125/logstream.git
cd logstream

# Start Kafka + supporting services
docker-compose up --build

# Run the ETL pipeline
python run_pipeline.py
```

*(Adjust the above to match your actual folder structure and entry points before pushing.)*

## Project Structure

```
logstream/
├── ingestion/         # Kafka producers/consumers
├── etl/                # Spark transformation and enrichment jobs
├── storage/            # S3 and PostgreSQL writers
├── docker/             # Dockerfiles and docker-compose config
└── README.md
```

## Status

Built in 2025 as a distributed security log analytics project, focused on turning raw multi-source log data into queryable operational and security insights.
