# Docker ViruClust

To execute ViruClust the user must have a .tsv file with sequences' metadata from GISAID.

1) Download docker-compose.yml

2) Open terminal

3) In terminal, go to the directory where "docker-compose.yml" is.

4) Run command:   FILE_PATH=/path_of_directory_of_tsv FILE_NAME=name.tsv docker-compose up



FILE_PATH is the path of the directory that contains the .tsv previously downloaded from GISAID.

FILE_NAME is the name of the .tsv file.