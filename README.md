# awards-claim-adjustments
A web scraper to post claims adjustment data.

## Prepare the Excel file
| Payer    | Program Billing Group | NEW Batch | Program                   | CLIENT ID | Diagnosis | Date      | Procedure   | OLD Amount | Units | NEW Amount | TCN             | AuthID | New Invoice |
|----------|-----------------------|-----------|---------------------------|-----------|-----------|-----------|-------------|------------|-------|------------|-----------------|--------|-------------|
| Medicaid | DDD                   | 000200    | DDD Adult Training Center | 100013100 | F79       | 6/10/2019 | T2021:HI:US | $58.32     | 24    | 60.96      | 201919654532901 | 286    |             |
| Medicaid | DDD                   | 000200    | DDD Adult Training Center | 100013100 | F79       | 6/10/2019 | A0090:HI:22 | $1.48      | 2     | 1.58       | 201919654533501 | 285    |             |
1. `pip install requirements.txt`
