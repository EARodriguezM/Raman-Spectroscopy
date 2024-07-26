# RAMAN Data Analysis Tool

This Python script is designed to analyze RAMAN spectroscopy data. It processes raw data files, splits them into header and data sections, performs peak detection, and fits multiple Lorentzian models to the detected peaks.

<a href="https://github.com/EARodriguezM/Raman-Spectroscopy/stargazers"><img src="https://img.shields.io/github/stars/EARodriguezM/Raman-Spectroscopy" alt="Stars Badge"/></a> 
<a href="https://github.com/EARodriguezM/Raman-Spectroscopy/network/members"><img src="https://img.shields.io/github/forks/EARodriguezM/Raman-Spectroscopy" alt="Forks Badge"/></a>
<a href="https://github.com/EARodriguezM/Raman-Spectroscopy/pulls"><img src="https://img.shields.io/github/issues-pr/EARodriguezM/Raman-Spectroscopy" alt="Pull Requests Badge"/></a>
<a href="https://github.com/EARodriguezM/Raman-Spectroscopy/issues"><img src="https://img.shields.io/github/issues/EARodriguezM/Raman-Spectroscopy" alt="Issues Badge"/></a>
<a href="https://github.com/EARodriguezM/Raman-Spectroscopy/graphs/contributors"><img alt="GitHub contributors" src="https://img.shields.io/github/contributors/EARodriguezM/Raman-Spectroscopy?color=2b9348"></a>
<a href="https://github.com/EARodriguezM/Raman-Spectroscopy/blob/main/LICENSE"><img src="https://img.shields.io/github/license/EARodriguezM/Raman-Spectroscopy?color=2b9348" alt="License Badge"/></a> 

<!-- <a href="https://github.com/EARodriguezM/Raman-Spectroscopy/blob/main/esREADME.md"><img src="https://img.shields.io/static/v1?label=&labelColor=505050&message=Spanish README &color=%230076D6&style=flat&logo=google-chrome&logoColor=green" alt="website"/></a> -->

<i>Loved the project? Please consider giving a Star ⭐️ to help it improve!</i>

## Features

- Automatic encoding detection for input files
- Splitting of input files into header and data sections
- Data visualization of raw RAMAN spectra
- Peak detection
- Multiple Lorentzian peak fitting
- Generation of fitted spectra plots
- Extraction and reporting of fitted peak parameters

## Requirements

- Python 3.x
- Required Python packages:
  - csv
  - chardet
  - matplotlib
  - numpy
  - lmfit
  - scipy

## Usage

1. Place your RAMAN data files in a folder named 'Data' in the same directory as the script.
2. Run the script. It will process all files in the 'Data' folder.
3. Results will be saved in a 'Results' folder, with subfolders for each processed file.

## Output

For each processed file, the script generates:

- A header file with the equipment parameters(header.txt)
- A CSV file with the raw data (data.csv)
- A plot of the raw spectrum (.png and .svg formats)
- A plot of the fitted spectrum with individual peak components (.png and .svg formats)
- A text file with detailed fit results (results_fitted.txt)
- A text file with summarized peak information (results_peaks_info.txt)

## Functions

- `files_path_searcher`: Finds all files in the specified folder
- `path_helper`: Generates necessary file paths for output
- `detect_encoding`: Automatically detects the encoding of input files
- `split_file`: Splits the input file into header and data sections
- `read_data`: Reads the data and generates a raw spectrum plot
- `lorentzian`: Defines the Lorentzian function for peak fitting
- `analyze_data`: Performs peak detection, fitting, and generates result plots and files
