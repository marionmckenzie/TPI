# Topographic Position Index (TPI) Landscape Analysis
ArcGIS toolbox and ArcPy code to run topographic postion index (TPI) analysis across any digital elevation model (DEM). The ArcGIS toolbox (TPI_SemiAutomatedTool.tbx) within this repository contains a model builder realization of steps (TPI_SemiAutomatedID) and a script tool (TPI Standardization). The TPI_SemiAutomatedID model builder semi-automatically identifies positive relief feature polygons across any input digital elevation model (DEM) dataset. The TPI Standardization script tool streamlines this process by calculating elevation and slope variates across input DEMs and standardizes the output based on an input neighborhood annulus neighborhood size. After positive relief feature identification, the model builder tool processes these data and develops Minimum Bounding Geometry attributes for post-analysis and filtering of data to only include features of interest. While originally developed to determine streamlined subglacial bedforms, this tool may be used to find other positive relief features of interest across any input DEM. Applications of this tool and code may be found in [McKenzie et al., 2022](https://onlinelibrary.wiley.com/doi/full/10.1002/esp.5382); [McKenzie et al., 2023](https://tc.copernicus.org/articles/17/2477/2023/); [Abrahams and McKenzie et al., 2024](https://ui.adsabs.harvard.edu/abs/2024EaArX...X51403A/abstract).

The ArcPy code that runs behind the script (TPI_code.py) is also available in this repository.

## Running the TPI toolbox in ArcGIS
Please follow the below step-by-step instructions to make the TPI tool operable in new ArcGIS projects. 
1. After downloading the toolbox and the TPI_code.py file, add the toolbox to an ArcGIS project.
2. Within the toolbox, you should see both the script tool "TPI Standardization" and model builder "TPI_SemiAutomatedID".
3. Right click on the script tool and select "Properties".
4. Then, under the "Execution" tab, navigate to the "TPI_code.py" file and select. This now connects the ArcPy code to the script tool that will allow it to run.
5. Back in the toolbox, right click on the "TPI_SemiAutomatedID" model builer and select "Edit".
6. Within the model build, you will need to replace the existing “neighborhood”, “TPI Standardization”, and “standardized output” options with your newly configured script tool by dragging the “TPI Standardization” tool onto the model builder screen. Make sure that when setting up the neighborhood parameter, you have selected “annulus” and your pixel size of interest.

Once completing these steps, these inputs can be streamlined into the rest of the model builder as is. If you have problems or questions, please contact marion.mckenzie@mines.edu. A video for making the TPI tool operable within new ArcGIS projects will be available through a Jupyter Book by the end of 2024. The current TPI_code.py configuration only saves the standardized raster from TPI analysis. The standardized raster dataset is input into the rest of the "TPI_SemiAutomatedID" model builder. Lines of code are available within TPI_coe.py to save the unstandardized TPI raster as well and just need to be commented in. 

## Post-feature identification processing
To utilize this TPI tool to identify streamlined subglacial bedforms across deglaciated landscapes, please see [https://github.com/elliesch/bedfinder](https://github.com/elliesch/bedfinder) and [Abrahams and McKenzie et al., 2024](https://ui.adsabs.harvard.edu/abs/2024EaArX...X51403A/abstract). 

## References & Attribution
If you make use of the TPI tool, please cite:
[![DOI]([https://zenodo.org/badge/DOI/10.5281/zenodo.13685546.svg](https://zenodo.org/records/13685546)
```
@misc{TPI_dataset,
  author       = {Marion A {McKenzie},
  title        = {Topographic Position Index (TPI) enabled for ArcGIS},
  year         = {2024},
  doi          = {10.5281/zenodo.13685546},
  url          = {[https://zenodo.org/records/13685546](https://zenodo.org/records/13685546)},
  note         = {v1.0.0}
}
```

If utilizing any previously ientified streamlined subglacial bedforms from  McKenzie et al., 2022, please reference
```
@misc{mckenzie2022_dataset,
 author={Marion A {McKenzie} and Lauren M {Simkins} and Sarah M {Principato}},
 title={{Streamlined subglacial bedforms across the deglaciated Northern Hemisphere}},
 year={2022},
 doi={10.1594/PANGAEA.939999},
 url={https://doi.org/10.1594/PANGAEA.939999},
 type={data set},
 publisher={PANGAEA}
}
```
