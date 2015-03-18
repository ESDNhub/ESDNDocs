Much of our process at Empire State Digital Network is driven by our
being a new hub that is just starting with DPLA. As a result, we are
not repurposing data at this time. We act as a simple conduit between
our providers and DPLA. We have plans for further presentation or
hosting of provider data in future, but this is what our process looks
like at the moment.

1. We harvest metadata from our partners via OAI-PMH into REPOX. So
   far, the majority of our partners have been CONTENTdm sites
   providing oai_dc. We do have at least one provider (METRO, our host
   organization) that is providing MODS via Islandora. As we grow and
   add providers we expect to deal with a wider variety of formats and
   CMSes.
2. In REPOX we write XSL stylesheets to transform the data to ESDN and
   DPLA MAP compliant MODS.
3. DPLA harvests compliant MODS from us via OAI-PMH via REPOX.
4. Profit! I mean, our providers appear in DPLA.

Since we are still waiting on our first ingest to be complete, we have
not yet had to deal with a number of issues like incremental
harvesting and the like.
