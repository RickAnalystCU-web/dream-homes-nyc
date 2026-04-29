# Dream Homes NYC

Dream Homes NYC is a course project for a fictional New York City real estate agency. The repository packages a finalized PostgreSQL schema, synthetic relational data, ETL/loading code, analytical SQL procedures, and support materials used for reporting and dashboard work.

The project is organized to support both transactional database loading and business analysis. Core entities include offices, employees, agents, clients, properties, listings, inquiries, appointments, open houses, and completed transactions.

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

## SQL And Script Notes

- The schema file in `sql/schema/` should be treated as the source of truth.
- The ETL loader in `scripts/etl/` preserves the original project loading logic and uses the curated `data/raw/` folder.
- Analytical queries are grouped together in `sql/analysis/dreamhomes_analytical_queries.sql`.
- The ERD PDF is stored in `docs/erd/dreamhomes_nyc_erd.pdf`.
- Dashboard screenshots are stored in `dashboards/screenshots/`.
- Final deliverable PDFs are stored in `docs/final/`.

## Requirements

Install the Python dependencies with:

```bash
pip install -r requirements.txt
```

## Current Gaps

- A duplicate root-level ERD file is still present in the repo folder and can be reviewed manually later.
- If you want the editable presentation source in the repo, the `.pptx` file still needs to be added intentionally.
