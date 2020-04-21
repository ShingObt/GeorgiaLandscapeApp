# Georgia Forest resources visualization: With Google Earth Engine App 

![gaga](data)

The app is available from [here](https://sobata5632.users.earthengine.app/view/georgia-landscape).

## About this project


Among the states in the southeastern United States, Georgia has the largest area of timberland. The plantations in Georgia consist predominantly of loblolly pine (Pinus taeda L.), which is the dominant commercial tree species in the southeastern United States. The continuous efforts to increase plantation volume yields have led to the shortening the pine plantation rotations to 20-25 years. Because of the warm and humid climate, the characteristics of the forestland, and common forest management practices, the forest land-scape in Georgia evolves rapidly, showing significant changes over relatively short periods of time. The pertinent question regarding the welfare of Georgia forests is whether they are managed on a sustainable basis.

This web-app shows the spatial forest resource information that provides the fundamental data to analyze the sustainability of the forest resources in Georgia. 


## How to use

This web-app is composed of 4 layers. Users can retrieve the information stored in each layer by manipulating the slider or clicking an arbitrary point on a map. Four layers are; 

- The time series Landsat 5/7/8 composite between 1987-2019. Entire Georgia is covered by this dataset.
- The estimated growing stock volume (m3/ha). Only the area equivalent to path 17 row 38 in WRS-2 is covered. This layer is created as a part of my graduate study.
- The last disturbance year of forest stands between 1987-2016. This layer is created as a part of my graduate study and summarized in [^1] [^2]. 
- SRTM Digital Elevation Data Version 4. 

You can:

* Filter each column by sort in boxes under the header of each column.
* Order the columns by clicking on the column header (ascending and descending).
* Adjust the columns are visible by clicking the Visibility button for columns.
* Click the 'CSV' or 'Excel' button to save the filtered data to the.csv or.xlsx file
* See how many entries are left in the bottom-left after screening, where it states 'Showing X to Y Z entries'


[^1]: Obata, Shingo et al. 2019. “Preliminary Analysis of Forest Stand Disturbances in Coastal Georgia (USA) Using Landsat Time Series Stacked Imagery.” FORMATH 18: 1–11.

[^2]: Obata, Shingo, Pete Bettinger, Chris J. Cieszewski, and Roger C. Lowe III. 2020. “Mapping Forest Disturbances between 1987-2016 Using All Available Time Series Landsat TM/ETM+ Imagery: Developing a Reliable Methodology for Georgia, United States.” Forests 11(3): 335.


## Development

### Data collection

The store location is collected from the websites of [Yoshinoya](https://www.yoshinoya.com/en/) and [Starbucks Japan](https://www.starbucks.co.jp/en/index.html).

I used [Python 3.5.1](https://www.python.org/downloads/release/python-351/) operating under [Anaconda Distribution](https://www.anaconda.com/distribution/) to scrape store information from two websites. The modules employed for the task are:

* [selenium](https://pypi.org/project/selenium/) for web-scraping.
* [pandas](https://pandas.pydata.org/) to manage and structure the scraped data.
* [googlemaps](https://github.com/googlemaps/google-maps-services-python) to use [Geocoding API](https://developers.google.com/maps/documentation/geocoding/start) provided by Google.

As a result of the scraping with Python, All the store name,store address, and store coordinates (defined by latitude and longitude) are obtained in the python code.

### Interactive web-app

To create interactive web-app, [R v3.5.1](https://www.r-project.org/) and [Rstudio v 1.1.423](https://rstudio.com/) are used. R Markdown based [flexdashboard](https://rmarkdown.rstudio.com/flexdashboard/) is the key feature for this ap. The R packages employed for the creation of this web-app are:

* flexdashboard
* [leaflet](https://rstudio.github.io/leaflet/) to achieve interactive mapping of the rasters and points. 
* [DT](https://rstudio.github.io/DT/) to create interactive table.
* [crosstalk](https://rstudio.github.io/crosstalk/) for inter-widget (between filters, table, and map) interaction.
* [rgdal](https://cran.r-project.org/package=rgdal), [raster](https://cran.r-project.org/package=raster/raster.pdf), and [sp](https://cran.r-project.org/package=sp/sp.pdf) to handle the spatial dataset. 

### Resources

This web-app is located at [my portfolio site](https://shingobt.github.io/visualization/flexdashboard) (the portfolio site itself is under construction). 

### Future works

Remained tasks for this project are:

* scraping more information from the websites such as parking lot availability and business hour.
* adding more franchises as the object of comparison.
* performing more advanced geospatial analysis.
