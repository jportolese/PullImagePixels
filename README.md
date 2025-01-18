This project has three parts and is based on a change detection methodology I'm working on
- It requires a geojson file of polygons (in my case building footprints)
- It also requires two images of the same type a before event image and an after event image
- The geojon file and the imagery must be in the same coordinate system so the first step projects the files (in my case to UTM zone 11 - I used planetscope imagery)
- Buildings (polygons) that are smaller than a certain size are identified and an attribute is added to the file to identify buildings that don't meet the threshold and tags them as "outbuildings"
- The final step takes each footprint and cuts the pixels in the image into a separate image for each footprint for both the before and after imagery.
- The images are numbers by the ID field of the geojson polygon and stored as before_ID.tif and after_ID.tif in the final output directory


  
