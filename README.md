# Bioenergy from Eurostat's SHARES database

Analysis of 'Share of energy from renewable sources until 2020' (nrg_ind_share) from the tsv tables in the [Energy database](https://ec.europa.eu/eurostat/web/energy/data/database) - energy indicators.

Eurostat publishes three tsv tables for each sector (electricity, heating and cooling, transport).
* [Use of renewables for electricity - details](https://ec.europa.eu/eurostat/estat-navtree-portlet-prod/BulkDownloadListing?file=data/nrg_ind_ured.tsv.gz) (nrg_ind_ured)
* [Use of renewables for heating and cooling - details](https://ec.europa.eu/eurostat/estat-navtree-portlet-prod/BulkDownloadListing?file=data/nrg_ind_urhcd.tsv.gz) (nrg_ind_urhcd)
* [Use of renewables for transport - details](https://ec.europa.eu/eurostat/estat-navtree-portlet-prod/BulkDownloadListing?file=data/nrg_ind_urtd.tsv.gz) (nrg_ind_urtd)

These Jupyter nootebooks serve to tidy the original data (from tsv) and obtain few variables relevant for bioenergy in the EU as csv files for further use elsewhere.

In the folder 'selection' are data for a selected set of countries (AT, CZ, DK, NL, PL, SK). 

The 'eu' folder contains tables covering all countries from the SHARES database. 

Notebooks in the 'eu/tidy' folder build on the original tsv tables, which were made tidier (variables from the energy balances vocabulary moved from rows to columns).
