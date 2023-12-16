## High-Frequency Monetary Shocks for China

Updated on: December 2023

### Contents
1. **china_mpshocks.csv**
    - High-frequency monetary policy shocks for China constructed in [Monetary Poicy Transmission and Policy Coordination in China](https://www.sciencedirect.com/science/article/abs/pii/S1043951X23001177) by Sonali Das and Wenting Song, *China Economic Review*, Volume 82, December 2023, 102032.
    - Sample: 2006-2020

### Variable descriptions

- For details on shock construction, refer to the main text of the [paper](https://www.sciencedirect.com/science/article/abs/pii/S1043951X23001177).

- The csv file contains the following variables:

  | Variable   | Description                                                      | Type     |
  | ---------- | ---------------------------------------------------------------- | -------- |
  | `date`     | Date of monetary shocks                                          | datetime |
  | `datetime` | Time of monetary event announcements                             | dateimte |
  | `shock_1y` | Monetary shocks constructed using 1-year IRS on the 7-day repo   | float    |
  | `shock_5y` | Monetary shocks constructed using 5-year IRS on the 7-day repo   | float    |
  | `isMain`   | Indicator variable for the main measure of shocks **(baseline)** | boolean  |
  | `isBroad`  | Indicator variable for the broad measure of shocks               | boolean  |

- The file also provides details the type of monetary policy event that underlies a certain shock.
- For the main measure of monetary shocks, monetary policy events include changes to the PBC's main policy instruments:
  | Variable | Description                                                      | Type     |
  | -------- | ---------------------------------------------------------------- | -------- |
  | `isdRRR`   | The underlying monetary event is changes to the reserve requirement ratio (RRR) | boolean  |
  | `isdRevrepo` | The underlying monetary event is changes to PBC's 7-day reverse repor rate | boolean  |
  | `isdLDR` | The underlying monetary event is changes to benchmark deposit and lending rates | boolean  |
  | `isdMLF` | The underlying monetary event is changes to the rate on the PBC’s medium-term lending facility (MLF)  | boolean  |


- For the broad measure of monetary shocks, monetary policy events additionally include:
  | Variable | Description | Type |
  | -------- | ----------- | ---- |
  | `isMPR`    | The underlying monetary event is quarter releases of monetary policy reports   | boolean  |
  | `isFX`   | The underlying monetary event is foreign exhcange policy reforms  | boolean  |
  | `isTMLF` | The underlying monetary event is recent changes to the MLF  | boolean  |