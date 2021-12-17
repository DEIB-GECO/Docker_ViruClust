# Docker ViruClust

Prerequisites:
- the user must have a .tsv file with sequences' metadata from GISAID.
- the user must have installed Docker Desktop (https://www.docker.com/products/docker-desktop)

How to start ViruClust:
1) Download docker-compose.yml

2) Open terminal

3) In terminal, go to the directory where "docker-compose.yml" is.

4) Run command:   FILE_PATH=/path_of_directory_of_tsv FILE_NAME=name.tsv docker-compose up

FILE_PATH is the path of the directory that contains the .tsv previously downloaded from GISAID.

FILE_NAME is the name of the .tsv file.


5) Wait until the process finishes to insert all the data in the database (for big .tsv ~5GB could require few hours)

6) Open in a browser: http://localhost:5000/viruclust/