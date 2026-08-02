The final dataset contains 13,080 total rows across 16 tables.

| Table | File | Row Count |
| --- | --- | ---: |
| agent | agent.csv | 72 |
| appointment | appointment.csv | 850 |
| client | client.csv | 1000 |
| client_inquiry | client_inquiry.csv | 2400 |
| client_preference | client_preference.csv | 650 |
| employee | employee.csv | 120 |
| listing | listing.csv | 1000 |
| listing_ownership | listing_ownership.csv | 1239 |
| neighborhood | neighborhood.csv | 24 |
| office | office.csv | 8 |
| open_house | open_house.csv | 320 |
| open_house_attendance | open_house_attendance.csv | 2100 |
| property | property.csv | 850 |
| school | school.csv | 72 |
| transaction_client_role | transaction_client_role.csv | 1675 |
| transactions | transactions.csv | 700 |

Verification note: the existing `outputs/tables/row_counts.csv` matches the row totals for all tables, but it uses the table name `transaction` while the actual dataset file is `transactions.csv`.
