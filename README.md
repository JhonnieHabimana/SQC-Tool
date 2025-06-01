# SQC-Tool
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

## 2. File Summary
-Displays metadata statistics about the dataset, such as:
  - Number of files per participant
  - Reach directions
  - Dominant legs
  - Baseline vs. follow-up distributions
- Outputs a summarized table of key counts and classifications.

## 3. File Re-ordering
- Renames or reorders filenames for consistent time-series sorting.
- Helps maintain chronological ordering of repeated trials or sessions.

## 4. Data Analysis
- Computes and visualizes distribution curves and box plots for metrics like:
  - Jerk Magnitude RMS
  - Gyro Magnitude RMS
  - Sample Entropy (SampEn)
- Flags statistical outliers automatically using IQR logic.

## 5. Visualisation Tool
- Interactive plotting interface to toggle through each trial.
- Enables manual flagging of signal issues such as:
  - Noisy
  - Inverted
  - Incomplete
  - Discard
- Plots both `Gyro_Magnitude` and `Accel_X` for better comparative insight.

## 6. Generate Report
- Exports flagged files and summary statistics to CSV.
- Prepares cleaned data pipeline-ready output for further processing.

## GUI Screenshot

Here's what the final GUI layout looks like:
<img width="785" alt="GUI image" src="https://github.com/user-attachments/assets/24e91253-22e8-476f-b88e-4c39bed31736" />

### Prerequisites
- Python 3.8+
- Libraries: `pandas`, `matplotlib`, `tkinter`, `seaborn`, `os`, `glob`


