# VIC

This python program describes the use of the VIC method described at https://www.sciencedirect.com/science/article/abs/pii/S0950705118300091

To run the program the sklearn library is needed.

In this method a dataset is read and their classes are defined based by a split point. The splits points can be defined in line 187. Multiple classifiers can also be used an defined in line 85. The classifiers follow the structure of sklearn. If a new model is being integrated the BNHandler class can be used to follow this structure.

The VIC can be run with multiple threads. Depending on the threads the split datasets are organized. While implementing a tensorflow model this causes an error, due to the session handling. One workaround is to use the GPU devices as different threads and apply the different classifiers in the BNHandler class.

