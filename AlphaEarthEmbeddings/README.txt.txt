GEE directory:
--------------
Contains 2 scripts that can be run in Google Earth Engine.

* GEE_script_for_similarity_search: 
Script that samples embeddings from a 1-year product within a specific area (area of interest: AOI). A 50-metre buffer is used around three reference points (chosen arbitrarily here) to sample embeddings; it then calculates the ‘average embedding vector’ and, based on cosine similarity, compares this average embedding vector with the embedding vectors of all pixels falling within your AOI. Cosine similarity is mathematically equivalent to the Pearson correlation between these vectors when mean-centred (mean = 0). Based on the Z-scores of this cosine similarity, you can then search for pixels that closely resemble your reference (the mean embedding vector, calculated from your points) based on a chosen threshold value. A high Z-score means we are applying stricter criteria and looking for pixels that are very similar. Your embedding product for that year (RGB based on your own chosen 3 embeddings), your Z-scores from your cosine similarity, and the pixels that meet your threshold value. 



* GEE_script_download_yearly_embeddings_for_Flanders: 
Script that downloads the Alpha Earth Embeddings for Flanders and export it to a defined folder. 


Google Colab Notebooks directory:
---------------------------------
Contains 4 scripts that can be run in jupyter notebook, but uses the gee and ee packages. You do need a Google Earth Engine account to work with these notebooks.

* AE_Find_similar_pixels_within_one_embedding_year:quite similar to the GEE_script_for_similarity_search. This notebook select habitats from the BWK, select some pixels from these habitat polygons. Extract the embeddings from the embeddings of that year. Calculate the mean vector embedding, calculate the cosine similarity of each pixels of that embedding year with this vector. Calculate the Z-scores and perform thresholding to distinguish similar and non-similar pixels. Evaluate the "similar" pixels with points of that same habita (but that have been iventoried in another year). 

* AE_Pixel_similarity_between_years: This notebook calculates the dot product of each pixel between 2 embedding years. Based on this dot product, we can flag pixels that have been changed moderately or highly. You DON'T need to download the raw embeddings to visualize them and to calculate/visualize the dotproduct.

* AE_Embeddings_BWK_2018: example script on how to extract embeddings for point locations and export them to a .csv file for later data analysis (used in grassland phase prediction).

* AE_Embeddings_BWK_3years_embeddings: example script on how to extract embeddings from the year of inventory and the two years before, with point locations. Export the embeddings as a .csv file for later data analysis (used in grassland phase prediction).

--> for the concrete grassland phase detection with Alpha Earth embeddings > go to https://github.com/inbo/Slimmebeeldverwerking/tree/main/foundation_model_embeddings_grassland_phase_detection

