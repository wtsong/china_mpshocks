## High-Frequency Monetary Shocks for China

Updated on: December 2021

### Contents
1. **china_mpshocks.csv**:
  Data file containing the high-frequency monetary policy shocks for China (2006-2020) constructed in [Monetary Poicy Transmission and Policy Coordination in China](https://www.imf.org/-/media/Files/Publications/WP/2022/English/wpiea2022074-print-pdf.ashx) by Sonali Das and Wenting Song.

### Variable descriptions

- For details of shock construction, refer to the main text of the [paper](https://www.imf.org/-/media/Files/Publications/WP/2022/English/wpiea2022074-print-pdf.ashx). 

- The csv file contains the following variables:

  | Variable   | Description   | Type |
  | ---------- | ------------- | ---- |
  | date       | Shock date    | datetime |
  | shock_1y   | Monetary shocks constructed using 1-year IRS on the 7-day repo | float |
  | shock_5y   | Monetary shocks constructed using 5-year IRS on the 7-day repo | float |
  | isMain     | Indicator variable of the main measure of shocks | boolean |

### Examples
- The following Python code replicates Figure 2 in the paper:

  ```
  import pandas as pd
  import matplotlib.pyplot as plt

  df = pd.read_csv('china_mpshocks.csv')
  df['date'] = pd.to_datetime(df['date'])
  plt.plot(df['date'], df['shock_1y'], df['date'], df['shock_5y'])
  ```
