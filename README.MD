# VepiSET to EDF Converter

## Overview

This repository provides a tool to convert the VepiSET dataset from MATLAB (.mat) files to the European Data Format (EDF). The VepiSET dataset contains electrophysiological data, and converting it to EDF allows for easier analysis with various tools that support this format.

## Requirements

To use this tool, you need the following Python libraries:

- [numpy](https://numpy.org/): For numerical computations.
- [mne](https://mne.tools/): For processing electrophysiological data.
- [edfio](https://edfio.readthedocs.io/): For reading and writing EDF files.

You can install these libraries using pip:
```python
pip install numpy mne edfio
```
# Installation

1. **Clone the repository**:
2. **Navigate to the repository directory**:
3. **Install the required libraries** as mentioned above.

## Usage

1. **Set the `base_path`**:
- Open the `02.ipynb` notebook and set the `base_path` variable to the directory containing the VepiSET dataset’s `MAT-Files` folder.

2. **Set the `output_path`**:
- Set the `output_path` variable to the directory where you want to save the converted EDF files.

3. **Run the notebook**:
- To run the `02.ipynb` Jupyter notebook, you need Jupyter installed. If you don’t have it, install it with:`pip install jupyter`

- Then, start Jupyter Notebook:`jupyter notebook`
- Open `02.ipynb` and run all cells to perform the conversion.

## Verification

After running the notebook, check the `output_path` directory for the converted EDF files. To verify them, you can use MNE like this:

```python
import mne

edf_file = mne.io.read_raw_edf('path/to/your/file.edf')
print(edf_file.info)





