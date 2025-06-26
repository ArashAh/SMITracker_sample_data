<!-- badges: start -->

[![Lifecycle: stable](https://img.shields.io/badge/lifecycle-stable-brightgreen.svg)](https://lifecycle.r-lib.org/articles/stages.html#stable)

<!-- badges: end -->
# SMITracker Sample Dataset Repository

This repository contains sample datasets for test-running the [SMITracker platform](https://github.com/ArashAh/SMITracker).

## Directory structure and content

The repository includes three main sub-directories:

- **`input_data/`:** This directory contains `.JSON` files generated during the signal localization process using Fiji.

- **`output_data/`:** This directory includes `.rds` files produced during data processing with the SMITracker application. The file names start with numbers 1-5, corresponding to the outputs of the first 5 tabs of the application. Additionally, there are three exemplary files named `plot.1.1.data` to `plot.1.3.data` representing the data behind plots in the *Scanning Speed* section of *Analysis Output* tab.

- **`visual_log/`:** This directory contains screenshots of different tabs of the SMITracker interface while processing data and generating output data. The files are named after their corresponding tab in the application interface. There are 12 versions for *Spatial Filtering* tab, representing screenshots related to spatial filtering of the 12 sample datasets. Also there are 6 versions for *Visual Inspection* tab; files ending with *odd* numbers are examples of normal interactions that can be approved, while files ending with *even* numbers represent examples of noise in the data that should be removed from the optimization dataset in *Visual Inspection* tab. In addition, there are 4 versions for *Noise Exclusion* tab; files ending with *odd* numbers shows the visualization of results in the presence of noise, and the files ending with *even* numbers visualizes the results in the absence of noise.

## How to Use

To use these datasets as samples for running SMITracker, follow these steps:

1. **Clone the Repository:**  
   Clone this repository to your local machine.
   ```sh
   git clone https://github.com/ArashAh/SMITracker_sample_data
   ```
2. **Run the Platform:**  
Run the SMITracker platform either as an R package or a Docker container, following the instructions provided by the [SMITracker platform](https://github.com/ArashAh/SMITracker).

3. **Input Data:**  
In the first tab of the application, set the path to the `input_data/` directory from the cloned repository and start the processing using the provided sample datasets. 

4. **Process Data:**  
Use the screenshots in the `visual_log/` directory as a guide for setting variables in the SMITracker interface. For detailed information on processing data, read the published paper [here](link to the published paper).

5. **Output Data:**  
Save the results of your analysis in the `output_data/` directory. File names will be labeled with the analysis ID you provide and the date of the analysis. Note that using the same analysis ID on the same date will overwrite previous outputs.
