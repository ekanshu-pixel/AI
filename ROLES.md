# Role-based access map
Fill this in first — it decides what each person's dashboard shows.
Each role gets its OWN Google Sheet and its OWN Drive folder. Share each folder only
with that role. Pull shared numbers across with IMPORTRANGE, never by copying raw data.

| Role      | Person(s) | Drive folder        | Sheet name              | Sees                                   |
|-----------|-----------|---------------------|-------------------------|----------------------------------------|
| Founders  | Rajneesh, Ekanshu | /MIRA/founders | Founders Dashboard   | Everything (summaries)                 |
| CFO       | [name]    | /MIRA/finance       | CFO Dashboard           | Cash, AR/AP, margins, bank balances    |
| Sales     | [name]    | /MIRA/sales         | Sales Dashboard         | Orders, pipeline, collections          |
| Plant     | [name]    | /MIRA/plant         | Plant Dashboard         | Production, downtime, stock, quality   |

Rollout rule (from the 1 Oct meeting): start with founders/senior management only.
Add other roles once you trust the data separation.
