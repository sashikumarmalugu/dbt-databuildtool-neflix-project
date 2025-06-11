# dbt-databuildtool-neflix-project
A fully-managed, modular ELT pipeline that ingests raw Netflix data from CSV → Amazon S3 → Snowflake, then uses dbt to deliver clean, tested, analytics-ready tables that feed dashboards in Looker Studio, Power BI, and Tableau.
![image](https://github.com/user-attachments/assets/0ba07d8b-7340-43cf-a559-278e53b149cf)


# Why this project matters
End-to-end reference for building lakehouse-style analytics on Snowflake

dbt-driven transformations: version-controlled SQL, tests, and documentation

Layered warehouse model: Raw → Staging → Serving for rock-solid data contracts

Vendor-agnostic BI: the same serving layer powers multiple visualisation tools

Lightweight & reproducible: everything provisioned with IaC / simple CLI scripts

# Tech stack

| Stage             | Tooling & Services                             |
| ----------------- | ---------------------------------------------- |
| **Extract/Load**  | Python loader (or AWS Glue) → **Amazon S3**    |
| **Raw Layer**     | Snowflake `RAW` database                       |
| **Transform**     | **dbt** (Core/Cloud) for SQL modelling + tests |
| **Staging layer** | Snowflake `STG` database                       |
| **Serving layer** | Snowflake `DEV` / `PROD` database              |
| **Orchestration** | dbt Cloud jobs or GitHub Actions workflow      |
| **Visualization** | Looker Studio · Power BI · Tableau             |

