# Patient Vitals Analytics

## Project Overview

This project analyzes patient vitals from a CSV dataset (`patient_vitals.csv`) and generates a summary report.
It calculates key statistics (mean, median, mode) and identifies outliers in Heart Rate and Temperature using the IQR method.

The project is organized in **three modules**:

* **Module 1: Data Loader** – Loads CSV data into a list of dictionaries with error handling.
* **Module 2: Analytics Engine** – Implements statistical functions manually:

  * `calculate_mean(values)`
  * `calculate_median(values)`
  * `calculate_mode(values)`
  * `calculate_outliers(values)` using IQR
* **Module 3: Reporting** – Generates a summary report and flags patients who are outliers in Heart Rate or Temperature.

---

## Workflow Diagram

```
+-----------------+       +---------------------+       +-----------------------+
|  Module 1:      |       |  Module 2:          |       |  Module 3:            |
|  Data Loader    | ----> |  Analytics Engine   | ----> |  Reporting & Outliers |
|  (load CSV)     |       |  (stats calculations)|      |  (summary & table)   |
+-----------------+       +---------------------+       +-----------------------+
```

* **Step 1:** Load patient data from CSV into a list of dictionaries.
* **Step 2:** Calculate statistics (mean, median, mode) and detect outliers using IQR.
* **Step 3:** Generate a summary report showing vitals stats and patient IDs flagged as outliers.

---

## Dataset

* **File:** `patient_vitals.csv`

* **Fields:**

  * `patient_id` (Integer) – Unique patient ID
  * `age` (Integer) – Patient age
  * `temperature` (Float) – Body temperature in °C
  * `heart_rate` (Integer) – Beats per minute
  * `systolic_bp` (Integer) – Systolic blood pressure
  * `oxygen_saturation` (Integer) – SpO₂ percentage

* **Source:** •	[Mendeley] Blood Pressure Data (Nigeria/Ogun State):https://data.mendeley.com/datasets/3xp4r3xsr5.

---

## How to Run

1. Make sure you have **Python 3.8+** installed.
2. Place `patient_vitals.csv` in the same folder as the scripts.
3. Run Jupyter notebook:



or, if using a Jupyter Notebook, run all cells sequentially.

4. The report will display:

   * Mean, median, and mode for Heart Rate and Temperature
   * List of patient IDs flagged as outliers with their values

**Example:**

```
=== Patient Vitals Summary Report ===

Heart Rate:
  Mean: 80.2
  Median: 78.5
  Mode: 72
  Outlier Count: 0

Temperature:
  Mean: 37.1
  Median: 36.9
  Mode: 36.6
  Outlier Count: 5

=== Outlier Patients (Heart Rate or Temperature) ===
Patient ID Heart Rate  Temp    HR Outlier  Temp Outlier
108        92          38.1   False       True
114        90          38.0   False       True
120        94          38.2   False       True
126        88          37.9   False       True
128        92          38.0   False       True
```

---

## Notes

* Outliers are calculated using the **IQR (Interquartile Range) method**.
* The `multiplier` can be adjusted in the report function to detect more or fewer outliers.
* All statistical calculations are implemented manually without using Pandas for learning purposes.

---

## Dependencies

* Python standard libraries only: `math`, `collections`
* No external packages are required.

---

## Author

* ZeenatOyetolu
* [oyetoluzeenat@gmail.com / https://github.com/Oyetoluzeenat]


