# India-Stocks-1171-1200-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1171 to 1200)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1171-1200-Historical-Data/
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

## 📦 Constituents (1171 to 1200)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1171 | `GOKEX` | Gokaldas Exports Limited | `GOKEX.NS` |
| 1172 | `GOKUL` | Gokul Refoils and Solvent Limited | `GOKUL.NS` |
| 1173 | `GOKULAGRO` | Gokul Agro Resources Limited | `GOKULAGRO.NS` |
| 1174 | `GOLDENTOBC` | Golden Tobacco Limited | `GOLDENTOBC.NS` |
| 1175 | `GOLDIAM` | Goldiam International Limited | `GOLDIAM.NS` |
| 1176 | `GOLDTECH` | AION-TECH SOLUTIONS LIMITED | `GOLDTECH.NS` |
| 1177 | `GOODLUCK` | Goodluck India Limited | `GOODLUCK.NS` |
| 1178 | `GOODYEAR` | Goodyear India Limited | `GOODYEAR.NS` |
| 1179 | `GOPAL` | Gopal Snacks Limited | `GOPAL.NS` |
| 1180 | `GOYALALUM` | Goyal Aluminiums Limited | `GOYALALUM.NS` |
| 1181 | `GPPL` | Gujarat Pipavav Port Limited | `GPPL.NS` |
| 1182 | `GPTHEALTH` | GPT Healthcare Limited | `GPTHEALTH.NS` |
| 1183 | `GPTINFRA` | GPT Infraprojects Limited | `GPTINFRA.NS` |
| 1184 | `GRADIENTE` | Gradiente Infotainment Limited | `GRADIENTE.NS` |
| 1185 | `GRANDOAK` | Grand Oak Canyons Distillery Limited | `GRANDOAK.NS` |
| 1186 | `GRAUWEIL` | Grauer & Weil India Limited | `GRAUWEIL.NS` |
| 1187 | `GRAVISSHO` | Graviss Hospitality Limited | `GRAVISSHO.NS` |
| 1188 | `GREAVESCOT` | Greaves Cotton Limited | `GREAVESCOT.NS` |
| 1189 | `GREENLAM` | Greenlam Industries Limited | `GREENLAM.NS` |
| 1190 | `GREENPANEL` | Greenpanel Industries Limited | `GREENPANEL.NS` |
| 1191 | `GREENPLY` | Greenply Industries Limited | `GREENPLY.NS` |
| 1192 | `GREENPOWER` | Orient Green Power Company Limited | `GREENPOWER.NS` |
| 1193 | `GRINDWELL` | Grindwell Norton Limited | `GRINDWELL.NS` |
| 1194 | `GRINFRA` | G R Infraprojects Limited | `GRINFRA.NS` |
| 1195 | `GRMOVER` | GRM Overseas Limited | `GRMOVER.NS` |
| 1196 | `GROBTEA` | The Grob Tea Company Limited | `GROBTEA.NS` |
| 1197 | `GRPLTD` | GRP Limited | `GRPLTD.NS` |
| 1198 | `GRWRHITECH` | Garware Hi-Tech Films Limited | `GRWRHITECH.NS` |
| 1199 | `GSFC` | Gujarat State Fertilizers & Chemicals Limited | `GSFC.NS` |
| 1200 | `GSLSU` | Global Surfaces Limited | `GSLSU.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream GOKEX 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1171-1200-Historical-Data/main/GOKEX/1m/2026/10/GOKEX_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
