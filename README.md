# GMENoiseReduce

Python implementation of the Generalized Maximum Entropy white noise elimination technique discussed in https://pubs.aip.org/aip/jap/article/132/7/074903/2837401/Eliminating-white-noise-in-spectra-A-generalized

## Installation
	

 - **Requires Numpy, no other dependencies**

	`pip install GMENoiseReduce`

## Usage

    from GMENoiseReduce import GME
    x,y = data
    smoothed-yvals = GME.smooth(x,y)
  ![Test results on artificial data](![image](https://github.com/user-attachments/assets/eade4a72-af9a-4617-b920-1b91f15a5e45)
)
## Advanced Usage
The full function takes in additional arguments if the curve is not ideal 

    smoothed-yvals = GME.smooth(x,y, int order, int noise_threshold, int offset)

 Despite this method needing zero information about the original system,  the solutions provided are currently not always stable. 

 - **order :**  The order of the CME (Corrected Maximum Entropy) calculations, defaults to ***22***
 - **noise_threshold :** The white noise coefficient cut-off, defaults to ***10***
 - **offset :** The empirical offset to the R-matrix zero coefficient, defaults to ***2***
