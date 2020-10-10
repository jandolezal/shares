# Bioenergy from Eurostat's SHARES database

Data from the tsv tables accessed from the [Energy database](https://ec.europa.eu/eurostat/web/energy/data/database) under energy indicators as 'Share of energy from renewable sources until 2020' (nrg_ind_share). Three tsv tables for each sector (electricity, heating and cooling, transport).
* Use of renewables for transport - details (nrg_ind_urtd)
* Use of renewables for electricity - details (nrg_ind_ured)
* Use of renewables for heating and cooling - details (nrg_ind_urhcd)

**Last interation is in the notebook shares_eu_tidier.ipynb and the directory eu_tidy.**

Three of the output csv files are a tidier version of the Eurostat data. The rest is pivot tables for biofuels for each country and year.

Very helpful is the [Standard international energy product classification (SIEC)](http://dd.eionet.europa.eu/vocabulary/eurostat/siec/) vocabulary and the [Energy balance](http://dd.eionet.europa.eu/vocabulary/eurostat/nrg_bal/) vocabulary.

## Fuels
Biomass-based fuels I cover here (SIEC codes in brackets):
* Primary solid biofuels (R5110-5150_W6000RI)
* Biogases (R5300)
* Liquid biofuels (R5200)
* Renewable municipal waste (W6210)

Other fuels we care about:
* Renewables and biofuels (RA000)
* Total (TOTAL)

## Variables
If I understand it correctly in the SHARES database in the **electricity sector** I should look for 'Gross electricity generation' for biomass-based fuels, in the **heating sector** it seems as a sum of 'Final consumption in industry and others sectors' and 'Gross heat production' and in the **transport sector** the variables are probably 'Final consumption' variable for road, rail and other sectors.

Depending on the sector (electricity, heating and cooling, transport) we are interested in the following variables:

### Electricity
* Gross electricity production - Renewable Energy Directive (GEP_RED)

### Heating and cooling
* Gross heat production - Renewable Energy Directive (GHP_RED)
* Final consumption - industry and other sectors - energy use (FC_IND_OTH_E)

### Transport
* Final consumption - other transport sector- energy use - Renewable Energy Directive (FC_TRA_OTH_E_RED)
* Final consumption - transport sector - road - energy use - Renewable Energy Directive (FC_TRA_ROAD_E_RED)
* Final consumption - transport sector - rail - energy use - Renewable Energy Directive (FC_TRA_RAIL_E_RED)

Disclaimer: I might got something wrong. I still have to go through the whole [Energy balance guide](https://ec.europa.eu/eurostat/documents/38154/4956218/ENERGY-BALANCE-GUIDE-DRAFT-31JANUARY2019.pdf/cf121393-919f-4b84-9059-cdf0f69ec045). I hope I do not aggregate variables which should be kept separate or miss some variable to add it to the bioenergy totals.
