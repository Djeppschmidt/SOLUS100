# SOLUS100
This is an archived copy of the complete NRCS Soils of the US 100 m resolution soil data maps.

# Original Documentation:

This repository provides extended documentation, code, and updated links to access the Soil Landscapes of the United States (SOLUS) 100-meter soil property maps. It provides supporting materials for a peer reviewed paper (Nauman et al., Soil Science Society of America Journal, 1–20. https://doi.org/10.1002/saj2.20769) documenting the theory and novel application of hybridized legacy training datasets used to inform the machine learning models used to create the new soil property maps presented here. The SOLUS dataset includes 20 different soil properties (listed below) with most properties predicted for seven standard depths (0, 5, 15, 30, 60, 100, and 150 cm). Further details on these properties and all included files are available in the README.docx document. Also included is a git repository formatted as a hybrid R package that includes all code used to create the soil property maps.

All SOLUS100 mapping layers are available as cloud optimized geotiffs at: https://storage.googleapis.com/solus100pub/index.html

Metadata: https://storage.googleapis.com/solus100pub/SOLUS100_metadata_pub.html

List of files at this URL are listed at: https://storage.googleapis.com/solus100pub/Final_Layer_Table_20231215.csv

Note that many of the raster files are scaled by multipliers of 10, 100, or 1000 to store the values as integers to decrease file size. The ‘scalar’ field of the file list table (Final_Layer_Table_20231215.csv) files provide those values. The actual rasters must be divided by the scalars to get the actual units of the properties. To download files, simply concatenate the google API URL with a forward slash and the file name listed in the table into a browser (e.g. EC at 0 cm would be https://storage.googleapis.com/solus100pub/ec_15_cm_p.tif). To automate downloads, a loop in python, R or your language of choice that builds file download urls from the file list in the csv can be implemented. Alternatively, some GIS programs (e.g. QGIS) will let you visualize and interact with the files without downloading the files by entering the URL.

All raster environmental covariates used in mapping are available here: https://storage.googleapis.com/cov100m/index.html

Properties included in SOLUS100:

1. Bulk density (oven dry)
2. Calcium carbonate
3. Cation Exchange Capacity (pH 7)
4. Clay
5. Coarse sand
6. Electrical Conductivity (sat. paste)
7. Effective cation exchange capacity
8. Fine sand
9. Gypsum (in <20 mm fraction)
10. Medium sand
11. pH (1:1 method)
12. Rock content
13. Sand
14. Sodium adsorption ratio
15. Silt
16. Soil organic carbon
17. Very coarse sand
18. Very fine sand
19. Depth to bedrock
20. Depth to restriction
