# __$8^{th}$  IAHR__ EUROPE CONGRESS | WATER - ACROSS BOUNDARIES

## Teaching and working in the cloud with Copernicus products: _A hands-on tutorial for learning the usefulness of cloud computation for collaboration and teaching on a study case_

This repository contains the guide and notebooks to follow the masterclass example on the **Iberian Peninsula**. In this way, it is hoped that the material deposited here will serve as support for the development of the masterclass sesion hold in the $8^{th}$  _IAHR EUROPE CONGRESS_ on $3^{th}$ june 2024. The practice is divided into two modules during which different notebooks will be used to generate and process all the data and files necessary for the successful completion of the practice.

> The [masterclass has a Drive folder](https://drive.google.com/drive/folders/15QpFKMZtpjjnCSg4C5bYA8Lu8i46iThw?usp=drive_link) with data, notebooks, results and documentation.

Below is a short description of each module and the link to the module guides and notebooks:

### Module 1: Land cover change analysis from an hydrological perspective using Copernicus products
 This is an introductory module to the different tools that can be used in geosciences to work in the cloud, from python and some of its most recognised scientific libraries (e.g. pandas, matplotlib, seaborn, etc.) to the _Harmonized Data Access_ (HDA) API__ to access a huge amount of open data. This module centres around an analysis of land cover change in the Iberian Peninsula from a hydrological perspective. First, we must [create](https://support.google.com/mail/answer/56256?hl=en) (or use if we already have one) a secondary gmail account separate from our personal and laboral accounts, if we are concerned about giving access to our Drive information (Google Colab and Drive will connect during the class and certain file manipulation permissions will need to be given). Second, we must create a Wekeo's account, you can register [here](https://www.wekeo.eu/register). Finally, we can follow the instructions in notebook [***01_EDA_LULC_CHANGE.ipynb***](https://colab.research.google.com/github/juampismon/IAHR24_LISBON/blob/main/01_EDA_LULC_CHANGE.ipynb) to get down to business.
 

### Module 2: Mapping and identifying hotspots for land use change in the Iberian Peninsula from an hydrological perspective
This module deals with the determination of the precipitation excess/runoff change of selected basins and subasins due to the land cover change  in the Iberian Peninsula. The expected precipitation excess change is determined using the SCS Curve Number (CN) approach. The input maps for the calculation of the curve number (slope map, land cover type map, hydrological soil group map) will be obtained from Copernicus products and [SoilGrids](https://soilgrids.org/) products. The slope map will be generated based on the Copernicus Digital Elevation Model ([COP-DEM GLO-90](https://spacedata.copernicus.eu/collections/copernicus-digital-elevation-model)), which has 90 meters resolution, using the notebook [***02_Slope.ipynb***](https://colab.research.google.com/github/juampismon/IAHR24_LISBON/blob/main/02_Slope.ipynb). The average curve number of the basin and each sub-basin will be determined with the notebook [***03_CN_2012_2018.ipynb***]("https://colab.research.google.com/github/juampismon/IAHR24_LISBON/blob/main/03_CN_2012_2018.ipynb). The curve number will be estimated using a map with reference ids for each combination of land cover type, hydrological soil group and slope will be created so that it can be related to the table  ___Tabla 2.4 GRUPOS HIDROLÓGICOS DE SUELO A EFECTOS DE LA DETERMINACIÓN DEL VALOR INICIAL DEL UMBRAL DE ESCORRENTÍA___ of the Spanish standard [Norma 5.2-IC](https://www.boe.es/boe/dias/2016/03/10/pdfs/BOE-A-2016-2405.pdf) (Ministerio de Fomento, 2016, España). Finally, the precipitation excess change wil be estimated using notebook [***04_Pexcess.ipynb***](https://colab.research.google.com/github/juampismon/IAHR24_LISBON/blob/main/04_Pexcess.ipynb).

# How to run the notebooks


Notebooks can be followed in two ways: "_Locally_" by installing Python and Jupyter and in _The Cloud_ without installing anything on the computer via [Google Colab ](https://colab.research.google.com/). The first way requires the prior installation of Python, as well as Jupyter and the required libraries for the execution of the notebooks (in the repository there is an environment that has the necessary libraries, however, compatibility problems may occur). On the other hand, to use google Colab you need a [Google account](https://www.google.com/intl/es/account/about/).

|Abre Colab para ejecutar los notebooks pulsando aquí abajo|
|:-:|
|[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)|


