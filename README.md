# Jobs and Housing Site Selection Map

Live map: https://benram3737.github.io/site-selection-map

This map shows where new workforce housing would put the most people close to their jobs in Savannah, GA and St. Petersburg, FL. I compared where jobs are against where workers live, found the areas where the two are most out of balance, and scored 100 candidate housing sites on job access and available land.

## The markets

- **Savannah metro area:** 1,828 hexagons, 22 clusters and 31 candidate sites.
- **Pinellas County / St. Petersburg:** 1,322 hexagons, 23 clusters and 69 candidate sites.

Use the switch at the top of the page to move between the two.

## How it works

1. **Jobs versus housing.** I split each market into a hexagon grid and counted jobs in the target wage range against resident workers in that same range, using 2023 Census job data (LODES, the Census Bureau's Origin Destination Employment Statistics). Each hexagon is colored by the gap between the two:
   - Dark red: strong job surplus, more than 5,000 jobs over workers
   - Light red: job surplus, 1,500 to 5,000
   - Neutral: balanced, within 1,500 either way
   - Light blue: housing surplus, 1,500 to 5,000 more workers than jobs
   - Dark blue: strong housing surplus, more than 5,000
2. **Clusters.** I used Local Moran's I, a test for statistically significant hot spots, to find groups of hexagons that stand out together at p ≤ 0.05. Job clusters (solid red outline) are places with far more jobs than local workers, so those workers commute in from elsewhere. Housing clusters (dashed blue outline) are where those commutes start.
3. **Candidate sites.** Each green hexagon is a candidate site with a score from 0 to 100. Darker green scores higher. Click a site to see what is behind its score:
   - Jobs in the target wage range within 1 km
   - Jobs reachable by vanpool
   - Retail and food within 1 km
   - Largest obtainable parcel and number of obtainable parcels of 3 acres or more
   - Share of the hexagon that is restricted land
   - Public land flagged as available

## What "obtainable" means

Land figures come from county parcel records for parcels of 1 acre or more. A parcel counts as obtainable unless it belongs to a government, port, airport, rail, utility, school, public university, cemetery or religious owner. Housing authorities, land trusts and redevelopment agencies count as available rather than as obstacles. Owner names are withheld in this public version.

## Using the map

- **Layers:** turn the hexagon grid, clusters, candidate sites, labels, restricted land and available public land on or off.
- **Minimum site score:** drag the slider to hide sites below a score.
- **Candidates by score:** the list on the left ranks every site shown. Click one to fly to it on the map.
- **Clusters:** click any cluster outline to see its number of jobs, resident workers, housing gap and how far its workers commute.

## Built with

- QGIS for the spatial analysis
- Leaflet for the web map
- LODES 2023 job data and county parcel records

The whole map is one HTML file with the data built in, so it loads without a server. If you open the file on your own computer while online, you also get the option to switch on street, aerial and topographic basemaps.

One caution: the scores rank sites against each other within each market. Treat a high score as a reason to look closer at a site, not as a finished feasibility study.
