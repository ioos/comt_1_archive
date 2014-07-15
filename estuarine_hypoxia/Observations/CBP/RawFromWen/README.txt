.
|-- 1original                          ---directory storing original data obtained from CBP
|                                         website: http://www.chesapeakebay.net/data_waterquality.aspx
|-- 2sepvar			       ---a directory storing program sepvar_trib.sh and sepvar_stem.sh
|                                         to separate the complex excel sheet txt file into separate 
|                                         parametrs. e.g. 2sepvar/trib_SALINITY_LE5.4_1990_2006.txt
|                                         ---------------------------------------------
|                                         year mm dd hh min depth-from-surface  salinity lat lon 
|                                         ---------------------------------------------
|                                         1990 01 17 08 40   1.0                15.1 36.95486 -76.39275
|                                         1990 01 17 08 40   3.0                16.8 36.95486 -76.39275
|                                         1990 01 17 08 40   5.0                18.2 36.95486 -76.39275
|                                         
|                                         similarly,sepvar_trib_DO_CHLA.sh and sepvar_stem_DO_CHLA.sh do
|                                         the same thing, but for dissolved oxygen(mg/L) and chlorophyll
|                                         (ug/L)
|                                             
|-- 4vertextrap                        ---a directory to store results produced by vertical_extrapolation.m
|                                         which generates vertically extraporlated (to 11 vertical levels)
|                                         unanimously so that it is easier to handle 
|-- graph                              ---directory to save pictures made by vertical_extrapolation.m
|-- README.txt                         ---this file
`-- vertical_extrapolation.m           ---program to do vertical extrapolation. It reads 
                                          ../model-results/ChesROMS/grid/chesroms_grd_smoother_msl.nc 
                                          for depth information, so you need mexnc+netcdf_toolbox to 
                                          be able to run this program 

