# Docker ViruClust

Prerequisites:
- the user must have a .tsv file with sequences' metadata from GISAID. Here follows the expected header with one example line: 
| Virus name | Type | Accession ID | Collection date | Location | Additional location information | Sequence length | Host | Patient age | Gender | Clade | Pango lineage | Pangolin version | Variant | AA Substitutions | Submission date | Is reference? | Is complete? | Is high coverage? | Is low coverage? | N-Content | GC-Content |
| --- | --- | --- | --- |--- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
hCoV-19/Italy/XXX/2020 | betacoronavirus | EPI_ISL_XXXXXX | 2020-01-01 | Europe / Italy / Italy |  | 29903 | Human | unknown | unknown | G | B.1 | 2021-01-01 |  | (NSP15_A283V,NSP12_P323L,Spike_D614G) | 2020-04-17 |  | True | True |  | 0.0068649119282 | 0.379674275888 |
- the user must have installed Docker Desktop (https://www.docker.com/products/docker-desktop)

How to start ViruClust:
1) Download docker-compose.yml

2) Open terminal

3) In terminal, go to the directory where "docker-compose.yml" is

4) Run command: `FILE_PATH=/path_of_directory_of_tsv FILE_NAME=name.tsv docker-compose up`, where:

  - FILE_PATH is the path of the directory that contains the .tsv previously downloaded from GISAID.

  - FILE_NAME is the name of the .tsv file.

5) Wait until the process finishes to insert all the data in the database (big .tsv files ~5GB could require a few hours)

6) Open in a browser: http://localhost:5000/viruclust/

The process can be stopped with CTRL+C; it can be restarted using the same or new .tsv files, requiring to rerun the whole upload.
