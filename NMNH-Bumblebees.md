## Dataset Summary 

The USNM Bumblebee Dataset is a natural history dataset containing, for each of 73,497 Bumblebee specimens in the family Apidae, a single image in lateral or dorsal view and a tab-separated value file with occurrence data. Occurrence data includes the species classification, the date and site/location of collection, and other metadata conforming to the Darwin Core data standard (https://dwc.tdwg.org). 11,421 specimens are not identified to species and these specimens are included as 'Bombus sp.' or 'Xylocopa sp.' The collecting sites/locations of the majority of specimens (55,301), have been georeferenced. The dataset is worldwide in scope, but is limited to the specimens available in the Smithsonian USNM collection.  

## Languages 

English 

## Data Instances 

A typical data point comprises of the specimen metadata and image information for a single bumblebee specimen.

An example from the dataset looks as follows:

```json
{
  'occurrenceID': 'http://n2t.net/ark:/65665/30042e2d8-669d-4520-b456-e3c64203eff8',
  'catalogNumber': 'USNMENT01732649',
  'recordedBy': 'R. Craig',
  'year': '1949',
  'month': '4',
  'day': '13',
  'country': 'United States',
  'stateProvince': 'California',
  'county': 'Fresno',
  'locality': 'Auberry',
  'decimalLatitude': '37.0808',
  'decimalLongitude': '-119.485',
  'identifiedBy': "O'Brien, L. R.",
  'scientificName': 'Xylocopa (Notoxylocopa) tabaniformis orpifex',
  'genus': 'Xylocopa',
  'subgenus': 'Notoxylocopa',
  'specificEpithet': 'tabaniformis',
  'infraspecificEpithet': 'orpifex',
  'scientificNameAuthorship': 'Smith',
  'accessURI': 'https://ids.si.edu/ids/deliveryService?id=NMNH-USNMENT01732649',
  'PixelXDimension': 2000,
  'PixelYDimension': 1212
}
```

## Data Fields 

Specimen metadata fields conform to the Darwin Core data standard and are detailed here: https://dwc.tdwg.org. Image metadata fields conform to the Audiovisual Core data standard and are detailed here: https://ac.tdwg.org/.

## Curation Rationale 

The dataset represents a portion of the U. S. National Entomological Collection. The U.S. National Entomological Collection (USNM) traces its origins in part to the acquisition of the U.S. Department of Agriculture Collection of 138,000 specimens donated in 1885. These specimens became the foundation of one of the world’s largest and most important accessible entomological collections, with over 33 million specimens taken care of by the combined staff of three government agencies: the Smithsonian Institution; the Systematic Entomology Laboratory (Agricultural Research Service, United States Department of Agriculture); and the Walter Reed Biosystematics Unit (Walter Reed Army Institute of Research). The specimens were imaged in a mass-digitization project in collaboration with the Digitization Program Office. The goal was to digitize every Bombus specimen in the collection.  

## Initial Data Collection and Normalization 

Bumblebee specimens were collected over a period of 150 years (earliest specimen dates from 1807, most recent specimen dates from 2020). The specimens were collected by and identified by many different individual researchers over this time. The initial images of about 49,000 specimens were taken in a rapid capture project by a dedicated team in 2014 with additional specimen images (about 25,000) taken in 2018. The labels containing the information on site/location, date of collection, collector, and identifier were removed from the insect pin. The occurrence data were transcribed from the labels by online volunteers and a professional transcription service into Darwin Core fields. Following quality control of the transcribed data by NMNH staff, they were imported into the institutional database (EMu). 

NMNH specimen data get exported to the Global Biodiversity Information Facility (GBIF) on a weekly basis through an installation of an Integrated Publishing Toolkit (IPT, https://collections.nmnh.si.edu/ipt/). Some data transformation takes place within EMu and GBIF likewise normalizes the data to meet their standards.  

 
## Who are the source language producers? 

The occurrence data were produced by humans, observed and written onto paper labels over the museum’s history, and then transcribed from paper labels pinned with the specimens upon collection. 


## Annotations 

The specimen occurrence data in Darwin Core fields. 

## Annotation process 

The occurrence data were transcribed from the labels by online volunteers and a professional transcription service into Darwin Core fields. 

## Who are the annotators? 

Original collectors and identifiers were entomologists and researchers from the Smithsonian and other institutions. Collectors may not be bumblebee specialists. For data transcription, online volunteers and professional transcription service workers. Demographic data of transcribers is unknown.  

## Personal and Sensitive Information 

The dataset contains the names of the collectors and identifiers.  

## Social Impact of Dataset 

Digitized natural history collections have the potential to be used in diverse research applications in evolutionary biology, ecology, and climate change.  

The dataset contains records for species listed on the U.S. Endangered Species List: Bombus affinis, Bombus franklini, and Bombus terricola. 

Some site/location names could cause harm as they are insensitive or racist towards indigenous communities. 

## Discussion of Biases 

Estimates of species geographic ranges based on these data may not be complete. There are many reasons collectors may collect more frequently from some areas rather than others, including their own taxonomic interests, proximity to collections institutions, accessibility via roads, ability to acquire permits for a specific area, or for geopolitical reasons. 

The majority of specimens in this dataset originate from North America.  

Most specimens are expected to be female, because bumblebees are social insects and it is more common to find female bees. 

## Other Known Limitations 

As with all natural history collections data, there is the potential that some metadata are inaccurate or inconsistent given that they have been collected and recorded over the course of the past 150 years. Smithsonian staff seek to correct these errors as they are identified but the dataset as presented is a snapshot in time. 

Species identifications may be inaccurate or not up-to-date based on the latest classification.  

Collector names may not be consistent across records (e.g. the same person’s name may be written differently). For women’s names, which were often historically recorded as Mrs. <spouse’s name>, only the spouse’s name may appear. 

Locality data may use historical place names that are no longer used. 

Dates may sometimes have been recorded by original collectors inconsistently or may be incomplete (no month/day information). 

For specimens collected from Brazil, specimen images are not included in the dataset. 

For endangered species, locality data is not included in the dataset. 

## Dataset Curators 

Smithsonian National Museum of Natural History, Department of Entomology. 

Jessica Bird (Data Manager in the Department of Entomology) is the main contact person for the dataset. 

## Licensing Information 

Public domain, Creative Commons CC0. 

## Citation Information 

Orrell T, Informatics Office (2023). NMNH Extant Specimen Records (USNM, US). Version 1.72. National Museum of Natural History, Smithsonian Institution. Occurrence dataset. https://collections.nmnh.si.edu/ipt/resource?r=nmnh_extant_dwc-a&v=1.72


## Contributions 

Thanks to NMNH for adding this dataset. 
