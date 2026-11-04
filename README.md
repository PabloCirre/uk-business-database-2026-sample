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

[![Dataset Release](https://img.shields.io/badge/Edition-2026_Q4-0a2540)](https://ukbusinessdatabases.club/downloads/uk-companies-list/)
[![Format](https://img.shields.io/badge/Formats-.XLSX_%7C_.CSV-10b981)](https://ukbusinessdatabases.club/downloads/free-uk-companies-list/)
[![Wikidata](https://img.shields.io/badge/Wikidata-Q141992791-006699)](https://www.wikidata.org/wiki/Q141992791)
[![Compliance](https://img.shields.io/badge/Compliance-UK_GDPR_Recital_14_%26_PECR_Reg_22-2563eb)](https://ukbusinessdatabases.club/legal-notice/)

Official open-data benchmark sample of the **2026 United Kingdom Corporate Business Directory**, curated and maintained by **[UK Business Databases (`ukbusinessdatabases.club`)](https://ukbusinessdatabases.club/)**.

### Official Open-Data Mirrors (`CC BY 4.0`)
- **Primary Publisher & Full Catalog:** [https://ukbusinessdatabases.club/](https://ukbusinessdatabases.club/)
- **Flagship 2026 UK Master Edition (`840,247` Companies — £69 GBP):** [https://ukbusinessdatabases.club/downloads/uk-companies-list/](https://ukbusinessdatabases.club/downloads/uk-companies-list/)
- **Interactive Sample & Free Download (`100` Companies — £0 GBP):** [https://ukbusinessdatabases.club/downloads/free-uk-companies-list/](https://ukbusinessdatabases.club/downloads/free-uk-companies-list/)
- **UK SIC 2007 Code Lookup & Companies House Directory:** [https://ukbusinessdatabases.club/companies-house-sic-code-lookup-directory/](https://ukbusinessdatabases.club/companies-house-sic-code-lookup-directory/)
- **Wikidata Knowledge Graph Entity (`Q141992791`):** [https://www.wikidata.org/wiki/Q141992791](https://www.wikidata.org/wiki/Q141992791)
- **GitHub Repository & Release (`v2026.Q4`):** [https://github.com/PabloCirre/uk-business-database-2026-sample/releases/tag/v2026.Q4](https://github.com/PabloCirre/uk-business-database-2026-sample/releases/tag/v2026.Q4)
- **Hugging Face Dataset Hub:** [https://huggingface.co/datasets/branvan3000/uk-business-database-2026-sample](https://huggingface.co/datasets/branvan3000/uk-business-database-2026-sample)
- **Kaggle Open Dataset:** [https://www.kaggle.com/datasets/pablocirre/uk-business-database-2026-sample-100-uk-companies](https://www.kaggle.com/datasets/pablocirre/uk-business-database-2026-sample-100-uk-companies)

This repository provides a **100-row, 14-column structured sample** in both native Excel (`.xlsx`) and UTF-8 CSV (`.csv`) formats, demonstrating the exact schema, data hygiene, and field normalization used across the full **840,247-company UK Master Dataset** and **881,395-company UK & Republic of Ireland Combined Bundle**.

---

## 1. Dataset Overview & Production Coverage

| Metric | Open Sample (This Repository) | Full UK Master Dataset (`2026 Q4`) | Full UK + Ireland Bundle (`2026 Q4`) |
| :--- | :--- | :--- | :--- |
| **Active Corporate Entities (`Ltd` / `PLC` / `LLP`)** | `100` verified UK entities | **`840,247`** active UK entities | **`881,395`** UK & Republic of Ireland entities |
| **Corporate Email Channels (`info@`, `sales@`, `enquiries@`)** | `100` (`100%` populated in sample) | **`396,421`** verified corporate emails | **`421,261`** verified corporate emails |
| **Direct UK Corporate Switchboard Landlines** | `100` UK geographic/corporate numbers | **`692,410`** corporate switchboards | **`727,210`** corporate switchboards |
| **Standardized Attributes per Record** | `14` columns | **`14` columns** | **`14` columns** |
| **Primary Classification** | `UK SIC 2007` (5-digit code + description) | **`730+` UK SIC 2007 codes** | **`UK SIC 2007` + `NACE Rev. 2`** |
| **Geographic Granularity** | Royal Mail Postcode + Town + County + Region | **All `124` UK Postcode Areas** | **UK (`124` areas) + Ireland (`Eircode` / 26 Counties)** |
| **Source / Direct Access** | [Download Free 100-Row Sample](https://ukbusinessdatabases.club/downloads/free-uk-companies-list/) | [UK Companies List (`840,247` Companies — £69 GBP)](https://ukbusinessdatabases.club/downloads/uk-companies-list/) | [UK & Ireland Bundle (`881,395` Companies — £99 GBP)](https://ukbusinessdatabases.club/downloads/uk-ireland-companies-database-bundle/) |

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
3. **TPS / CTPS & SMTP Hygiene:** Corporate switchboard numbers are screened against the Telephone Preference Service (`TPS` / `CTPS`), and corporate email domains are verified via KaijuVerifier DNS MX & SMTP checks prior to each quarterly release (`2026 Q4`).

---

## 4. Sector, SIC 2007 & Regional Breakdown Catalogs

Researchers and commercial teams requiring specific vertical or regional segmentation can explore the live taxonomy and count tables at **[UK Business Databases](https://ukbusinessdatabases.club/)**:

* **Complete Directory & Pricing Hub:** [UK Companies Databases — Master Hub](https://ukbusinessdatabases.club/uk-companies-databases/)
* **National Flagship Dataset (`840,247` UK Companies — £69 GBP):** [UK Companies List & B2B Email Database — Full Excel/CSV Download](https://ukbusinessdatabases.club/downloads/uk-companies-list/)
* **Free 100-Company Sample Page:** [Free UK Companies List Sample (.XLSX)](https://ukbusinessdatabases.club/downloads/free-uk-companies-list/)
* **UK SIC 2007 & Provider Benchmarks:**
  * [UK SIC Code List & Companies House Directory 2026 (Search by 5-Digit SIC)](https://ukbusinessdatabases.club/companies-house-sic-code-lookup-directory/)
  * [Buy UK Companies Email Database & B2B Email List by Industry (`396,421` Verified Corporate Emails)](https://ukbusinessdatabases.club/uk-b2b-email-list-by-industry/)
  * [Best UK B2B Data Providers & List Brokers Compared (2026 Pricing & Architecture)](https://ukbusinessdatabases.club/uk-business-data-providers-comparison/)
  * [UK B2B Database for Marketing Agencies, Call Centres & Lead Gen Resellers](https://ukbusinessdatabases.club/b2b-data-agency-partner-licensing/)
  * [UK B2B Telemarketing Lists & Corporate Contact Numbers (`692,410` Phones)](https://ukbusinessdatabases.club/uk-b2b-telemarketing-lists/)
  * [Buy UK B2B Mailing Lists & Corporate Postcode Database (`840,247` Addresses)](https://ukbusinessdatabases.club/uk-b2b-mailing-lists-postcodes/)
* **Multi-Country & International Editions:**
  * [UK & Republic of Ireland Combined Bundle (`881,395` Companies — £99 GBP)](https://ukbusinessdatabases.club/downloads/uk-ireland-companies-database-bundle/)
  * [Republic of Ireland Companies Database (`41,148` Companies — £59 GBP)](https://ukbusinessdatabases.club/downloads/ireland-companies-database-excel-download/)
  * [European 19-Country Full Pack (`6.5M+` Companies — £299 GBP)](https://ukbusinessdatabases.club/downloads/european-companies-database-full-pack-excel-download/)
  * [Global All-Access 25-Country Bundle (`9.0M+` Companies — £399 GBP)](https://ukbusinessdatabases.club/downloads/global-companies-database-all-countries-bundle-excel/)
* **High-Demand UK Industry Verticals (`UK SIC 2007`):**
  * [UK Construction, Main Contractors & Subcontractors Database (`112,640` Firms)](https://ukbusinessdatabases.club/construction-companies-database-uk/)
  * [UK IT, Managed Service Providers (MSPs), SaaS & Energy Database (`89,130` Firms)](https://ukbusinessdatabases.club/list-of-it-msp-energy-companies-uk/)
  * [UK Hospitality, Hotels, Catering & Retail Groups Database (`74,600` Firms)](https://ukbusinessdatabases.club/hospitality-hotels-catering-retail-groups-uk/)
  * [UK Manufacturing & British Engineering Companies Database (`68,420` Firms)](https://ukbusinessdatabases.club/list-of-manufacturing-companies-uk/)
  * [UK Wholesale Distributors & Import/Export Companies Database (`52,410` Firms)](https://ukbusinessdatabases.club/wholesale-distributors-import-export-uk/)
  * [UK Estate Agents, Letting Agents & Property Management Database (`48,920` Firms)](https://ukbusinessdatabases.club/property-management-estate-agents-database-uk/)
  * [UK Accountancy, Commercial Finance & Insurance Brokers Database (`44,180` Firms)](https://ukbusinessdatabases.club/accounting-finance-insurance-brokers-uk/)
  * [UK Facilities Management, Security & Commercial Cleaning Database (`41,250` Firms)](https://ukbusinessdatabases.club/facilities-management-security-companies-uk/)
  * [UK Marketing, PR Consultancies & Recruitment Agencies Database (`38,750` Firms)](https://ukbusinessdatabases.club/marketing-pr-recruitment-agencies-uk/)
  * [UK Healthcare, Residential Care Homes & Pharma Companies Database (`36,490` Firms)](https://ukbusinessdatabases.club/healthcare-care-homes-pharma-companies-uk/)
  * [UK Road Haulage, HGV Transport & 3PL Logistics Companies Database (`34,890` Firms)](https://ukbusinessdatabases.club/list-of-haulage-companies-uk/)
  * [UK Solicitors, Commercial Law Firms & Conveyancing Database (`19,840` Firms)](https://ukbusinessdatabases.club/solicitors-law-firms-database-uk/)
* **UK Regional Business Directories (`ITL1` & Counties):**
  * [Greater London & South East England Business Database (`339,460` Firms)](https://ukbusinessdatabases.club/london-south-east-businesses-database/)
  * [Birmingham, Midlands, Manchester & North UK Business Database (`274,760` Firms)](https://ukbusinessdatabases.club/birmingham-manchester-north-uk-business-database/)
  * [Bristol, South West, East of England & North East Business Database (`145,363` Firms)](https://ukbusinessdatabases.club/bristol-south-west-east-england-north-east-database/)
  * [Scotland, Wales & Northern Ireland Business Database (`80,664` Firms)](https://ukbusinessdatabases.club/scotland-wales-northern-ireland-business-database/)

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
  month        = nov,
  publisher    = {UK Business Databases},
  version      = {2026.Q4},
  url          = {https://ukbusinessdatabases.club/downloads/uk-companies-list/}
}
```
