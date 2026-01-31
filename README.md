# Will the Customer Accept the Coupon?

## Project Overview

This project analyzes factors that influence whether drivers accept coupons delivered to their cell phones while driving. The goal is to distinguish between customers who accepted a driving coupon versus those who did not, using exploratory data analysis and visualization techniques.

## Data Description

The data comes from the UCI Machine Learning Repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including destination, current time, weather, passenger, etc., and asks whether the driver will accept the coupon.

- **Y = 1**: Driver accepted the coupon
- **Y = 0**: Driver rejected the coupon

### Coupon Types
- Restaurant (< $20)
- Coffee House
- Carry out & Take away
- Bar
- Restaurant ($20 - $50)

### Features
The dataset includes:
- **User attributes**: gender, age, marital status, children, education, occupation, income
- **Contextual attributes**: destination, weather, temperature, time, passenger
- **Coupon attributes**: type, expiration time
- **Behavioral attributes**: frequency of visiting bars, coffee houses, restaurants, etc.

## Key Findings

### Overall Acceptance Rate
- **56.84%** of all coupons were accepted

### Bar Coupon Analysis
- Drivers who visit bars **more than 3 times/month** have a **76.86%** acceptance rate vs **37.42%** for those who visit 3 or fewer times
- Drivers who visit bars **more than once/month AND are over 25** have a **69.73%** acceptance rate
- Drivers who visit bars **more than once/month, have no kids as passengers, and don't work in farming** have a **71.09%** acceptance rate

### Coffee House Coupon Analysis
- Frequent coffee house visitors show higher acceptance rates
- Morning hours (7AM-10AM) show higher acceptance rates
- Younger drivers (under 30) tend to accept more coffee house coupons

## Hypothesis

Drivers who accept coupons are more likely to:
1. Be frequent visitors of the coupon's venue type
2. Have passengers that align with the venue (e.g., no kids for bar coupons)
3. Have no urgent destination
4. Receive coupons at appropriate times (e.g., morning for coffee)

**Key Takeaway**: Existing behavior patterns are the strongest predictor of coupon acceptance.

## Files

| File | Description |
|------|-------------|
| `coupons.csv` | Raw dataset |
| `coupon_analysis.ipynb` | Jupyter notebook with analysis |
| `README.md` | Project documentation |

## Tools Used

- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn

## How to Run

1. Clone this repository
2. Ensure you have the required libraries installed:
   ```
   pip install pandas numpy matplotlib seaborn
   ```
3. Open `coupon_analysis.ipynb` in Jupyter Notebook
4. Run all cells

## Data Source

[UCI Machine Learning Repository - In-Vehicle Coupon Recommendation](https://archive.ics.uci.edu/ml/datasets/in-vehicle+coupon+recommendation)

## Author

Data Science Student

## License

This project is for educational purposes.
