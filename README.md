<img width="785" alt="GUI image" src="https://github.com/user-attachments/assets/8cbc8421-947c-4b4b-988e-aaeb0d90a8bc" /># SQC-Tool
Signal Quality Control (SQC) GUI built from scratch for time-series data inspection and cleaning. 
Initially created remotely and version control done via BitBucket. Transfer to Github done on 01/06/2025
Features 6 tabs: File Check &amp; View, File Summary, File Re-ordering, Data Analysis, Visualisation Tool, and Generate Report.

# Purpose

This tool addresses the challenge of manually assessing and cleaning signal data at scale. It enables users to interactively visualize, inspect, and categorize faulty files before processing, making it easier to maintain clean and consistent datasets for downstream analysis or machine learning workflows.

# Main Features

The tool is organized into six interactive tabs:

## 1. File Check & View
- Detects and flags empty or corrupted files.
- Identifies inconsistent MAC addresses across data.
- Enables file-by-file inspection before processing.
<img width="861" alt="Screenshot 2025-06-02 at 10 22 13" src="https://github.com/user-attachments/assets/7424050a-cba3-469e-b651-9c2589258585" />

## 2. File Summary
-Displays metadata statistics about the dataset, such as:
  - Number of files per participant
  - Reach directions
  - Dominant legs
  - Baseline vs. follow-up distributions
- Outputs a summarized table of key counts and classifications.
  
<img width="932" alt="Screenshot 2025-06-02 at 10 23 53" src="https://github.com/user-attachments/assets/d47a2877-c178-4af1-ac62-02bc9802e844" />

## 3. File Re-ordering
- Renames or reorders filenames for consistent time-series sorting.
- Helps maintain chronological ordering of repeated trials or sessions.

## 4. Data Analysis
- Computes and visualizes distribution curves and box plots for metrics like:
  - Jerk Magnitude RMS
  - Gyro Magnitude RMS
  - Sample Entropy (SampEn)
- Flags statistical outliers automatically using IQR logic.
  
<img width="946" alt="Screenshot 2025-06-02 at 10 24 32" src="https://github.com/user-attachments/assets/0ca7a8ef-2179-495b-aa50-5d4d7b1fc9ac" />

## 5. Visualisation Tool
- Interactive plotting interface to toggle through each trial.
- Enables manual flagging of signal issues such as:
  - Noisy
  - Inverted
  - Incomplete
  - Discard
- Plots both `Gyro_Magnitude` and `Accel_X` for better comparative insight.
<img width="785" alt="GUI image" src="https://github.com/user-attachments/assets/a2c71aad-97c0-4fd5-a89f-bbce4822b9e3" />

## 6. Generate Report
- Exports flagged files and summary statistics to CSV.
- Prepares cleaned data pipeline-ready output for further processing.


### Prerequisites
- Python 3.8+
- Libraries: `pandas`, `matplotlib`, `tkinter`, `seaborn`, `os`, `glob`


