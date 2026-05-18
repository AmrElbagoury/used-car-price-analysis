# Used Car Price Analysis
### Practical Application Assignment — UC Berkeley Professional Certificate in ML & AI

---

## Summary of Findings

This project analyzes a dataset of 135,566 used car listings to identify the
key factors that drive used car prices. The goal is to provide a used car
dealership with clear, data-driven recommendations for fine-tuning their
inventory strategy.

Using a **Ridge Regression model** trained on the cleaned dataset, we achieved
a test RMSE of **$5,824** against a median market price of **$15,590**.

### Key Findings

- **Age and Mileage are the strongest price drivers** — newer vehicles
  with lower mileage consistently command higher prices regardless of other
  factors.

- **Trucks and Pickups command the highest premiums** — trucks and pickups
  are priced up to 12% above comparable SUVs even when age and mileage are
  identical. Sedans carry an inherent 6% discount vs SUVs.

- **Diesel and Electric vehicles fetch premium prices** — diesel vehicles
  have a median price of $27,490 and electric vehicles $23,990, compared to
  $13,998 for gas vehicles.

- **4WD and RWD vehicles outperform FWD** — front-wheel drive vehicles
  carry a 16% price discount even when in comparable condition to 4WD vehicles.

- **Title status directly impacts value** — clean title vehicles sell for
  a median of $15,991 while salvage title vehicles fetch only $7,999 and
  missing title vehicles as low as $4,500.

- **Brand matters less than expected** — only Lexus, Porsche, and Tesla
  command meaningful price premiums. Age, mileage, type, and drive type are
  far more influential than manufacturer.

### Recommendations for the Dealership

- ✅ **Stock trucks, pickups, and SUVs** — they command the highest and most consistent prices
- ✅ **Prioritize newer vehicless** — age and mileage are the strongest price drivers
- ✅ **Seek out diesel and electric vehicles** — they fetch premium prices above comparable gas vehicles
- ✅ **Focus on 4WD and RWD vehicles** — FWD vehicles carry an inherent 16% price discount
- ✅ **Verify title status on every acquisition** — a salvage or missing title can cut a car's value in half
- ✅ **Do not overpay for brand** — condition, age, and type matter far more than the manufacturer badge

---

## Notebook

📓 [View the full analysis notebook here](prompt_II.ipynb)

The notebook covers the full CRISP-DM process:
1. Business Understanding
2. Data Understanding
3. Data Preparation
4. Modeling
5. Evaluation
6. Deployment

---

## Dataset

- **Source:** Kaggle — Used Car Listings
- **Original size:** ~3 million records
- **Working subset:** 426,880 records
- **After cleaning:** 135,566 records
- **File:** `data/vehicles.csv`

---

## Model Performance

| Metric | Value |
|--------|-------|
| Model | Ridge Regression (alpha=10) |
| CV MSE | 0.1145 |
| Validation MSE | 0.1154 |
| Test MSE | 0.1173 |
| Test RMSE | $5,824 |
| Median Price | $15,590 |
| RMSE as % of Median | 37.4% |

---

## Project Structure

```
used-car-price-analysis/
│
├── data/
│   └── vehicles.csv          # Raw dataset
│
├── prompt_II.ipynb           # Full analysis notebook
├── README.md                 # This file
└── LICENSE                   # MIT License
```

---

## Requirements

```
python >= 3.8
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
```

Install dependencies:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## Author

Developed as part of the UC Berkeley Professional Certificate in Machine Learning & AI
