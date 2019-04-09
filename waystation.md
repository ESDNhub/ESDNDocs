

# Importing records into repox via an Omeka instance (waystation)


## Overview

Most institutions provide their records to ESDN via direct OAI feed.
There are some institutions that cannot provide an OAI feed for
wahtever reason. Often in this case, we use an installation of Omeka
Classic as an intermediate. By importing a comma separated values file
into the Omeka instance, we can then harvest the institution's records
from Omeka into our repox installation. We have used this approach
successfully with a number of institutions. I'll use one of the
largest collections in repox, the Museum of Modern Art's Artworks
collection, as an example here.


## MoMA Example

-   They publish their collection data on Github in a number of formats
-   They provide 2 main data sets, Artists and Artworks
-   We work with the  Artworks data in CSV (comma separated values) format
-   We pull the most recent revision of the repo and load the Artworks.csv file into [OpenRefine](http://openrefine.org)
    -   We remove a number of fields that are irrelevant to our mapping
    -   Since we want records that point back to a page on MoMA's site, we strip out all records lacking a URL field
-   We then export the cleaned data back to a new CSV
-   We use [Csv Import Plus](https://github.com/Daniel-KM/Omeka-plugin-CsvImportPlus), a fork of the standard Omeka CSV import plug-in
    -   It is considerably more flexible, but the main advantage is that it accepts larger import files
        -   We import the new CSV into an existing MoMA collection in Omeka
        -   We map the URL field as the unique identifier
        -   We set the importer to update the record if it exists and create a new one if it doesn't
-   Once the data is imported, we look it over in the waystation for problems
-   We then harvest the collection from Waystation into repox via OAI

