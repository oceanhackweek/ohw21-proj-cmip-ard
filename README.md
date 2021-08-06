# ohw21-proj-cmip-ard
### An *OceanHackWeek21* project to learn & document examples of CMIP6 workflows, turning big climate projection data into useful inputs for modelling and analysis.

Goals of this project include building clean, well-commented Jupyter notebooks that document CMIP6 workflows for generating analysis ready datasets (ARD) for specific examples.  A stretch-goal for this project is to complete and publish examples, possibly in a [Pangeo Gallery](https://gallery.pangeo.io/repos/pangeo-gallery/cmip6/index.html)?

This effort will leverage all the great work across the Pangeo & other open-source communities and may include:<br>
- [cmip6_preprocessing](https://cmip6-preprocessing.readthedocs.io/en/latest/)<br>
- [xgcm](https://xgcm.readthedocs.io/en/latest/)<br>
- [regionmask](https://regionmask.readthedocs.io/en/stable/)<br>
- [intake-esm](https://intake-esm.readthedocs.io/en/latest/)<br>

### Use case #1: SST & surface nitrate projections for Arabian Sea ecological modelling
A **hypothetical** ecological model of the Arabian Sea includes basin averaged SST and surface nitrate as inputs.  Researchers would like to explore ecosystem responses to future climate change projections under both SSP1-2.6 and SSP5-8.5 scenarios.  A monthly timeseries through 2100, averaged over the Arabian Sea, is required from a range of CMIP6 models to start the effort, and ouput in a useful format for import into R is required.  Another useful final product would be regridding all models onto a common grid for further comparison.

Tasks:<br>
*0. What CMIP6 models should we include in our ensemble and why? How do they perform for our areas of interest and with what known biases? (Out of scope - especially for this hypothetical example - but a literature review might be the first step here)*
1. Loading SST and surface nitrate for your chosen CMIP6 multi-model ensemble *(in this case arbitrarily choose a few models only, keeping in mind hub memory limits)*
2. Visualise the spread of values across the multi-model ensembles for each scenario.
3. Do we need to de-drift each CMIP model and how?
4. Build an appropriate mask for computing the Arabian Sea spatially-averaged timeseries.
5. Generate the region-average timeseries considering appropriate weighting for each model's grid. Format the timeseries data in a useful, human readable way.

Stretch task:

6. Regrid the multi-model ensemble onto a single, common grid for further comparison.


### Other use cases?


