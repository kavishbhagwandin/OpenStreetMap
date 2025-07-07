# OpenStreetMap

This project makes use of an existing recommender server --> https://github.com/martaannaj/RecommenderServer, and this is the paper --> https://link.springer.com/content/pdf/10.1007/978-3-030-49461-2_11.pdf

The python file (Jupyter file) was made in the same folder as the RecommenderServer, after setting up the server based on their instructions, a .exe file should 
have been created in the same folder (for me at leats it did).

The data that was used is downloaded from OpenStreetMap Geofabric's server, "netherlands-latest.osm.pbf".
The data is then extracted using the osmium library (https://wiki.openstreetmap.org/wiki/Osmium) (https://lonvia.github.io/geopython17-pyosmium/#1), take note
that the extraction took almost **8 HOURS!!!** for me.

When building the server, you need your data to be in a .tsv file or another format if that is specified in their setup.
This is the command i use to build the server: ./RecommenderServer.exe build-tree from-tsv "your_tsv_file".tsv 

After the server has been build, a .tsv.schemaTree.typed.pb file will be created and we use it to start running the file.
This is the command i use to start running the server: ./RecommenderServer.exe serve "your_tsv_file".tsv.schemaTree.typed.pb
