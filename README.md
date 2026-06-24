# Bangalore House Price Analysis — Outlier Removal with Normal Distribution & Z-Score

## Overview

This project analyzes property price data from Bangalore, India (`bhp.csv`) with a focus on cleaning the `price_per_sqft` column by identifying and removing outliers. Two statistical techniques are applied and compared: **percentile-based filtering** and **Z-score / standard deviation filtering**.

---

## Dataset

- **File:** `bhp.csv`
- **Source:** Bangalore house prices dataset
- **Key column analyzed:** `price_per_sqft`

---

## Steps Covered

1. **Percentile-based outlier removal** — Filter out values below the 0.1th percentile and above the 99.9th percentile to get a cleaner baseline DataFrame.

2. **Standard deviation filtering (4σ)** — On the percentile-filtered data, remove any remaining outliers that fall more than 4 standard deviations from the mean.

3. **Z-score filtering (threshold = 4)** — Apply Z-score method to the percentile-filtered data as an alternative approach. Produces the same result as step 2, confirming consistency between the two methods.

---

## Key Concepts

- **Normal Distribution** — The assumption that `price_per_sqft` follows a roughly bell-shaped distribution after cleaning.
- **Percentile technique** — A non-parametric way to cap extreme values at the tails of the distribution.
- **Standard deviation rule** — Values beyond ±4σ from the mean are treated as outliers.
- **Z-score** — A standardized measure of how many standard deviations a value is from the mean. Mathematically equivalent to the standard deviation approach.

---

## Technologies Used

- Python 3
- Pandas
- NumPy
- Google Colab

---

## How to Run

1. Clone this repository
2. Upload `bhp.csv` to your Colab environment or place it in the project directory
3. Open and run the notebook step by step

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
```

---

## Results

After applying outlier removal, the `price_per_sqft` distribution closely follows a normal curve, confirming the effectiveness of both techniques. The percentile and Z-score methods yield identical results when using a threshold of 4.


## Setup & Installation

1. Clone the repository
```bash
   git clone https://github.com/Emeka024/bangalore-house-prices.git
   cd bangalore-house-prices
```

2. Create and activate a virtual environment
```bash
   python3 -m venv .venv
   source .venv/bin/activate
```

3. Install dependencies
```bash
   pip install pandas numpy matplotlib scipy
```

4. Open the notebook
```bash
   code notebooks/bangalorehouseprices.ipynb
```