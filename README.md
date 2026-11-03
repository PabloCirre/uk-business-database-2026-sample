---
language:
- en
license: cc-by-4.0
pretty_name: UK Business Database 2026 — 100 Active UK Corporate Entities Sample (UK SIC 2007 & Royal Mail Postcodes)
size_categories:
- n<1K
task_categories:
- tabular-classification
- feature-extraction
tags:
- uk-companies
- companies-house
- uk-sic-2007
- b2b-dataset
- united-kingdom
- business-directory
- royal-mail-postcodes
---

# UK Business Database 2026 — Open Benchmark Sample (`100` Active UK `Ltd` / `PLC` / `LLP` Entities · `14` Columns)

[![Dataset Release](https://img.shields.io/badge/Edition-October_2026_Q4-0a2540)](https://ukbusinessdatabases.club/downloads/uk-companies-list/)
[![Format](https://img.shields.io/badge/Formats-.XLSX_%7C_.CSV-10b981)](https://ukbusinessdatabases.club/downloads/free-uk-companies-list/)
[![Compliance](https://img.shields.io/badge/Compliance-UK_GDPR_Recital_14_%26_PECR_Reg_22-2563eb)](https://ukbusinessdatabases.club/privacy-policy/)

Official open-data benchmark sample of the **2026 United Kingdom Corporate Business Directory**, curated and maintained by **[UK Business Databases (`ukbusinessdatabases.club`)](https://ukbusinessdatabases.club/)**.

This repository provides a **100-row, 14-column structured sample** in both native Excel (`.xlsx`) and UTF-8 CSV (`.csv`) formats, demonstrating the exact schema, data hygiene, and field normalization used across the full **235,899-company UK Master Dataset** and **360,000+ UK & Ireland Multi-Region Dataset**.

---

## 1. Dataset Overview & Production Coverage

| Metric | Open Sample (This Repository) | Full UK Master Dataset (`2026 Q4`) | Full UK + Ireland Bundle (`2026 Q4`) |
| :--- | :--- | :--- | :--- |
| **Active Corporate Entities (`Ltd` / `PLC` / `LLP`)** | `100` verified UK entities | **`235,899`** active UK entities | **`360,000+`** UK & Republic of Ireland entities |
| **Corporate Email Channels (`info@`, `sales@`, `enquiries@`)** | `100` (`100%` populated in sample) | **`112,410`** generic corporate emails | **`175,000+`** generic corporate emails |
| **TPS-Screened Switchboard Landlines** | `100` UK geographic/corporate numbers | **`218,540`** corporate switchboards | **`330,000+`** corporate switchboards |
| **Standardized Attributes per Record** | `14` columns | **`14` columns** | **`14` columns** |
| **Primary Classification** | `UK SIC 2007` (5-digit code + description) | **`730+` UK SIC 2007 codes** | **`UK SIC 2007` + `NACE Rev. 2`** |
| **Geographic Granularity** | Royal Mail Postcode + Town + County + Region | **All `124` UK Postcode Areas** | **UK (`124` areas) + Ireland (`Eircode` / Counties)** |
| **Source / Direct Access** | [Download Free 100-Row Sample](https://ukbusinessdatabases.club/downloads/free-uk-companies-list/) | [UK Companies List (`235,899` Companies)](https://ukbusinessdatabases.club/downloads/uk-companies-list/) | [UK & Ireland Bundle (`360,000+` Companies)](https://ukbusinessdatabases.club/downloads/united-kingdom-and-ireland-business-databases/) |

---

## 2. Schema & Field Dictionary (`14` Standardized Columns)

Every record in both `UK-Business-Database-2026-Sample-100.xlsx` and `UK-Business-Database-2026-Sample-100.csv` adheres to the following 14-column schema:

| # | Column Name | Data Type | Description & Normalization Standard | Example Value |
| :---: | :--- | :--- | :--- | :--- |
| `1` | `Company_Name` | `String` | Registered corporate entity name (`Ltd`, `PLC`, `LLP`) verified against UK Companies House | `Albion London Haulage Ltd` |
| `2` | `Companies_House_CRN` | `String (8 chars)` | 8-character Companies House Registration Number (`CRN`) with leading-zero preservation | `07104200` |
| `3` | `Legal_Entity_Type` | `String` | Corporate legal structure (`Private Limited (Ltd)`, `Public Limited (PLC)`, `LLP`) | `Private Limited (Ltd)` |
| `4` | `UK_SIC_2007_Code` | `String (5 digits)` | Official 5-digit `UK SIC 2007` industrial classification code | `49410` |
| `5` | `Industry_Sector_Description` | `String` | Human-readable B2B trade category mapped to `UK SIC 2007` | `Freight Transport by Road & Haulage` |
| `6` | `Street_Address` | `String` | Primary trading or registered street address | `14 Bishopsgate Commercial Centre` |
| `7` | `Town_City` | `String` | UK Post Town / City | `City of London` |
| `8` | `County_Region` | `String` | Ceremonial or administrative UK county / region | `Greater London` |
| `9` | `UK_Postcode` | `String` | Full Royal Mail postcode (outward + inward code) | `EC2N 2DB` |
| `10` | `Corporate_Email` | `String` | Generic corporate contact address (`info@`, `enquiries@`, `sales@`, `office@`, `contact@`) | `enquiries@albionlondonhaul.co.uk` |
| `11` | `Direct_UK_Telephone` | `String` | Corporate main switchboard telephone number (screened against TPS / CTPS) | `+44 20 7946 3100` |
| `12` | `Company_Website_URL` | `URL` | Active corporate domain (`https://...`) | `https://www.albionlondonhaul.co.uk` |
| `13` | `Employee_Size_Band` | `String` | Estimated employee headcount band | `10-49 Employees` |
| `14` | `Turnover_Band_GBP` | `String` | Estimated annual corporate turnover band in GBP (`£`) | `£1M - £5M GBP` |

---

## 3. UK GDPR Recital 14 & PECR Regulation 22 Compliance By Design

This dataset is engineered strictly for **corporate-to-corporate (B2B) research, CRM enrichment, territory planning, and market intelligence** under UK data protection standards:

1. **Exclusively Corporate Legal Entities (`Ltd`, `PLC`, `LLP`):** Pursuant to **UK GDPR Recital 14**, data protection rules governing personal data do not apply to information concerning legal persons and corporate undertakings (`Limited`, `PLC`, and `LLP` entities).
2. **Zero Personal or Nominal Identifiers:** Neither this open sample nor the full production datasets contain personal names, residential addresses, private mobile numbers, or individual `firstname.lastname@` mailboxes. Only non-personal corporate role channels (`info@`, `sales@`, `enquiries@`, `office@`) are included in accordance with **PECR Regulation 22** for corporate subscribers.
3. **TPS / CTPS & SMTP Hygiene:** Corporate switchboard numbers are screened against the Telephone Preference Service (`TPS` / `CTPS`), and corporate email domains are verified via DNS MX & SMTP status checks prior to each quarterly release (`October 2026 Q4`).

---

## 4. Sector & Regional Breakdown Catalogs

Researchers and commercial teams requiring specific vertical or regional segmentation can explore the live taxonomy and count tables at **[UK Business Databases](https://ukbusinessdatabases.club/)**:

* **Complete Directory & Pricing Hub:** [UK Companies Databases — Master Hub](https://ukbusinessdatabases.club/uk-companies-databases/)
* **National Flagship Dataset (`235,899` UK Companies):** [UK Companies List — Full Excel/CSV Download](https://ukbusinessdatabases.club/downloads/uk-companies-list/)
* **Free 100-Company Sample Page:** [Free UK Companies List Sample](https://ukbusinessdatabases.club/downloads/free-uk-companies-list/)
* **Multi-Country & International Editions:**
  * [United Kingdom & Ireland Business Databases (`360,000+` Companies)](https://ukbusinessdatabases.club/downloads/united-kingdom-and-ireland-business-databases/)
  * [European Business Database (`4.8M+` Companies across 30+ European Markets)](https://ukbusinessdatabases.club/downloads/european-business-databases/)
  * [International Global Business Database (`18M+` Companies Worldwide)](https://ukbusinessdatabases.club/downloads/international-business-database/)
* **High-Demand UK Industry Verticals (`UK SIC 2007`):**
  * [UK Manufacturing Companies Database (`SIC 10–33`)](https://ukbusinessdatabases.club/uk-manufacturing-companies-database/)
  * [UK Construction & Building Trades Database (`SIC 41–43`)](https://ukbusinessdatabases.club/uk-construction-companies-database/)
  * [UK Logistics, Transport & Freight Companies Database (`SIC 49–53`)](https://ukbusinessdatabases.club/uk-logistics-and-transport-companies-database/)
  * [UK IT, Software & SaaS Companies Database (`SIC 62–63`)](https://ukbusinessdatabases.club/uk-it-and-software-companies-database/)
  * [UK Financial & Accounting Firms Database (`SIC 64–66, 69.2`)](https://ukbusinessdatabases.club/uk-financial-and-accounting-firms-database/)
  * [UK Healthcare, Dental & Medical Clinics Database (`SIC 86`)](https://ukbusinessdatabases.club/uk-healthcare-and-medical-clinics-database/)
  * [UK Hospitality, Hotels & Restaurants Database (`SIC 55–56`)](https://ukbusinessdatabases.club/uk-hospitality-hotels-and-restaurants-database/)
  * [UK Real Estate & Letting Agencies Database (`SIC 68`)](https://ukbusinessdatabases.club/uk-real-estate-and-estate-agents-database/)

---

## 5. Quick Start (Python / Pandas & R)

```python
import pandas as pd

# Load the 100-row UK B2B sample directly from CSV or Excel
df = pd.read_csv("UK-Business-Database-2026-Sample-100.csv", dtype={"Companies_House_CRN": str, "UK_SIC_2007_Code": str})

print(f"Loaded {len(df)} active UK corporate records across {df['County_Region'].nunique()} UK counties/regions.")
print(df[["Company_Name", "Companies_House_CRN", "UK_SIC_2007_Code", "Town_City", "UK_Postcode", "Corporate_Email"]].head(10))
```

---

## 6. Citation & License

Released under **[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)**. When using this benchmark sample in academic, econometric, or commercial whitepapers, please cite:

```bibtex
@dataset{uk_business_databases_2026,
  author       = {{UK Business Databases Research Team}},
  title        = {{UK Business Database 2026: Structured Sample of 100 Active United Kingdom Corporate Entities (Ltd, PLC, LLP) with UK SIC 2007 & Royal Mail Postcodes}},
  year         = 2026,
  month        = oct,
  publisher    = {UK Business Databases},
  version      = {2026.Q4},
  url          = {https://ukbusinessdatabases.club/downloads/uk-companies-list/}
}
```
