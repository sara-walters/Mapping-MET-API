### Mapping Antiquities from the Art Institute of Chicago's Collections

The metadata for each object in the Art Institute’s collection was accessed through the museum’s public API. The script collects information about each object’s place of origin and provenance, along with a link to the object’s image and the original item record. 

For more on the the Art Institute's API: https://api.artic.edu/docs/#introduction 

Using the information provided by the “Place of Origin” field, each artifact was manually matched with coordinates provided by a gazetteer. Historical place names were identified using the ancient gazetteer Pleiades, and modern place names were identified through OpenStreetMap. 

The original data is available to access in AIC_Artifacts_Greek-Roman-Byzantine.xlsx, and the cleaned version with updated coordinates is in CLEANED_AIC_Artifacts_Greek-Roman-Byzantine.xlsx. 
 
### Notes about data collection and cleaning

Only items that were linked with detailed geographic information were mapped. For a majority of the records, the “place of origin” field only includes broad regional or country information. These records were excluded from the cleaned data. 

(Examples of excluded place names: Anatolia, Ancient Greece, Ancient Egypt, Ancient Mediterranean, Byzantine Empire, Eastern Europe, Eastern Mediterranean, Egypt, Greece, Iran, Iraq, Italy, Macedonia, Levant, North Africa, Southern Italy, Syria)

Because the API query had to be made through a keyword search rather than accessing the “Greek, Roman, and Byzantine” collection directly, the original data also included a significant amount of data from outside this area that included keywords like “greek” or “roman” in their metadata – mostly objects produced in Western Europe and the United States in the 19th and 20th century. These records were excluded from the cleaned data as well. A future project would need to refine the script in order to avoid picking up these types of additional results. 
