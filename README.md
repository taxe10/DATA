The dataset is available as .RAR files in 2 parts each. Make sure to unzip the files before executing the codes.

1) Fresh THz data: Mouse5B_Fresh.mat
2) Block THz data: Mouse5B_Block.mat

Dataset description:

1) ScanData: matrix with dimensions <y,x,t> representing the data of the THz scan. y and x are the positions of the scan where a signal was received while t is the 1024-point time-domain signal received at that position. Generally our basic imaging consists of looking at the maximum of the ScanData along the t-axis to get a 2D image with dimensions <x,y>.
2) xrange: physical positions of the x-axis in the scan in millimeters.
3) yrange: physical positions of the y-axis in the scan in millimeters.
4) trange: time-domain axis of the reflected signal at each point in picoseconds in case you wish to plot individual time-domain signals.
5) matrix: matrix with dimensions <y,x> representing the ground truth obtained by morphing the pathology results. IMPORTANT: The data should be flipped vertically before being used (see line 28 in Amplitude_EM).
6) matrix_key_number: vector with dimension <k_total> with the key number representation of the k_total regions within the sample.
7) matrix_key_tissue: matrix with dimensions <k_original,c>, where c corresponds to the length of the string. Each row corresponds to the name that was given to each region and it follows the same order given in matrix_key_number, i.e., the matrix_key_number = 1 for matrix_key_tissue = CANCER.
