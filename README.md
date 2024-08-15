# Topographic Position Index (TPI) Landscape Analysis
ArcGIS toolbox and ArcPy code to run topographic postion index (TPI) analysis across any digital elevation model (DEM). The ArcGIS toolbox (TPI_SemiAutomatedTool.tbx) within this repository contains a model builder realization of steps (TPI_SemiAutomatedID) and a script tool (TPI Standardization). The TPI_SemiAutomatedID model builder semi-automatically identifies positive relief feature polygons across any input digital elevation model (DEM) dataset. The TPI Standardization script tool streamlines this process by calculating elevation and slope variates across input DEMs and standardizes the output based on an input neighborhood annulus neighborhood size. After positive relief feature identification, the model builder tool processes these data and develops Minimum Bounding Geometry attributes for post-analysis and filtering of data to only include features of interest. While originally developed to determine streamlined subglacial bedforms, this tool may be used to find other positive relief features of interest across any input DEM. Applications of this tool and code may be found in [McKenzie et al., 2022](https://onlinelibrary.wiley.com/doi/full/10.1002/esp.5382); [McKenzie et al., 2023](https://tc.copernicus.org/articles/17/2477/2023/); [Abrahams and McKenzie et al., 2024](https://ui.adsabs.harvard.edu/abs/2024EaArX...X51403A/abstract).

The ArcPy code that runs behind the script (TPI_code.py) is also available in this repository.

## Running the TPI toolbox in ArcGIS
To run the tool, the “neighborhood”, “TPI Standardization”, and “standardized output” and “unstandardized output” options need to be replaced within the model builder setup by dragging the “TPI Standardization” tool into the model builder “edit” screen. Make sure that when setting up the neighborhood parameter, you have selected “annulus” and your pixel size of interest. These inputs should be streamlined into the rest of the model builder as is. If you have problems or questions, please contact marion.mckenzie@mines.edu.

## Post-feature identification processing
To utilize this TPI tool to identify streamlined subglacial bedforms across deglaciated landscapes, please see [https://github.com/elliesch/bedfinder](https://github.com/elliesch/bedfinder) and [Abrahams and McKenzie et al., 2024](https://ui.adsabs.harvard.edu/abs/2024EaArX...X51403A/abstract). 

## References & Attribution
If using this specific model builder and script tool, please reference 
[![DOI](https://zenodo.org/badge/768265366.svg)](https://zenodo.org/doi/10.5281/zenodo.11660146)
```
@misc{wiscbaylobe_dataset,
  author       = {Ellianna {Abrahams} and Marion A {McKenzie},
  title        = {bedfinder: A Python package for the Automatic Detection of Glacially-Derived Bedforms},
  year         = {2024},
  doi          = {10.5281/zenodo.11660146},
  url          = {https://zenodo.org/doi/10.5281/zenodo.11660146},
  note         = {Pre-release}
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
