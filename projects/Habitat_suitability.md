
---
layout: default
title: Habitat Suitability
---

[← Back to portfolio](https://kward-alt.github.io/)


# Comparing habitat suitability under climate change for Sorghastrum nutans between Kansas and Illinois

In this project I look at the habitate suitability of Sorghastrum nutans (Indiangrass) under four different climate projections at two different sites in the US. 

## Indiangrass overview

I selected Sorghastrum nutans (Indiangrass), a native warm-season perennial bunch grass (i.e., grows in clumps) common in tallgrass and mixed-grass prairie systems across much of the central and eastern contiguous United States. It is typically found in open grasslands, prairie restorations (or land reclaimation projects), fallow farmland, and especially where periodic fire limits woody encroachment. There are two sites of interest for this project: Illinois and Kansas.

Geographic range is broad in CONUS, but persistence is strongest in intact prairie landscapes. Main pressures that disrupt indiangrass include conversion to agriculture/urban land cover (the primary driver of indiangrass loss), fragmentation (also due to human activity), woody encroachment from fire suppression, and climate-driven loss due to moisture stress. Since moisture stress is important I focus on precipation as my climate variable in this project.
Benefits of indiangrass

The loss of indiagrass harms both ecosystem services and native species that rely on it. For example, indiangrass provides substantial ecological value:

    - It is used as nesting material and escape cover for grassland birds (Brakie, 2017)
    - Their seeds provide additional nutrition for grassland birds (Brakie, 2017)
    - It provides grazing for buffalo and for livestock (Brakie, 2017)

## The role of fire

Walker (1991) also notes that fire disturbance is important to the persistence or lacktherof of indiangrass. Fire has historically maintained tallgrass prairie, and indiangrass is repeatedly characterized as fire tolerant through postfire sprouting from rhizomes. Walker (1991) also notes controlled burns (particularly late spring burns in many tallgrass systems) have been observed to support the proliferation of the species. In restoration and conservation practice, indiangrass is widely used for prairie reconstruction, conservation cover, and erosion control from wind and rain. It is typically planted in mixtures with other warm-season grasses to rebuild tallgrass habitats (Brakie, 2017).

## Key traits and characteristics
**Key traits** [Brakie, 2017; USDA, n.d.]
- Trait: [Indiangrass typical range / value]
- Height (culms): [~1–2.5 m (3–8 ft)]
- Leaf blade width: [~5–10 mm (to ~12 mm reported in some materials)]
- Flowering window: [Mid‑summer to fall; often ~Jul–Oct across the range (earlier north, later south)]
- Seed mass: [~1.9–2.0 g per 1,000 seeds (≈1.9–2.0 mg per seed; method-dependent)]
- Season: [C4 (warm-season)]
- Lifespan: [Perennial; productive seed stands commonly reported ~10–15 years under managed production]
- pH range: [4.8-8.0]
- Precipitation: [11-45 inches]
- Root depth: [24 inches minimum]
- Salinity toleranace: [Medium]
- Shade tolerance: [High]

#### Note: there are also cultivars of Indiangrass that have different traits, but for the purpose of this project I am just referring to the primary species in the PLANTS database.

# The project

To evaluate habitat suitability under climate change, I use:

- **Soil pH (POLARIS, 60-100 cm)** as an edaphic control. I use 60-100cm due to the root depth of Indiangrass.
- **Slope** (derived from SRTM) as a topographic constraint (flatter prairie landscapes are generally more suitable). However the two sites I review in this project are both mostly flat to hilly (Kansas and Illinois).
- **Annual precipitation** climate normal (MACAv2) as the primary climate driver for this C4 grass. Since the plant is sensitive to precipitation I thought this would be a somewhat good substitution for the lack of fire regime data in the model.

**Core question:** How does projected mid-century climate change (relative to a historical baseline) alter suitable habitat for S. nutans across contrasting prairie-region sites in CONUS [Kansas v. Illinois], and how sensitive are results to climate-model uncertainty?

**Sites:**
- Tallgrass Prairie National Preserve, Kansas [referred to as Tallgrass in the notebook]
- Midewin National Tallgrass Prairie, Illinois [referred to as Midewin in the notebook]

<src="/img/site_maps.png" width="600" height="600">

*Figure 1* Locations of and boundaries of Tallgrass and Midewin sites

## The Last "Stand" or the Tallgrass Prairie National Preserve, Kansas

The National Park Service notes that "tallgrass prairie once covered 170 million acres of North America...[but] today less than 4% remains intact, mostly in the Kansas Flint Hills." [National Park Service, n.d.; National Preserve Kansas]

As such the Flint Hills tallgrass landscape has a relatively intact prairie and strong fire-grazing ecological dynamics. This site makes for good comparison to Illinois where that has been mostly a restoration project not a conservation project.

We can also see in the Kansas map that the surrounding area is also unfragmented and not interrupted by other land cover, namely built environments.

## From Munitions to Grass? The Midewin National Tallgrass Prairie, Illinois

The Illinois site is a large restoration project. As noted by the U.S. Forestry Service (n.d.), the site "[Turns] back the clock from a landscape dominated by rusting munitions factories and abandoned ammunitions bunkers into a 20,283-acre pristine tallgrass prairie." They go one to embellish that this, "makes the Midewin a compelling vision for landscape scale restoration."

Of course, we know that this site is not pristine especially if it was previously a significantly disturbed site by a different form of "fire."

Noteably, the Illinois site is very different from the Kansas site. The area around Midewin are very developed and there is a lot of fragmentation.

**Expected suitability**

I expect both sites to remain at least mostly suitable because S. nutans is broadly distributed across the U.S., and based on its traits, seems to establish itself well as long as woody invasives are managed. Similarly, both sites are (seemingly) cared for due to the threatened status of indiangrass. However, I do expect greater climate-model spread in projected suitability at Midewin (IL) because it is a more fragmented site, and may be more sensitive to precipitation-seasonality shifts. Tallgrass (KS) should remain comparatively strong since this habitat has been preserved and not disturbed by ammunition.

## Applying climate models
In order to to do climate projections on these two sites, two different timeframes are required for modeling or "climate normals." For the purposes of my project I use the following: 

- Historical baseline: 1981-2010 (MACAv2 historical scenario)
- Mid-century future: 2041-2070 (MACAv2 RCP8.5 scenario)

This pair should provide a good baseline and future modeling comparison. However, the two sites should likely be modeled with their own independent set of time periods (even though that doesn't allow for comparison then). I say this because the Tallgrass (KS) site was established in 1996 and has been preserved for 30 years now so the habitat is more stable. In comparison the Midewin (IL) site was "established" in 1996, but due to the reclamation process, was not actually finished until 2004. That is almost a decade of difference between the two sites in terms of establishment.

## Climate models used

This analysis uses four global climate models (GCMs). These models simulate future climate under the RCP8.5 emissions scenario and are commonly used to capture uncertainty across different climate projections.

**Models Used:**

1. CanESM2 (Canada) [best fit for warm & wet]
- Developed by: Canadian Centre for Climate Modelling and Analysis
- Type: Earth system model (includes carbon cycle feedbacks)
- General traits:
  - Often shows warmer and wetter futures
  - Can "produce" strong vegetation and ecosystem responses
    - Why included:
      - Represents a higher-sensitivity climate response
      - Because I am using precipitation and soil ph this model may provide a good assessment for Indiangrass (can handle dry and wet years)

2. CNRM-CM5 (France) [best fit for more "moderate" conditions]
- Developed by: Centre National de Recherches Météorologiques
- Type: Coupled atmosphere–ocean model
- General traits:
  - Typically produces moderate warming signals
  - Often considered middle-of-the-road among CMIP5 models
    -Why included:
      - Serves as a baseline / moderate scenario
      - Since Indiangrass is established across much of the U.S. a more "intermediate" scenario could suit it better since it seems to thrive pretty much anywhere that it gets established (and not crowded out by woody species)

3. HadGEM2-ES (United Kingdom) [best fit for warm & dry]
- Developed by: Met Office Hadley Centre
- Type: Earth system model (includes atmospheric chemistry + carbon cycle)
  = General traits:
    - Often projects strong warming and drying in some regions
    - Captures complex land–atmosphere interactions
      - Why included:
        - Represents perhaps the most reasonable model for the two sites in the future, as both Kansas and Illinois are getting warmer but not wetter (CanESM2)

4. inmcm4 (Russia) [best for counterfactual cooler & dry]
- Developed by: Institute of Numerical Mathematics
- Type: Coupled climate model
  - General traits:
    - Often shows lower climate sensitivity
    - Produces more conservative (muted) changes
      - Why included:
        - Provides a more conservative projection
        - I thought it would provide an interesting contrast to the other models since Indiangrass does not have a high cold tolerance

## Soil data
I pulled the soil data from the POLARIS dataset based on the PLANTS database criteria I specified earlier in the indiangrass introduction. Since the minimum depth of roots for indiangrass is 24 inches, I am using the 60 to 100 cm depth in POLARIS. 24 inches is approximately 60 cm and since it is the minimum, the 60cm to 100cm depth is most suitable.

<src="/img/soil_ph_maps.png" width="600" height="600">

*Figure 2* The deep dark blue areas on these maps are water (especially for the Midewin site), which I also confirmed via google earth. I expect there is a lot of fertilizer run off in these areas as there is both agriculture and built environments near these sites. We can see across these maps that beyond water sources, the rest of the landscape meets the pH range for Indiangrass as we expected (4.8-8.0).

## Topographic data
I also plotted the topographic data or slopes of these sites. As one would expect from Kansas and Illinois they do not have very heterogenious elevations (e.g. mountains).

<src="/img/topography_maps.png" width="600" height="600">

*Figure 3* Based on the gradual change in elevation (in meters), we can see that both of these sites feature gentle hills with the Tallgrass site being more clearly hilly (low of 370 meters above sea level to a high of 450) where as the Midewin site has a west to east hill (low elevation of 165 meters to 205 meters). This means the lower areas of the sites will be wetter which we should also see highlighted in the climate modeling. 

## Climate model data 

I used MACAv2-METDATA daily downscaled climate projections to characterize precipitation (pr) and computed 30-year climate normals by averaging annual precipitation totals over each target period. MACAv2 provides statistically downscaled climate data at ~4 km resolution, derived from CMIP5 global climate models and bias-corrected using historical observations.

In order to project these models I use fuzzy logic modeling. Fuzzy logic modeling is a useful approach for climate projection analysis because it allows environmental variables to be treated as gradual suitability conditions rather than strict yes/no thresholds. Instead of classifying either of my locations as simply “suitable” or “unsuitable,” fuzzy logic assigns each variable, such as precipitation, temperature, slope, or soil conditions, a membership score between 0 and 1 based on how closely it matches an ideal range. These scores can then be combined to estimate overall suitability under historical and future climate scenarios. 

For our modeling we can see some basic information on habitat quality (HSI) first before plotting the habitate suitability. 

<src="/img/mean_hsi.png" width="600" height="600">

*Figure 4* Summary table of HSI at both sites

*Midewin (IL)*
- Historical to Future Mean HSI: 0.866 → 0.824
  - So between time periods a little bit of a drop.
- Suitable area: 47% → 47%
  - Really did not change much at all.

*Tallgrass (KS)*
- Historical to Future Mean HSI: 0.836 → 0.833
  - Very little change in Kansas.
- Suitable area: 45% → 45%
  - Seemingly no climate change effects for the Kansas Preserve

It is important to note that this is the suitability within the bounds of the preserve. It does not mean that indiangrass is not more suitable in other areas of Kansas or Illinois. The HSI is stable over time, and roughly 50% of each site remains a good fit for the species. Importantly the habitat quality (HSI) stays stable over time.

What is interesting is that under climate change we would expect northern sites to do better, but Illinois fair marginally worse than Kansas. Kansas may just be in the south-north range sweet spot for indiangrass even under projected precipitation stress.

**Considering what the climate models show**
We can also consider how HSI would change under each of the selected climate models. 

<src="/img/change_HSI_model.png" width="600" height="600">

*Figure 5* Summary table of HSI change at both sites under the different climate models. 

From this table we can see that CanESM2 (warmer and wetter) has a worse outcome for the Midewin, IL site (a total change or delta hsi of a little more than 10%) whereas there is no effect at the Tallgrass, Kansas site. Even under a moderate warming scenario (CNRM-CM5) the Midewin site struggles. In comparison the Tallgrass site is seemingly impervious to any projected climate effects. As a result, the Midewin site is more sensitive/vulnerable to both moderate warming, and warmer + wetter scenarios. As the CanESM2 projection is the most severe, we will plot that.  


<src="/img/hsi_maps_CanESM2.png" width="600" height="600">
*Figure 6* A plot of the two sites under the CanESM2 scenario. As we already knew from the delta HSI, the Midewin site fairs far worse across the entire extent of the prairie. 

## Key takeaway

Climate change produces very modest declines in habitat quality (HSI) at Midewin, while the overall extent of suitable habitat remains largely stable across both sites (above 50%). Tallgrass Prairie (KS) remains highly stable, while Midewin (IL) shows slightly greater sensitivity to future conditions.

## Larger analysis

Across both sites, the fuzzy model indicates that habitat suitability for _Sorghastrum nutans_ remains consistently high under both historical (1981–2010) and future (2041–2070) climate conditions (precipitation). Mean habitat suitability values are slightly higher under historical conditions and decline modestly in future projections, particularly at the Midewin National Tallgrass Prairie site.

At Midewin, mean HSI decreases from approximately 0.87 to 0.82, indicating a measurable reduction in overall habitat quality. However, the percentage of area classified as suitable remains nearly unchanged (~47%), suggesting that while conditions become somewhat less optimal, most of the landscape remains above the suitability threshold. This pattern indicates a within-class decline in suitability, rather than a large-scale loss of suitable habitat.

In contrast, the Tallgrass Prairie site shows minimal change between historical and future conditions. Mean HSI values remain nearly constant (~0.84), and suitable area also remains stable (~45%). This suggests that Tallgrass Prairie is relatively robust to projected mid-century climate changes, at least under the variables included in this model.

Compared to earlier iterations of this analysis (re:boundarygate), differences across climate models are less pronounced. This reflects improvements in spatial processing, including the use of official site boundaries and more consistent raster alignment. As a result, I believe the updated outputs provide a more stable and realistic estimate of habitat suitability.

## Quanitfying change over time due to model differences

Although earlier runs suggested strong model disagreement—particularly at the Midewin site—the updated results indicate more consistent outcomes across models. Rather than large divergences, the primary pattern is a modest decline in mean suitability at Midewin and near-complete stability at Tallgrass.

This suggests that projected climate impacts on _Sorghastrum nutans_ habitat are relatively subtle at the spatial scale of this analysis. The results emphasize that changes in habitat quality may occur without large changes in total suitable area.

For example in the pivot table, examining model-specific changes in habitat suitability reveals that the CanESM2 model (warm + wet projection) produces the largest declines in HSI at both sites. This is expected since my climate variable was precipitation. In contrast, the HadGEM2 model (often characterized as warmer and drier) shows little to no change in suitability.

I first thought that drier conditions should to reduce habitat suitability more strongly. However, I have to think how the model thinks, so this pattern reflects the structure of the fuzzy model, which is primarily driven by precipitation rather than temperature. In this framework, increases in precipitation beyond the optimal range can reduce suitability just as much as decreases below it. As a result, the “warm + wet” scenario produces larger declines because it pushes conditions outside the modeled optimal precipitation window, whereas the “warm + dry” scenario may still fall within acceptable bounds even if we know the US will experience warming.

## Limitations

I used a compact fuzzy rule set (soil pH, slope, precipitation) and did not include disturbance regime (e.g., fire/grazing), land use, or dispersal constraints, so the maps represent only potential climatic suitability.

Additionally, while official administrative boundaries were used to improve spatial accuracy, these boundaries do not perfectly correspond to ecological prairie extent. Therefore, the results and plots I have should be interpreted as approximate representations of site-level suitability rather than precise delineations of habitat.

## More grass digging--Why is the grass not *greener* on the other site

The biggest limitation, based on the literature, is actually the inability of my fuzzy model to capture fire ecology. As mentioned in the introduction at the beginning of this notebook, fire suppression may negative effect indiangrass because it allows intrusion by woody species. This is important because as Walker (1991) states, "The maintenance of the tallgrass prairie before European settlement was largely due to the occurrence of fire. In the absence of fire, invasion by woody species is common [12]. Without periodic fires Indiangrass declines in terms of reproductive effort and relative cover [32]. Indiangrass survives fire by sprouting from on-site surviving rhizomes." (FIRE ECOLOGY OR ADAPTATIONS).

Because fire regime is not included in my model, these results reflect climatic suitability only and may underestimate the importance of disturbance processes in maintaining high-quality habitat. This would be important to model because Walker (1991) makes it clear that fire is good for this species and can rebound quickly depending on the season. Noteably annual burns are important. I am including the excerpt from the section PLANT RESPONSE TO FIRE

    Indiangrass density and apparent vigor [17,22], number of flowering
    culms [9,38,45], and percent canopy and basal cover [5,57] increase with
    late spring burning conducted prior to green-up.  Burning during other
    seasons may increase flowering stems [38] or decrease percent
    composition of Indiangrass [72].  The greatest increase in canopy cover,
    density, production, and flowering occurs following annual burns
    [2,25,44,45].  Seeds are generally absent in burned soils, and most
    reproduction following fire is vegetative [2].  Fire intensity affects
    short-term rhizome reproduction.  Late summer fires (September 5th) were
    conducted with both high-intensity and low-intensity fuels.  Little or
    no damage occurred on the low-intensity fuel area, but tiller densities
    were reduced on the high-intensity fuel area.  However, tiller density
    returned to normal by the following August. (Walker, 1991).

It would be interesting to model the affects of changing fire regimes, especially as humans try to tamp down on fires as much as possible. **My hypothesis is that: Kansas is less densely populated than Illinois, which may allow for more frequent use of prescribed fire and fewer constraints on fire management. In contrast, more developed landscapes in Illinois may limit the use of fire as a management tool, potentially influencing habitat conditions for fire-dependent species.** If we look at the site plots from early with the topo basemaps, the Illinois site is encircled by built environments, so I imagine the likelihood of prescribed burns is very low compared to Kansas.

### References

Brakie, M. 2017. Plant Guide for Indiangrass (Sorghastrum nutans). USDA-Natural Resources Conservation Service, East Texas Plant Materials Center. Nacogdoches, TX 75964. https://www.nrcs.usda.gov/plantmaterials/etpmcpg13196.pdf

Climate Toolbox model-selection resources and MACA model comparison tools (https://climatetoolbox.org)

National Park Service. n.d. National Preserve Kansas. https://www.nps.gov/tapr/index.htm U.S. Forestry Service. n.d. Midewin National Tallgrass Prairie. https://www.fs.usda.gov/r09/midewin

USDA. n.d. Sorghastrum nutans (L.) Nash. PLANTS database. https://plants.sc.egov.usda.gov/plant-profile/SONU2/characteristics

Walkup, Crystal J. 1991. Sorgastrum nutans. In: Fire Effects Information System, [Online]. U.S. Department of Agriculture, Forest Service, Rocky Mountain Research Station, Fire Sciences Laboratory (Producer). Available: https://www.fs.usda.gov/database/feis/plants/graminoid/sornut/all.html [2026, March 23].






