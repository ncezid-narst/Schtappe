# Schtappe

Welcome to Schtappe, what is going to be a suite of Nextflow workflows created to address a variety of CDC/NCEZID/DFWED/EDLB/NARST Nanopore sequencing bioinformatics needs. Although Schtappe is intended for CDC users, the portable nature of Nextflow should allow for external users to easily adapt these workflows to their specific environments and/or needs. To facilitate that, all of the processes use Singularity containers.

As of 6/16/2023, the workflows currently available include:

* Stylo - Nanopore assembly workflow from basecalled reads to polished assembly plus assembly QC, metrics, and plasmid replicon detection
  * https://github.com/ncezid-narst/stylo
* Messer - Post-assembly small plasmid recovery and size correction workflow for nanopore sequence data
  * https://github.com/ncezid-narst/messer 
* Geteilt - NARST workflow built in nextflow. Pulls paired short-read data from NCBI using SRRs, and runs through read metrics, coverage cutoff, assembly, and AR, plasmid, and point-mutation screening
  * https://github.com/ncezid-narst/geteilt

## Future plans
Stylo: 
* Support for short-reads to run through Unicycler
* More param options for each process (ideally I guess all of them?)
* A barcode renaming script that will handle the read concatenating necessary to run the workflow
* CI

Geteilt:
* Update CG-PIPELINE with fasten container
* BATS testing
* CI

### Nextflow:
If you're unfamiliar with Nextflow or would like to just learn more, consider doing these free trainings found here: https://training.nextflow.io/
The Nextflow documentation is super helpful as well, especially to learn more about what process directives and profile configurations you can include in your local copy of `stylo.config`. An entire section is dedicated to just containers which should help troubleshoot any issues with Singularity or assist in using Docker instead. Nextflow documentation can be found here: https://www.nextflow.io/docs/latest/index.html

If you're a CDC user, you should register for Scicomp's Nextflow tutorials here: https://info.biotech.cdc.gov/info/training-portal-updated-tracks/
Or you can access the material directly here: https://training.biotech.cdc.gov/nextflow/

## Thanks
Special thanks to: 
* Jess Chen, Lee Katz, and Curtis Kapsak for their enthusiastic guidance and wealth of data science expertise
* Kaitlin Tagg and Hattie Webb for their encouragement and passion for plasmids that started this whole venture
* StaPH-B who are an indispensable resource for bioinformatics in public health
* Seqera whose workshop is a fantastic introduction to writing in Nextflow
* OpenAI - ChatGPT is an amazing tool for looking up documentation, especially when you're a bad coder

## Etymology
The names 'Schtappe', 'Stylo', 'Messer', and 'Geteilt' are all spells from a wonderful book series called Ascendance of a Bookworm by Miya Kazuki. Obviously, they're all German words. The meaning of the spells all somewhat capture their respective purposes. Do check it out.
