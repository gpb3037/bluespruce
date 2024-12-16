# bluespruce
Habitat suitability analysis for the Colorado Blue Spruce

NOTE: This repository was intended to be the test repository with a new one being made called TreeHabitat to be more generalized, but problems were encountered with file space limitations
based on too large a selection of data, thus for purposed of this project the test repository will be used.

Blue spruce (Picea pungens) is also called Colorado blue spruce, 
Colorado spruce, silver spruce, and pino real.
https://www.srs.fs.usda.gov/pubs/misc/ag_654/volume_1/picea/pungens.htm

Areas of focus (find FIPS codes vis https://www.census.gov/library/reference/code-lists/ansi.html#cou)
Primary - Boulder County, Colorado  (FIPS 08013)
Secondary, based upon similar characteristics to Boulder County

<!-- attempted to implement the following in the TreeHabitat repositiory but only got as far as defining
the county shapefiles and associated linear water features 
**Taos County, New Mexico (FIPS 35055)
Elevation: 5,000 to 13,000 feet.
Climate: Cold winters and monsoon-driven precipitation.
Features: Shares a focus on natural land conservation and mountainous terrain.

Albany County, Wyoming (FIPS 56001)
Elevation: Ranges from around 5,000 to 13,000 feet.
Climate: Similar to Boulder County with cold winters and a combination of alpine and montane zones.
Vegetation: Forested areas with suitable conditions for blue spruce, particularly around the Medicine Bow Range.
Land Use: Mixed urban (Laramie) and wilderness areas like the Medicine Bow National Forest, which supports blue spruce.** -->

Data sources
from Census TIGER Topologically Integrated Geographic Encoding and Referencing system
reference https://www.census.gov/programs-surveys/geography/guidance/tiger-data-products-guide.html

Boundary - Census county boundaries selected by FIPS code from shapes within  https://www2.census.gov/geo/tiger/TIGER2024/COUNTY/tl_2024_us_county.zip

Hydrography - Census linear water for selected FIPS codes
https://www2.census.gov/geo/tiger/TIGER2024/LINEARWATER/tl_2024_08013_linearwater.zip  BOULDER


<!-- the following were not implemented except at the start of the TreeHabitat repository
 https://www2.census.gov/geo/tiger/TIGER2024/LINEARWATER/tl_2024_35055_linearwater.zip  TAOS
https://www2.census.gov/geo/tiger/TIGER2024/LINEARWATER/tl_2024_56001_linearwater.zip  ALBANY -->

Digital Elevation Model -
##### SRTM or the Shuttle Radar Topography Mission was started 1999 onboard the Endeavour and collected data for 11 days. As the orbit of the shuttle was not circumpolar but sinusoidal it was only possible to  cover a small portion of the earth surface. The shuttle therefore used the reflection of emitted radar signals in the so-called C-band (wavelength 5.6 cm) for the SIR-C sensor developed by the Jet Propulsion Laboratory and the X-band (wavelength 3.1 cm) for the X-SAR sensor developed by the German Aerospace Agency. The mission was clear: map the world!


##### 90m at ground worldwide
##### active system
##### from 60° north latitude to 58° south
##### acquired 2000 /different releases
##### free download without registering
##### once acquired, source data hasn’t changed

Aspect (North, East, South, or West facing) will be a derived factor from the DEM

Climate - Geophysical Fluid Dynamics Laboratory Earth System Model 2G 
Differences in the ocean mean state include the thermocline depth 
being relatively deep in ESM2M and relatively shallow in ESM2G compared to observations
ref https://www.usgs.gov/publications/gfdls-esm2-global-coupled-climate-carbon-earth-system-models-part-i-physical
The timeframes selected were 2016-2020 and 2046-2050 and only the model is condidered in the analysis
the goal would be to compare the acutal data collected 2016-2020 with the model to provide
inferences about the later estimates.
In a more rigorous analysis several models pertinent to north america would be considered