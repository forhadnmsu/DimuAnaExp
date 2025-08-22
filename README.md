## Goal
The goal of the DimuAnaExp module is to read input data from a ROOT file (in DST format) and convert it into the RUS (ROOT Universal Structure) format. In this version, I have added dimuon variables only to analyze the commissioning data.

``` Compilation before running the Fun4All macro locally or in the grid                                                      
cd DimuAnaExp
source setup.sh    
cmake-this    
make-this    
```    
### Uses                                                                                              
#Converting DST to RUS

Add your own DST file lists, and update the file name in `DimuAnaExp/Convert/gridsub.sh`:

Line 4: `LIST_VEC=list.txt` # File containing the list of recontructed DST files
Line 6: `JOB_NAME=pol_kmag_aug16_2025`

For the commissioning data, you can run it locally or on the grid, depending on the processing time.

```bash
   ./gridsub.sh -j 1-5 -g -o

    1. `-j 1-5`: Specifies the range of input DST files to process (from the 1st row to the 5th one).
    2. `-g`: Enables grid mode for processing.
    3. `-o`: Overwrites existing files.

