# Release notes

#### v0.9.1 - 2019-11-13
Maintenance release:

:   * Add rule for coverage track in bigWig format (alignment module)
    * Merge basecall files (fastx) from list of filenames to avoid temporary files
    * Merge alignment files (bam) from list of filenames, handle systems ulimit with partial merges
    * Pin snakemake to version 5.5.2
    * Upgrade go in transcript container to 1.13.4

#### v0.9.0 - 2019-08-30
Main release:

:   * Add guppy_barcoder to workflows for sequence based demultiplexing
    * Improve singularity handling by auto-mounting raw data and reference folders
    * Document singularity user installation
    * Fix bug in demultiplexing rules when using singularity (issue [#5](https://github.com/giesselmann/nanopype/issues/5))
    * Fix merge of bam batches for many files
    * Fix wrong singularity paths in methylation module

#### v0.8.0 - 2019-07-01
Main release:

:   * Allow customization of runtime and memory requirements for cluster computing (env.yaml)
    * Update guppy_basecaller to version 3.1.5
    * Change guppy config from flow-cell/kit to cfg file
    * Fix guppy installation in Docker
    * Improve Docker installation and tutorial documentation

#### v0.7.0 - 2019-05-16
Development release:

:   * Update guppy_basecaller to version v3.0.3
    * Move guppy installation into separate directory
    * Fix demultiplexing rule raw data fetching
    * Add doc section on updating the pipeline
    * Minor documentation edits

#### v0.6.0 - 2019-04-30
Development release:

The output of nanopype >= v0.6.0 is **not** backwards compatible due to major changes in the output filesystem structure.

:   * Introduce tag-concept to re-run the same workflow under different conditions
    * Transparent demultiplexing with 'special' tags
    * Rules to clean up batch data
    * Enhance documentation on singularity usage
    * Include STRique version v0.3.0
    * Update Pychopper to version v0.5.0
    * Update guppy_basecaller to version v2.3.7


#### v0.5.0 - 2019-03-26
Development release:

The output of nanopype >= v0.5.0 is **not** backwards compatible due to major changes in the output filesystem structure.

:   * Rework alignment module to support sequence post-processing
    * Enable Pinfish package for isoform detection


#### v0.4.1 - 2019-03-15
Development release:

:   * Update guppy_basecaller to version v2.3.5


#### v0.4.0 - 2019-03-13
Development release:

Version 0.4.0 is the singularity and bulk-fast5 release.

:   * Setup singularity images for each module
    * Support both, .tar of single fast5 and bulk-fast5 of current MinKNOW versions
    * Enhance documentation details on installation and cluster usage


#### v0.3.0 - 2019-02-05
Development release:

The output of nanopype >= v0.3.0 is **not** backwards compatible due to major changes in the output filesystem structure.

:   * Fix guppy installation instructions to not overwrite existing library installations
    * Apply general output structure of *tool2/tool1/runs/runname.x* to all processing chains (see module documentation/tutorial for details).


#### v0.2.1 - 2019-01-28
Development release:

:   * Parse experimental Flappie methylation calls to bedGraph/bigWig
    * Detect bigWig coverage from wildcards without requiring config entry

Known issues:

:   * Installing guppy after flappie is overwriting a symlink to *libhdf5.so* causing the flappie basecaller to load a hdf5 library it was not linked to. This will be fixed in a future release by separating the libraries properly.


#### v0.2.0 - 2019-01-21
Development release:

:   * Nanopolish                v0.11.0
    * htslib                    v1.9
    * OpenBLAS                  v0.3.4

#### v0.1.0 - 2018-12-24
Initial release with tool versions (for development or untagged repositories, the master branch with the tested version in brackets is used):

:   * Bedtools                  v2.27.1
    * Samtools                  v1.9
    * UCSCTools
        * bedGraphToBigWig      v4
    * Flappie                   master (1.1.0-9ef4edf)
    * Minimap2                  v2.14-r883
    * GraphMap                  master (v0.5.2)
    * NGMLR                     v0.2.7
    * Sniffles                  v1.0.10
    * Deepbinner                v0.2.0

Manual installations of *albacore* and *guppy* can't be versioned. The pipeline was tested with albacore 2.3.3 and guppy 2.1.3.
