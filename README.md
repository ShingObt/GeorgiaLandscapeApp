# Georgia Forest resources visualization: With Google Earth Engine App 

![gaga](data)

The app is available from [here](https://sobata5632.users.earthengine.app/view/georgia-landscape).

## About this project


Among the states in the southeastern United States, Georgia has the largest area of timberland. The plantations in Georgia consist predominantly of loblolly pine (Pinus taeda L.), which is the dominant commercial tree species in the southeastern United States. The continuous efforts to increase plantation volume yields have led to the shortening the pine plantation rotations to 20-25 years. Because of the warm and humid climate, the characteristics of the forestland, and common forest management practices, the forest land-scape in Georgia evolves rapidly, showing significant changes over relatively short periods of time. The pertinent question regarding the welfare of Georgia forests is whether they are managed on a sustainable basis.

This web-app shows the spatial forest resource information that provides the fundamental data to analyze the sustainability of the forest resources in Georgia. 


## How to use

This web-app is composed of 4 layers. Users can retrieve the information stored in each layer by manipulating the slider or clicking an arbitrary point on a map. Four layers are; 

- The time series Landsat 5/7/8 composite between 1987-2019. Entire Georgia is covered by this dataset. For selected year, Landsat imagery taken in the middle of the leaf-on season (June to Augst) are used to create annual composite.  
- The estimated growing stock volume (m3/ha). Only the area equivalent to path 17 row 38 in WRS-2 is covered. This layer is created as a part of my graduate study.
- The last disturbance year of forest stands between 1987-2016. This layer is created as a part of my graduate study and summarized in the published papers https://www.mdpi.com/1999-4907/11/3/335,  https://www.jstage.jst.go.jp/article/formath/18/0/18_001/_article/-char/en.
- SRTM Digital Elevation Data Version 4. 

You can:

* Move the slider to change the year of the Landsat composite displayed. 
* Turn on/off the 4 checkboxes at the right panel to show/hide the layers. The checkbox settings are reset when the user change the year of the Landsat composite. 
* Click on the map. Then you will get the information about the point. The information provide is;
    - Coordinates of the selected point
    - The last disturbance year. If no disturbance is recorded, 0 is returned.
    - Elevation (meter)
    - Growing stock volume (m^3/ha). If no volume is recorded, null is returned.
    - Time series chart of the NDVI over the time period. It is possible to export the data by clicking the export button at the top right corner of the chart.
It takes a while until the chart is shown. Thank you for your great patience in advance.

## Development
This section is under construction.
