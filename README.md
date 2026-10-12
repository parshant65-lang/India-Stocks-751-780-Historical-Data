# India-Stocks-751-780-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 751 to 780)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-751-780-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (751 to 780)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 751 | `BASML` | Bannari Amman Spinning Mills Limited | `BASML.NS` |
| 752 | `BATLIBOI` | Batliboi Limited | `BATLIBOI.NS` |
| 753 | `BAYERCROP` | Bayer Cropscience Limited | `BAYERCROP.NS` |
| 754 | `BBL` | Bharat Bijlee Limited | `BBL.NS` |
| 755 | `BBTC` | The Bombay Burmah Trading Corporation Limited | `BBTC.NS` |
| 756 | `BBTCL` | B&B Triplewall Containers Limited | `BBTCL.NS` |
| 757 | `BCG` | Brightcom Group Limited | `BCG.NS` |
| 758 | `BCLIND` | Bcl Industries Limited | `BCLIND.NS` |
| 759 | `BCONCEPTS` | Brand Concepts Limited | `BCONCEPTS.NS` |
| 760 | `BCPL` | BCPL Railway Infrastructure Limited | `BCPL.NS` |
| 761 | `BEARDSELL` | Beardsell Limited | `BEARDSELL.NS` |
| 762 | `BECTORFOOD` | Mrs. Bectors Food Specialities Limited | `BECTORFOOD.NS` |
| 763 | `BEDMUTHA` | Bedmutha Industries Limited | `BEDMUTHA.NS` |
| 764 | `BEEKAY` | Beekay Steel Industries Limited | `BEEKAY.NS` |
| 765 | `BELDING` | Belding India Limited | `BELDING.NS` |
| 766 | `BELLACASA` | Bella Casa Fashion & Retail Limited | `BELLACASA.NS` |
| 767 | `BENARAS` | Benares Hotels Limited | `BENARAS.NS` |
| 768 | `BENGALASM` | Bengal & Assam Company Limited | `BENGALASM.NS` |
| 769 | `BEPL` | Bhansali Engineering Polymers Limited | `BEPL.NS` |
| 770 | `BESTAGRO` | Best Agrolife Limited | `BESTAGRO.NS` |
| 771 | `BETA` | Beta Drugs Limited | `BETA.NS` |
| 772 | `BFINVEST` | BF Investment Limited | `BFINVEST.NS` |
| 773 | `BFUTILITIE` | BF Utilities Limited | `BFUTILITIE.NS` |
| 774 | `BGLOBAL` | Bharatiya Global Infomedia Limited | `BGLOBAL.NS` |
| 775 | `BGRENERGY` | BGR Energy Systems Limited | `BGRENERGY.NS` |
| 776 | `BHAGCHEM` | Bhagiradha Chemicals & Industries Limited | `BHAGCHEM.NS` |
| 777 | `BHAGERIA` | Bhageria Industries Limited | `BHAGERIA.NS` |
| 778 | `BHAGYANGR` | Bhagyanagar India Limited | `BHAGYANGR.NS` |
| 779 | `BHANDARI` | Bhandari Hosiery Exports Limited | `BHANDARI.NS` |
| 780 | `BHARATGEAR` | Bharat Gears Limited | `BHARATGEAR.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream BASML 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-751-780-Historical-Data/main/BASML/1m/2026/10/BASML_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
