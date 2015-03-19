**Incremental harvest workflow**

ESDN relies on [REPOX](http://sysresearch.org/repox/) (https://github.com/europeana/REPOX) for all aggregation and ingest processes for the collection and contribution of statewide cultural heritage metadata to DPLA. 

Each month, ESDN ingests data from [partner institutions](https://docs.google.com/spreadsheets/d/1fI3P8CwjNCQAS3-er9bQE6wl4W6LXOl9GTHnSIIIWn0/edit?usp=sharing), transforms that data using XSLT to a set of select [MODs](https://docs.google.com/spreadsheet/ccc?key=0AjuVASmQStk8dDBJS1VfUUpqZV8tb21HcFpMelFzdWc&usp=sharing) elements that have been aligned with the [DPLA MAP](http://dp.la/info/developers/map/), and then outputs that data to DPLA in a single [[OAI feed](http://repox.metro.org:8080/repox/OAIHandler?verb=ListRecords&metadataPrefix=mods)] - link to OAI mods output. 

*Schedule*

To insure that edits, additions and deletions to partner records are reflected in DPLA, we ingest partner data into REPOX monthly. The current partner ingest schedule is as follows (with "Week 1" referring to the first full week of each month):

Monthly schedule

Week 1 - M,T,W: New York Heritage

Week 2 - M,T: Hudson River Valley Heritage

Week 3 - M,T: METRO’s Digital Culture

Week 3 - W: Long Island Memories

Week 4 - M,T,W, Th: All other partners

*Workflow*

The workflow for harvesting in REPOX is very manual. There is currently no way to automate recurring ingests. Although REPOX appears to support scheduled incremental and full ingests, we have not been able to make that work. REPOX development is inactive at the moment and they have not announced plans for further development. For now, our harvest workflow is as follows:

1. Select data set to be reharvested.

2. Empty the selected data set.

3. Re-Ingest the data set.

4. Confirm transforms.

So, in practice, we do a full re-ingest of our partners data each month, as incremental harvests in REPOX are currently not possible.

We have found that emptying and reharvesting multiple data sets at the same time can cause stability issues with REPOX, so we harvest data sets one a time.

*Communication with partners*

ESDN maintains a shared spreadsheet detailing the harvest schedule and processes with our partners. At any time, partners can check the schedule to see the most recent and upcoming harvest dates. That schedule is managed manually by ESDN staff. Once we begin regularly scheduled ingests with DPLA, we will also include the most recent and upcoming DPLA harvest dates.

