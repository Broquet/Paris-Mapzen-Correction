# Paris-Mapzen-Correction

# Wrangle OpenStreetMap Data Project Project overview

XML OSM dataset of Paris have been downloaded from https://mapzen.com/data/metro- extracts/ (https://mapzen.com/data/metro-extracts/). I chose to analyze Paris, as I recently went there for my holidays and wanted to know if the data conerning this city was consistent. The OSM downloaded is 975Mo. Therefore, it has been parsed with a parameter of k = 100, so that codes could be applied faster. Then, munging techniques have been applied to the data, such as assessing the quality of the data for validity, accuracy, completeness, consistency and uniformity, to clean the OpenStreetMap data. Errors in the dataset have been identified and corrected about:
Amenities Street names Postal codes
Then, the file has been converted to CSV and finally, SQL has been used to the data schema to complete the project.

# The Dataset
OpenStreetMap's data are structured in well-formed XML documents (.osm files) that consist of the following elements:
* Nodes: individual dots used to mark specific locations (such as a postal box). Two or more nodes are used to draw line segments or "ways".
* Ways: a line of nodes, displayed as connected line segments. "Ways" are used to create roads, paths, rivers, etc.
* Relations: When "ways" or areas are linked in some way but do not represent the same physical thing, a "relation" is used to describe the larger entity they are part of. "Relations" are used to create map features, such as cycling routes, turn restrictions, and areas that are not contiguous. The multiple segments of a long way, such as an interstate or a state highway are grouped into a "relation" for that highway. Another example is a national park with several locations that are separated from each other. Those are also grouped into a "relation".
* Tags: description of names or types of elements, such as roads and other attributes.
