# sar-data
 Data on Species at Risk assessment and listing timelines

The Species at Risk Public Registry (https://www.canada.ca/en/environment-climate-change/services/species-risk-public-registry.html) contains important information on wildlife species in Canada that are at heightened risk of extinction or extirpation. Crucially, information on this website about species assessment and listing histories can inform conclusions on how efficiently endangered species are being assessed, listed, and protected. We used web scraping to extract and compiled all relevant assessment and listing timeline data for every species on the registry, which we store here. We hope that this resource can help those interested in conserving biodiversity in Canada with understanding patterns in assessment and listing timelines of at-risk Canadian wildlife.

The "all_species_dates" CSV file contains this information and the date in the filename reflects the date at which these data were last updated. The file includes the following data fields:
- species: English name of the species or population, as per the Species at Risk registry.
- tax_group: The taxnomic group containing this taxon. One of "Mammals (terrestrial)", "Mammals (marine)", "Birds", "Amphibians", "Reptiles", "Fishes (freshwater)", "Fishes (marine)", "Molluscs", "Arthropods", "Vascular Plants", "Mosses", and "Lichens". This is relevant because certain aquatic species (Fishes, Molluscs, and marine mammals) have an additional 12 months for their assessments to be processed.
- cosewic_status: The status most recently assessed by COSEWIC for this taxon. Typically one of "Not at Risk", "Special Concern", "Threatened", "Endangered", "Extirpated", or "Extinct".
- sara_status: The taxon's current protection under the Species at Risk Act. Typically one of "Not on Schedule 1" (i.e., no protections), "Special Concern", "Threatened", "Endangered", "Extirpated", or "Extinct".
- url: The URL corresponding to the individual species page on the Species at Risk registry, where relevant information on assessment timelines can be found.
- flag_any: A Boolean variable ("True" or "False") indicating whether or not the species has exceeded its assessment timeline.
- flag_2017: A Boolean variable ("True" or "False") indicating whether or not the most recent ministerial Response Statement was issued for this taxon after January 1, 2017, after which point the established timelines should be obeyed.
- max_lag_gic: The maximum time lag from the Ministerial Response Statement to the Governor-in-Chief (GiC) receipt, in days.
- last_response_statement: The date of the most recent Response Statement from the Minister for this taxon.
- date_##, doc_type_##: A series of documents (either "COSEWIC Assessment", "(Ministerial) Response Statement", "Consultation Period Begin", "Consultation Period End", "GiC Receipt (of assessment)", "GiC Listing Decision") and their associated dates.