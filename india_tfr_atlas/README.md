# India TFR Atlas 1971-2025

Reproducible Python publication pipeline for a print-ready A4 portrait PDF titled India Total Fertility Rate (TFR) Atlas 1971-2025.

Build status: source code and local artifacts were generated. The PDF is a 220-page publication scaffold because no official raw source files were present at build time. The project deliberately avoids fabricated observed data and marks missing outputs as placeholders.

Run:

```bash
pip install -r requirements.txt
python run_all.py
```

Add official source files under data/raw/ before rerunning:

- srs: Sample Registration System
- nfhs: National Family Health Survey
- census: Census of India
- world_bank: World Development Indicators
- un_wpp: UN World Population Prospects
- geo: state and union territory boundaries

Expected direct TFR CSV schema:

```csv
geography,level,residence,year,tfr,source,status
India,national,total,2021,2.0,SRS 2021,observed
```

Allowed data status values: observed, interpolated, model_forecast, placeholder.

Generated outputs include a final PDF, figure inventory, map inventory, table inventory, validation report, build report and data-lineage log.
