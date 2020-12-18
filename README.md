# Spectrum Challange 2 Dataset and Frame Error Prediction Code
Deep Learning for Frame Error Prediction using a DARPA Spectrum Collaboration Challenge (SC2) Dataset.

# Dataset
The dataset is contained in two files - scrimmage4_link_dataset.pickle and scrimmage5_link_dataset.pickle (will be available soon)

The pickle files are stored as list of tuples, each list corresponding to a single link, and containing two elements. Length of each element equal to the number of frames in that link - it varies between link to link.
The first tuple contains the paramenters:
1. Signal to Noise Ratio ('snr') - 1 element
2. The Modulation and Coding Scheme ('mcs') - 1 element
3. The center frequency of the link ('centerFreq') - 1 element
4. The bandwidth of the link ('bandwidth') - 1 element
5. The Power Spectral Density ('psd') - 16 elements
Thus the total width of each element of the first tuple for a link is 20.

The second tuple contains the success of transmission ('rxSuccess'). If it is 1, there is no frame error, if it is 0, there is a frame error.

# Code
1. The code is provided into separate files, one for each scrimmage (Scrimmage-4.ipynb & Scrimmage-5.ipynb). Every file contains five different neural network architectures, with two separate approaches for creating the train-validation-test set. 
2. RFE.ipynb: Implement Feature Selection method.
3. Plots.ipynb: Plot figures.
Please refer to the paper for a detailed description.

