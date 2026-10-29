* Download_data_from_Geo_Tessera:
Script to download a Tessera embedding (product of 1 year) for a region of interest. Export it as a .tif file.

* Tessera_Embeddings_BWK_2018: example script on how to extract embeddings for point locations and export them to a .csv file for later data analysis (used in grassland phase prediction).

* Tessera_Embeddings_BWK_3years_embeddings: example script on how to extract embeddings from the year of inventory and the two years before, with point locations. Export the embeddings as a .csv file for later data analysis (used in grassland phase prediction).


--> for the concrete grassland phase detection with Tessera embeddings > go to https://github.com/inbo/Slimmebeeldverwerking/tree/main/foundation_model_embeddings_grassland_phase_detection

More documentation on how to work with geotessera: https://geotessera.readthedocs.io/en/latest/quickstart.html


* TS_Pixel_similarity_between_years: This notebook calculates the dot product of each pixel between 2 embedding years. Based on this dot product, we can flag pixels that have been changed moderately or highly. You DO need to download the raw embeddings to visualize them and to calculate/visualize the dotproduct.