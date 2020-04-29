# awards-claim-adjustments
A web scraper to post claims adjustment data.

## Prepare the Excel file
| Payer    | Program Billing Group | NEW Batch | Program                   | CLIENT ID | Diagnosis | Date      | Procedure   | OLD Amount | Units | NEW Amount | TCN             | AuthID | New Invoice |
|----------|-----------------------|-----------|---------------------------|-----------|-----------|-----------|-------------|------------|-------|------------|-----------------|--------|-------------|
| Medicaid | DDD                   | 000200    | DDD Adult Training Center | 100013100 | F79       | 6/10/2019 | T2021:HI:US | $58.32     | 24    | 60.96      | 201919654532901 | 286    |             |
| Medicaid | DDD                   | 000200    | DDD Adult Training Center | 100013100 | F79       | 6/10/2019 | A0090:HI:22 | $1.48      | 2     | 1.58       | 201919654533501 | 285    |             |

The NEW BATCH and NEW Amount columns must be calculated manually.  
- **NEW BATCH** must be an empty batch for each program billing group.  If the batch number starts with leading zeroes, format as text.
- **NEW Amount** is calculated using VLOOKUP of the procedure to the procedure in the rate.xlsx file. If there are any N/A's it is because either the procedure does not have an applicable rate increase (e.g. transportation) or the procedure in your database settings does not match exactly. (e.g. "T2021:HI:US (Effect. 7/1/19)" will not match to the rate.xlsx value of "T2021:HI:US")

Then,

`python urlscrape.py`

and enter your domain, username, and password.
