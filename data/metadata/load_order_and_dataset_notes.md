# Load Order And Dataset Notes

This dataset follows the final listing-centered ownership design used in the Dream Homes NYC schema.

## Recommended PostgreSQL Load Order

1. `office`
2. `employee`
3. `agent`
4. `client`
5. `client_preference`
6. `neighborhood`
7. `school`
8. `property`
9. `listing`
10. `listing_ownership`
11. `client_inquiry`
12. `appointment`
13. `open_house`
14. `open_house_attendance`
15. `transactions`
16. `transaction_client_role`

## Notes

- `listing_ownership` uses `(listing_id, client_id)` as its composite primary key.
- `transaction_client_role` uses `(transaction_id, client_id)` as its composite primary key.
- Each listing can map to zero or one transaction in the final schema.
- The dataset includes 850 properties and 1,000 listings, so some properties appear in more than one listing cycle.
- The original workspace also contains a duplicate folder named `DreamHomes_Full_Synthetic_Dataset/`. The curated repo keeps `data/raw/` as the canonical dataset location.
