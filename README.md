# Dream Homes NYC

Dream Homes NYC is a course project for a fictional New York City real estate agency. The repository packages a finalized PostgreSQL schema, synthetic relational data, ETL/loading code, analytical SQL procedures, and support materials used for reporting and dashboard work.

The project is organized to support both transactional database loading and business analysis. Core entities include offices, employees, agents, clients, properties, listings, inquiries, appointments, open houses, and completed transactions.

## Project Snapshot

- PostgreSQL relational model with 16 tables
- 13,080 synthetic records in a referentially ordered CSV dataset
- Python ETL built with pandas and SQLAlchemy
- Analytical SQL covering sales, rentals, listings, clients, and agent performance
- Supporting [ERD](docs/erd/dreamhomes_nyc_erd.pdf), [final report](docs/final/dreamhomes_nyc_final_report_group6.pdf), [presentation](docs/final/dreamhomes_nyc_final_presentation.pdf), and [dashboard screenshots](dashboards/screenshots/)

## Repository Contents

- `sql/schema/` contains the final PostgreSQL schema. The canonical file is `dreamhomes_postgres_schema.sql`.
- `sql/analysis/` contains analytical SQL queries used for project reporting and dashboard metrics.
- `scripts/etl/` contains the Python loader used to create tables and insert CSV data.
- `data/raw/` contains the full synthetic CSV dataset used for loading the database.
- `data/sample/` contains small example CSV extracts for quick review.
- `data/metadata/` contains row-count, load-order, and dataset volume notes.
- `docs/erd/` contains the ERD PDF and ERD notes.
- `dashboards/screenshots/` contains dashboard screenshots exported for the project.
- `docs/final/` contains the final report PDF and final presentation PDF.
- `requirements.txt` lists the Python dependencies needed for the ETL script.

## Folder Structure

```text
dream-homes-nyc/
  README.md
  requirements.txt
  sql/
    schema/
    analysis/
  scripts/
    etl/
    validation/
  data/
    raw/
    sample/
    metadata/
  dashboards/
    screenshots/
    notes/
  docs/
    erd/
    final/
    references/
```

## Dataset Notes

- The dataset is synthetic and follows the final listing-centered ownership schema.
- The full dataset currently includes 16 CSV tables and 13,080 total rows.
- `data/metadata/row_count_summary.md` summarizes table volumes.
- `data/metadata/load_order_and_dataset_notes.md` records the recommended load order and naming notes.

## Quick Review Guide

- Start with the [ERD](docs/erd/dreamhomes_nyc_erd.pdf) and canonical [PostgreSQL schema](sql/schema/dreamhomes_postgres_schema.sql) for the relational design.
- Review [the ETL loader](scripts/etl/load_dreamhomes_data.py) together with [the documented load order](data/metadata/load_order_and_dataset_notes.md) for the data pipeline.
- See [the analytical SQL](sql/analysis/dreamhomes_analytical_queries.sql) and [dashboard summary](dashboards/notes/dashboard_summary.md) for the reporting layer.

## Running the ETL Loader

Install the Python dependencies from the repository root:

```bash
python -m pip install -r requirements.txt
```

Before running the loader, replace only the placeholder values in `CONNECTION_URL` near the top of `scripts/etl/load_dreamhomes_data.py` with the connection details for an existing PostgreSQL database. Do not commit real credentials. Then run:

```bash
python scripts/etl/load_dreamhomes_data.py
```

> **Caution:** The loader drops and recreates the project tables before loading the files in `data/raw/` in dependency order. Use a disposable or project-specific database.

Use the standalone schema in `sql/schema/dreamhomes_postgres_schema.sql` as the canonical schema reference.

## Additional Notes

- Analytical queries are grouped in `sql/analysis/dreamhomes_analytical_queries.sql`.
- Dashboard screenshots are stored in `dashboards/screenshots/`.
- Final course deliverables are stored in `docs/final/`.
