### Diffusion-weighted Sequence - Quantitative Validation 

This repo contains scripts for loading DICOM images of a diffusion-weighted (DWI) MRI sequence and comparing quantitative Apparent Diffusion Coefficient (ADC) maps to a benchmark sequence. Benchmarking is performed in the [NIST diffusion phantom](https://www.nist.gov/programs-projects/quantitative-mri).

Please see the "EXAMPLE" scripts for detailed walk-through of pre-processing and analysis workflows. 

# Pre-processing 
1. Load DICOMS - may be single- or multi-echo, 2D or 3D, radial or cartesian, multiple b-values
2. Use point-and-click interface to select phantom vials and create ROIs for quantitative analysis.
3. Perform rigid intensity-based registration to register phantom to benchmark images.

# Quantitative Validation 
1. Select a subset of DWI images to compare to the benchmark based on imaging parameters such as pulse prep, TR, acquisition date, and phantom orientation.
2. Calculate ADC of all voxels in vial ROIs and their summary statistics in all subset images and benchmark image. Choose parameters such as how many and which b-values to include in the ADC fit. 
3. Compare subset images to the benchmark with Box-and-Whisker plots, Pearson's correlation plots, and root-mean-square-error.
