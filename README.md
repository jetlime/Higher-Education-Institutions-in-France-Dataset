# Higher Education Institutions in France - Dataset

This repository contains a dataset of higher education institutions in France.  This includes x higher education institutions in France, including universities, universities of applied sciences, colleges of art and music, colleges of public administration, theological universities, and colleges of education.
This dataset was generated based on the . The data is being made publicly available to promote open science principles [2].

L'Onisep (Office national d'information sur les enseignements et les professions) est un opérateur de l’État relevant du ministère de l’Éducation nationale et de la Jeunesse et du ministère de l’Enseignement supérieur et de la Recherche. L'Onisep produit et diffuse toute l'information sur les formations et les métiers. Il offre également des services aux élèves, aux parents et aux équipes éducatives. 


L’Office national d'information sur les enseignements et les professions, plus connu sous l'acronyme ONISEP, est un organisme public français ayant le statut d'établissement public à caractère administratif. La direction (services centraux) est basée à Lognes. 

## Data

The data includes the following fields for each institution:

- Id: A unique identifier assigned to each institution.
- Region: The federal state in which the institution is located.
- Name: The full name of the institution.
- Category: Indicates whether the institution is public or private.
- Url: The website of the institution.

## Methodology

The methodology for creating the dataset involved obtaining data from two sources: the German federal office for statistics (Destatis)[3] and Hochschulkompass (HSK)[4].


1. Principal higher secondary education, https://www.data.gouv.fr/fr/datasets/principaux-etablissements-d-enseignement-superieur-mesr/#/resources. "Caractéristiques des principaux établissements d'enseignement supérieur." Provided by the ministry of Higher Education and Research (updated  14 mars 2024, accessed 15 march 2024).

2.Onisep - Idéo-Structures d'enseignement supérieur (Licence ODBL):  https://opendata.onisep.fr/data/5fa586da5c4b6/2-ideo-structures-d-enseignement-superieur.htm?tab=download (higher ed. without URLS)

&

Idéo-Actions de formation initiale-Univers enseignement supérieur https://opendata.onisep.fr/data/605344579a7d7/2-ideo-actions-de-formation-initiale-univers-enseignement-superieur.htm?tab=table_605385c5cd64c (all formations with URL)

The data from Destatis was obtained by requesting a list of registered HEIs, which was provided in the form of three spreadsheets. The data from these spreadsheets was then split into four CSV files, including a consolidated file that mapped each HEI to its type based on type-implying abbreviations in the name (`heis-mapped.csv`). However, the dataset did not contain website URLs for each HEI, so the URLs were manually obtained by conducting a Google search for each HEI's name and verifying the website using specific indicators. The resulint dataset is in `heis-mapped-url.csv`.

The HSK dataset was downloaded from the HSK website and converted to a CSV file. The CSV file was then used to verify the website URLs obtained from the manual collection process.

o validate and resolve any differences between the two datasets, a comparison was conducted using an OpenOffice spreadsheet. Funding types were classified into two categories (private and public), and mismatches in HEI types were ignored. Mismatching URLs were checked for redirects to the same destination domain, and mismatches in regions were resolved by checking the address on the website's imprint/contact page. For multiple mismatches, the aforementioned resolutions were applied, thus bringing them down to one difference, making them resolvable again.

Overall, this methodology ensured that the German HEIs dataset contains accurate and reliable information about registered HEIs in Germany. The final data was compiled into the dataset included in this repository.

## Usage

This data is available under the Creative Commons Zero (CC0) license and can be used for academic research purposes. We encourage the sharing of knowledge and the advancement of research in this field by adhering to open science principles [2].

If you use this data in your research, please cite the source and include a link to this repository. To properly attribute this data, please use the following DOI: TBA.

## Contribution

If you have any updates or corrections to the data, please feel free to open a pull request or contact us directly. Let's work together to keep this data accurate and up-to-date.

## Acknowledgment

TBA.

## References

1. TBA.
2. S. Bezjak, A. Clyburne-Sherin, P. Conzett, P. Fernandes, E. Görögh, K. Helbig, B. Kramer, I. Labastida, K. Niemeyer, F. Psomopoulos, T. Ross-Hellauer, R. Schneider, J. Tennant, E. Verbakel, H. Brinken, and L. Heller, Open Science Training Handbook. Zenodo, Apr. 2018. [Online]. Available: [https://doi.org/10.5281/zenodo.1212496]
3. French National Office for Information on Education and the Professions (*ONISEP*) - Dataset X, Jan 20XX. Available: [x](https://www.onisep.fr/) (Accessed March 2024).