## Cached Locations - Preload Map Locations 
#### Problem: App takes several seconds to load map locations

### Discussion
***Solution***

After fetching charging stations, persist them to local storage in an R-Tree. As the map's visible area changes, the widget loads cached locations while making the API call to the recommendation engine.

***Challenges***

- Location sample size
- Inaccurate location data
- Capturing comparable metrics

***Implementation*** 

This example uses the Google Maps SDK and includes an 80mb geojson file that represents 340,000 unique locations in California and Texas. The sheer amount of JSON data presents some issues worth considering on the mobile end. 

