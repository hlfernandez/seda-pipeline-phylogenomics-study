# Protocol for a phylogenomics study [![license](https://img.shields.io/github/license/pegi3s/seda-pipeline-phylogenomics-study?style=flat-square)](https://github.com/pegi3s/seda-pipeline-phylogenomics-study) [![dockerhub](https://img.shields.io/badge/Docker%20Hub-7289da.svg?style=flat-square)](https://hub.docker.com/r/pegi3s/seda-pipeline-phylogenomics-study) [![github](https://img.shields.io/badge/GitHub-7289da.svg?style=flat-square)](https://github.com/pegi3s/seda-pipeline-phylogenomics-study)

A [SEDA](https://www.sing-group.org/seda/) pipeline created in [Compi](https://www.sing-group.org/compi/) that implements the ["Protocol for a phylogenomics study"](https://www.sing-group.org/seda/manual/protocols.html#protocol-for-a-phylogenomics-study) SEDA-based protocol. Created using the [SEDA-Compi pipelines framework](https://github.com/sing-group/seda-compi-pipelines).

This protocol shows how to retrieve files and prepare datasets to be used in detailed phylogenomics studies. The given example concerns the use of mitochondrial genomes to pinpoint the most likely phylogenetic relationship between Rosaceae species, using a [concatenated sequence approach](http://doi.org/10.1002/jez.b.21026).

# Quick-start: running the pipeline with sample data

Download [this ZIP](https://static.sing-group.org/software/pegi3s/seda-pipeline-phylogenomics-study/sample-working-dir.zip) and decompress it. The path where it is extracted will be referred as "working directory" (`/path/to/working_dir`).

Then, move to the working directory and simply run `./run.sh "$(pwd)"` to execute the entire pipeline with the provided input files.

The input data for this protocol can be also obtained at [NCBI](https://www.ncbi.nlm.nih.gov/nucleotide/), by querying Rosaceae [Organisms] AND complete genome mitochondrion on the search field. After, download each mitochondrial genome individually, selecting Coding sequences in the Send to: option, and choosing the FASTA Nucleotide file type. Please note that some species have more than one mitochondrial genome data available, and some of the genomes may present an UNVERIFIED prefix. To avoid redundant or misleading data, the use of the most recent genome available and the exclusion of unverified datasets are highly advisable.

To run specific tasks an additional parameter can be passed to the `run.sh` script: `./run.sh "$(pwd)" "--single-task clustal-align"` or `./run.sh "$(pwd)" "--until clustal-align"`.

# Applying the protocol to other case studies

Applying the protocol to other case studies is easy, you only need to:

1. Put the protein FASTA files at `input/rename-header-multipart_1/`.
2. Edit the `params/*.sedaParams` in case you need to tune the operations parameters for your case study. These files can be also created and exported using the SEDA GUI.

# Contributors

<a href="https://github.com/pegi3s/seda-pipeline-phylogenomics-study/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=pegi3s/seda-pipeline-phylogenomics-study" />
</a>

<sup>Made with [contrib.rocks](https://contrib.rocks).</sup>
