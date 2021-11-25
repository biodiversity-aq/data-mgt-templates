# Documentation for template

Use sampling event template if there is no taxon involved, use occurrence template when there  is an occurrence of an organism/taxon identification.

## Definition of fields with comments and examples

### Sampling event template

| Field | Definition (see more https://dwc.tdwg.org/terms/) | Comments | Examples |
|---|---|---|---|
| eventID | An identifier for the set of information associated with an Event   (something that occurs at a place and time). May be a global unique   identifier or an identifier specific to the data set. |   | INBO:VIS:Ev:00009375 |
| parentEventID | An identifier for the broader Event that groups this and   potentially other Events. |   | A1 (parentEventID to identify the main Whittaker Plot in nested   samples, each with its own eventID - A1:1, A1:2). |
| eventDate | The date-time or interval during which an Event occurred. For   occurrences, this is the date-time when the event was recorded. Not suitable   for a time in a geological context. | Mandatory field for OBIS. Recommended best practice is to use a   date that conforms to ISO 8601-1:2019. | 2020-10-31 |
| year | The four-digit year in which the Event occurred, according to the   Common Era Calendar. |   | 2008 |
| month | The integer month in which the Event occurred. |   | 10 |
| day | The integer day of the month on which the Event occurred. |   | 28 |
| eventTime | The time or interval during which an Event occurred. | Recommended best practice is to use a date that conforms to ISO   8601-1:2019. | 08:30:00 |
| timeZone | The time zone of recorded time or interval during which an Event   occurred. |   | UTC |
| samplingProtocol | The name of, reference to, or description of the method or   protocol used during an Event. |   |   |
| samplingEffort | The amount of effort expended during an Event. |   | 40 trap-nights, 10 observer-hours, 10 km by foot, 30 km by car |
| sampleSizeValue | A numeric value for a measurement of the size (time duration,   length, area, or volume) of a sample in a sampling event. | A sampleSizeValue must have a corresponding sampleSizeUnit.  | 5 for sampleSizeValue with metre for sampleSizeUnit. |
| sampleSizeUnit | The unit of measurement of the size (time duration, length, area,   or volume) of a sample in a sampling event. | A sampleSizeUnit must have a corresponding sampleSizeValue, e.g.,   5 for sampleSizeValue with metre for sampleSizeUnit. | minute, hour, day, metre, square metre, cubic metre |
| fieldNumber | An identifier given to the event in the field. Often serves as a   link between field notes and the Event. |   |   |
| decimalLatitude | The geographic latitude (in decimal degrees, using the spatial   reference system given in geodeticDatum) of the geographic center of a   Location. Positive values are north of the Equator, negative values are south   of it. Legal values lie between -90 and 90, inclusive. | Mandatory field for OBIS.  | -41.09834 |
| decimalLongitude | 	The geographic longitude (in decimal degrees, using the spatial   reference system given in geodeticDatum) of the geographic center of a   Location. Positive values are east of the Greenwich Meridian, negative values   are west of it. Legal values lie between -180 and 180, inclusive. | Mandatory field for OBIS.  | -121.17611 |
| geodeticDatum | The ellipsoid, geodetic datum, or spatial reference system (SRS)   upon which the geographic coordinates given in decimalLatitude and   decimalLongitude as based. |   | EPSG:4326 |
| countryCode | The standard code for the country in which the Location occurs. | Recommended best practice is to use an ISO 3166-1-alpha-2 country code. https://en.wikipedia.org/wiki/ISO_3166-1 | AQ |
| footprintWKT | A Well-Known Text (WKT) representation of the shape (footprint,   geometry) that defines the Location. A Location may have both a point-radius   representation (see decimalLatitude) and a footprint representation, and they   may differ from each other. |   | POLYGON ((10 20, 11 20, 11 21, 10 21, 10 20)) (the one-degree   bounding box with opposite corners at longitude=10, latitude=20 and   longitude=11, latitude=21) |
| footprintSRS | 	A Well-Known Text (WKT) representation of the Spatial Reference   System (SRS) for the footprintWKT of the Location. Do not use this term to   describe the SRS of the decimalLatitude and decimalLongitude, even if it is   the same as for the footprintWKT - use the geodeticDatum instead. |   | GEOGCS["`GCS_WGS_1984`", DATUM["`D_WGS_1984`",   SPHEROID["WGS_1984",6378137,298.257223563]],   PRIMEM["Greenwich",0], UNIT["Degree",0.0174532925199433]]   (WKT for the standard WGS84 Spatial Reference System EPSG:4326). |
| eventRemarks | Comments or notes about the Event. |   | After the recent rains the river is nearly at flood stage. |


### Occurrence template

| Field | Definition,   see https://dwc.tdwg.org/terms/ | Remarks | Example |
|---|---|---|---|
| occurrenceID | An identifier for the Occurrence (as opposed to a particular   digital record of the occurrence). In the absence of a persistent global   unique identifier, construct one from a combination of identifiers in the   record that will most closely make the occurrenceID globally unique. | Mandatory field for GBIF and OBIS, unique per record | urn:catalog:UWBM:Bird:89776 |
| institutionCode | The name (or acronym) in use by the institution having custody of   the object(s) or information referred to in the record. |   | RBINS |
| collectionCode | The name, acronym, coden, or initialism identifying the   collection or data set from which the record was derived. |   | EBIRD |
| catalogNumber | 	An identifier (preferably unique) for the record within the data   set or collection. |   | 2008.1334 |
| basisOfRecord | The specific nature of the data record. | Mandatory field for GBIF and OBIS, standard label only. This   column contains validation of vocabularies for basisOfRecord stated in   "vocabulary" sheet: PreservedSpecimen, FossilSpecimen, LivingSpecimen, HumanObservation, MachineObservation, MaterialSample, Occurrence| PreservedSpecimen |
| type | The nature or genre of the resource. |   |   |
| associatedReferences | A list (concatenated and separated) of identifiers (publication,   bibliographic reference, global unique identifier, URI) of literature   associated with the Occurrence. |   | Christopher   J. Conroy, Jennifer L. Neuwald. 2008. Phylogeographic study of the California   vole, Microtus californicus Journal of Mammalogy, 89(3):755-767. |
| eventID | An identifier for the set of information associated with an Event   (something that occurs at a place and time). May be a global unique   identifier or an identifier specific to the data set. |   |   |
| decimalLongitude | The geographic longitude (in decimal degrees, using the spatial   reference system given in geodeticDatum) of the geographic center of a   Location. Positive values are east of the Greenwich Meridian, negative values   are west of it. Legal values lie between -180 and 180, inclusive. | Mandatory field for OBIS. This column contains data validation.   Only decimal values of -180 and 180 are valid | 	-121.17611 |
| decimalLatitude | The geographic latitude (in decimal degrees, using the spatial   reference system given in geodeticDatum) of the geographic center of a   Location. Positive values are north of the Equator, negative values are south   of it. Legal values lie between -90 and 90, inclusive. | Mandatory field for OBIS. This column contains data validation.   Only decimal values of -90 and 90 are valid | 	-41.09834 |
| geodeticDatum | The ellipsoid, geodetic datum, or spatial reference system (SRS)   upon which the geographic coordinates given in decimalLatitude and   decimalLongitude as based. | Recommended best practice is to use the EPSG code of the SRS | EPSG:4326 |
| eventDate | The date-time or interval during which an Event occurred. For   occurrences, this is the date-time when the event was recorded. Not suitable   for a time in a geological context. | Mandatory field for OBIS. Recommended best practice is to use a   date that conforms to ISO 8601-1:2019. | 2020-10-31 |
| year | The four-digit year in which the Event occurred, according to the   Common Era Calendar. |   | 2008 |
| month | The integer month in which the Event occurred. |   | 10 |
| day | The integer day of the month on which the Event occurred. |   | 28 |
| eventTime | The time or interval during which an Event occurred. | Recommended best practice is to use a date that conforms to ISO   8601-1:2019. | 08:30:00 |
| timeZone | The time zone of recorded time or interval during which an Event   occurred. |   | UTC |
| samplingProtocol | The name of, reference to, or description of the method or   protocol used during an Event. |   | https://doi.org/10.1111/j.1466-8238.2009.00467.x |
|  occurrenceStatus | A statement about the presence or absence of a Taxon at a   Location. | Mandatory field for OBIS.  | Present |
| individualCount | The number of individuals represented present at the time of the   Occurrence. |   | 25 |
| organismQuantity | A number or enumeration value for the quantity of organisms. | A dwc:organismQuantity must have a corresponding   dwc:organismQuantityType. | 27 (organismQuantity) with individuals (organismQuantityType) |
| organismQuantityType | The type of quantification system used for the quantity of   organisms. | A dwc:organismQuantityType must have a corresponding   dwc:organismQuantity. | 12.5 (organismQuantity) with %biomass (organismQuantityType). |
| sex | The sex of the biological individual(s) represented in the   Occurrence. |   | female, male, hermaphrodite |
| lifeStage | The age class or life stage of the biological individual(s) at   the time the Occurrence was recorded. |   | egg, eft, juvenile, adult |
| behavior | The behavior shown by the subject at the time the Occurrence was   recorded. |   | roosting, foraging, running |
| occurrenceRemarks | Comments or notes about the Occurrence. |   | found dead on road |
| identifiedByID | A list (concatenated and separated) of ORCID of people, groups,   or organizations who assigned the Taxon to the subject. | Recommended best practice is to separate the values in a list   with space vertical bar space ( \| ). |   |
| dateIdentified | The date on which the subject was determined as representing the   Taxon. | Recommended best practice is to use a date that conforms to ISO   8601-1:2019. | 2007-11-13 (YYYY-MM-DD) |
| scientificName | The scientific name, without authorship and date information if   known. When forming part of an Identification, this should be the name in   lowest level taxonomic rank that can be determined. This term should not   contain identification qualifications, which should instead be supplied in   the IdentificationQualifier term. | Mandatory field for OBIS.  | Ctenomys sociabilis |
| scientificNameAuthorship | The authorship information for the scientificName formatted   according to the conventions of the applicable nomenclaturalCode. |   | (Györfi, 1952) |
| identificationQualifier | A controlled value to express the determiner's doubts about the   Identification. |   | aff. risso  |
| kingdom | The full scientific name of the kingdom in which the taxon is   classified. |   | Animalia |
| taxonrank | The taxonomic rank of the most specific name in the   scientificName. |   | genus |
| scientificNameAuthorship | The authorship information for the scientificName formatted   according to the conventions of the applicable nomenclaturalCode. |   | (Györfi, 1952) |
| scientificNameID | An identifier for the nomenclatural (not taxonomic) details of a   scientific name. | Mandatory field for OBIS.  | urn:lsid:ipni.org:names:37829-1:1.3 |

