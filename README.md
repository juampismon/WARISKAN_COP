# __$8^{th}$  IAHR__ EUROPE CONGRESS | WATER - ACROSS BOUNDARIES

## Teaching and working in the cloud with Copernicus products: _A hands-on tutorial for learning the usefulness of cloud computation for collaboration and teaching on a study case_

This repository contains the guide and notebooks to follow the masterclass example on the [Iberian Peninsula](https://earthobservatory.nasa.gov/images/83321/clear-skies-over-the-iberian-peninsula). In this way, it is hoped that the material deposited here will serve as support for the development of the masterclass sesion hold in the __$8^{th}$  IAHR__ EUROPE CONGRESS on $3^{th}$ june 2024.

The practice is divided into two modules during which different software and routines will be used to generate and process all the data and files necessary for the successful completion of the practice.

Below is a short description of each module and the link to the module guides and notebooks:

## Module 1: Land cover change analysis from an hydrological perspective using Copernicus products
 Throughout this module the watercourse to be studied will be chosen with the help of the [GIS viewer](https://sig.mapama.gob.es/redes-seguimiento/) of the _Redes de Seguimiento del estado e Información Hidrológica_ (Hydrological condition monitoring and information system). Then, the vector files that will serve as a guide (mask) for downloading the Digital Elevation Model (DEM) cartographic sheets will be obtained from the [_Centro de Descargas_](https://centrodedescargas.cnig.es/CentroDescargas/index.jsp) of _Centro Nacional de Información Geográfica_ (CNIG: National Centre for Geographic Information); the vector files shall be obtained from the global hydrological information database [HydroSHEDS](https://www.hydrosheds.org/). Thus, with the software [ArcGIS Pro](https://www.esri.com/es-es/arcgis/products/arcgis-pro/overview) the DEM shall be prepared for use as an input file in the [HEC-HMS](https://www.hec.usace.army.mil/software/hec-hms/). In HEC-HMS, the initial delineation and characterisation of the basin and sub-basins corresponding to the chosen watercourse will be carried out.
 > The notebook used for this module can be found [**here**](https://drive.google.com/file/d/1T_AAegZmpMfl3lThacV7IVZv7YT1leI9/view?usp=drive_link).

## Module 2: Mapping and identifying hotspots for land use change in the Iberian Peninsula from an hydrological perspective
This module deals with the determination of the curve number of the selected basin and subasins. First, the input maps for the calculation of the curve number (slope map, land cover type map, hydrological soil group map) will be obtained. The slope map will be generated based on the same DEM that was used to delineate the watershed in HEC-HMS, the cover type map will be downloaded from the  [_Centro de Descargas_](https://centrodedescargas.cnig.es/CentroDescargas/index.jsp) of CNIG and the hydrological soil groups map will be obtained based on the global soil database  [SoilGrids](https://soilgrids.org/) using the notebook [***01_HydroSoilGroups.ipynb***](https://drive.google.com/file/d/1m0-gqsJ8hgjDftCJsIDhrLBTH9EXQO8K/view?usp=drive_link). It is worth mentioning that it may also not be necessary to determine a hydrological soil group map if it is observed that the entire catchment lies over the area marked for the same hydrological soil group in the GIS viewer ([SIGCAR](https://beta.sigcar.es/sigc.php)). 

Second, a map with reference ids for each combination of land cover type, hydrological soil group and slope will be created so that it can be related to the table  ___Tabla 2.4 GRUPOS HIDROLÓGICOS DE SUELO A EFECTOS DE LA DETERMINACIÓN DEL VALOR INICIAL DEL UMBRAL DE ESCORRENTÍA___ of the Spanish standard [Norma 5.2-IC](https://www.boe.es/boe/dias/2016/03/10/pdfs/BOE-A-2016-2405.pdf) (Ministerio de Fomento, 2016, España). Finally, the average curve number of the basin and each sub-basin will be determined with the notebook [***02_CN.ipynb***](https://drive.google.com/file/d/1tP7SXDDBBRIZwFxquHCs95xx7k_-qnoH/view?usp=drive_link).
 > The guide for this module can be found [**here**](https://drive.google.com/file/d/1s7X12alEYK3EqXbn0CkLvhyjdVpXRKlL/view?usp=drive_link).

## Module 3: Hydrological characterisation of the basin (Part 3)
In this module the time series with precipitation information for the basin will be obtained and prepared. This information shall be extracted from the data set [Spain02](https://www.aemet.es/es/serviciosclimaticos/cambio_climat/datos_diarios?w=2&w2=1), jointly developed by  Spanish meteorological agency  [AEMET](https://www.aemet.es/en/portada) and the [Santander Meteorology Group (UC-CSIC)](https://github.com/SantanderMetGroup), Notebooks  [***03_SPAIN02.ipynb***](f) will be used for this. Likewise, with these precipitation time series, IDF curves and storm hyetograms will be constructed for each data point with the notebooks. [***04_CurvasIDF.ipynb***](f) and [***05_Hietograma.ipynb***](f). 
 > The guide for this module can be found  [**here**](f) (To be uploaded, until next class).


## Module 4: Hydrological characterisation of the basin (Part 4)
Following the notebooks [***06_ThiessenPoly.ipynb***](f) and [***07_Hypsometric.ipynb***](f) the mean annual precipitation for the basin and each sub-basin shall be determined according to the Thiessen polygon method and the hypsometric method, respectively.On the other hand, the notebook [***08_Clark_Muskingum.ipynb***](f) will be followed to construct the Clark unit hydrograph and estimate the Muskingum K and X parameters to define the transit of the hydrograph corresponding to a gauged section of the river basin network. For this, it will be necessary to download from the [gauging yearbook](https://ceh.cedex.es/anuarioaforos/demarcaciones.asp) the daily flow information measured at a gauging station in the basin.
 > The guide for this module can be found [**here**](f) (To be uploaded, until next class).

## Module 5: Generation of response hydrographs with Hec-HMS
This module can be divided into two parts: 
- In the first part, a calibration of the K and X parameters corresponding to the Muskingum routing method will be carried out for the main sections of the basin defined in HEC-HMS. For this purpose, the model will be configured according to the characterisation of the basin carried out in the previous modules and the daily flow data discharged at the gauging station will be used for the calibration.
- In the second part, the calibrated hydrological model in HEC-HMS will be used to generate response hydrographs for the return periods of 10, 100 and 500 years. For this purpose, synthetic hydrographs generated for the mentioned return periods using the notebooks [***09_Synthetic_Hyetograms***]() and [***00_Hydro_Functions***]() will be used .
 > The guide for this module can be found  [**here**](f) (To be uploaded, until next class)

# How to run the notebooks


Notebooks can be followed in two ways: "_Locally_" by installing Python and Jupyter and in _The Cloud_ without installing anything on the computer via [Google Colab ](https://colab.research.google.com/). The first way requires the prior installation of Python, as well as Jupyter and the required libraries for the execution of the notebooks (in the repository there is an environment that has the necessary libraries, however, compatibility problems may occur). On the other hand, to use google Colab you need a [Google account](https://www.google.com/intl/es/account/about/).

|Abre Colab para ejecutar los notebooks pulsando aquí abajo|
|:-:|
|[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)|

# License

The documentation in this repository is protected under the [GNU Free Documentation License Version 1.3](https://www.gnu.org/licenses/fdl-1.3.html)

    Copyright (C)  2023 Juan Pablo García Montealegre.
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3
    or any later version published by the Free Software Foundation;
    with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts.
    A copy of the license is included in the section entitled "GNU
    Free Documentation License"
    
The notebooks contained in this repository are protected under the  [GNU General Public License Version 3](https://www.gnu.org/licenses/gpl-3.0.html#license-text).

    Copyright (C) <2023>  <Juan Pablo García Montealegre>

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details
