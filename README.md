# ![MultiQC](docs/images/MultiQC_logo.png#gh-light-mode-only) ![MultiQC](docs/images/MultiQC_logo_darkbg.png#gh-dark-mode-only)

### Aggregate bioinformatics results across many samples into a single report

##### Find [documentation](http://multiqc.info/docs) and [example reports](http://multiqc.info/examples/rna-seq/multiqc_report.html) at [http://multiqc.info](http://multiqc.info)

[![PyPI Version](https://img.shields.io/pypi/v/multiqc.svg?style=flat-square)](https://pypi.python.org/pypi/multiqc/)
[![Conda Version](https://anaconda.org/bioconda/multiqc/badges/version.svg)](https://anaconda.org/bioconda/multiqc)
[![Docker](https://img.shields.io/docker/automated/ewels/multiqc.svg?style=flat-square)](https://hub.docker.com/r/ewels/multiqc/)
[![GitHub Workflow Status - Linux](https://img.shields.io/github/workflow/status/ewels/MultiQC/MultiQC%20-%20Linux?label=build%20-%20Linux&logo=ubuntu&logoColor=white&style=flat-square)](https://github.com/ewels/MultiQC/actions?query=workflow%3A%22MultiQC+-+Linux%22)
[![GitHub Workflow Status - Windows](https://img.shields.io/github/workflow/status/ewels/MultiQC/MultiQC%20-%20Windows?label=build%20-%20Windows&logo=windows&style=flat-square)](https://github.com/ewels/MultiQC/actions?query=workflow%3A%22MultiQC+-+Windows%22)

[![Gitter](https://img.shields.io/badge/gitter-%20join%20chat%20%E2%86%92-4fb99a.svg?style=flat-square)](https://gitter.im/ewels/MultiQC)
[![DOI](https://img.shields.io/badge/DOI-10.1093%2Fbioinformatics%2Fbtw354-lightgrey.svg?style=flat-square)](http://dx.doi.org/10.1093/bioinformatics/btw354)

---

MultiQC is a tool to create a single report with interactive plots for multiple bioinformatics analyses across many samples.

MultiQC is written in Python (tested with v3.6+). It is
available on the [Python Package Index](https://pypi.python.org/pypi/multiqc/) and through conda using [Bioconda](http://bioconda.github.io/).

Reports are generated by scanning given directories for recognised log files.
These are parsed and a single HTML report is generated summarising the statistics
for all logs found. MultiQC reports can describe multiple analysis steps and
large numbers of samples within a single plot, and multiple analysis tools making
it ideal for routine fast quality control.

A very large number of Bioinformatics tools are supported by MultiQC. Please see the MultiQC website for a [complete list](https://multiqc.info/#supported-tools).

MultiQC can also easily parse data from custom scripts, if correctly formatted / configured.
See the [MultiQC documentation](http://multiqc.info/docs/#custom-content) for more information.

Please note that some modules only recognise output from certain tool subcommands.
Please see the [module documentation](http://multiqc.info/docs/#multiqc-modules) for more information.

More modules are being written all of the time. Please suggest any ideas as a new
[issue](https://github.com/ewels/MultiQC/issues) _(include an example log file if possible)_.

## Installation

You can install MultiQC from [PyPI](https://pypi.python.org/pypi/multiqc/)
using `pip` as follows:

```bash
pip install multiqc
```

Alternatively, you can install using [Conda](http://anaconda.org/)
from the [bioconda channel](https://bioconda.github.io/):

```bash
conda install -c bioconda multiqc
```

If you would like the development version instead, the command is:

```bash
pip install --upgrade --force-reinstall git+https://github.com/ewels/MultiQC.git
```

MultiQC is also available via [Galaxy](https://usegalaxy.org/) ([Toolshed](https://toolshed.g2.bx.psu.edu/view/iuc/multiqc/9a913cdee30e), [Galaxy wrapper](https://github.com/galaxyproject/tools-iuc/tree/master/tools/multiqc)).

## Usage

Once installed, you can use MultiQC by navigating to your analysis directory
(or a parent directory) and running the tool:

```bash
multiqc .
```

That's it! MultiQC will scan the specified directory (`.` is the current dir)
and produce a report detailing whatever it finds.

The report is created in `multiqc_report.html` by default. Tab-delimited data
files are also created in `multiqc_data/`, containing extra information.
These can be easily inspected using Excel (use `--data-format` to get `yaml`
or `json` instead).

For more detailed instructions, run `multiqc -h` or see the
[documentation](http://multiqc.info/docs/#running-multiqc).

## Development

MultiQC has been written in a way to make extension and customisation as easy as possible.
The documentation has a large section describing how to [code with MultiQC](https://multiqc.info/docs/#coding-with-multiqc) and you can find an example plugin at [https://github.com/MultiQC/example-plugin](https://github.com/MultiQC/example-plugin).

Pull-requests for fixes and additions are very welcome.
Please see the [contributing notes](https://github.com/ewels/MultiQC/blob/master/.github/CONTRIBUTING.md) for more information about how the process works.

## Citation

Please consider citing MultiQC if you use it in your analysis.

> **MultiQC: Summarize analysis results for multiple tools and samples in a single report.** <br> _Philip Ewels, Måns Magnusson, Sverker Lundin and Max Käller_ <br>
> Bioinformatics (2016) <br>
> doi: [10.1093/bioinformatics/btw354](http://dx.doi.org/10.1093/bioinformatics/btw354) <br>
> PMID: [27312411](http://www.ncbi.nlm.nih.gov/pubmed/27312411)

```BibTeX
@article{doi:10.1093/bioinformatics/btw354,
 author = {Ewels, Philip and Magnusson, Måns and Lundin, Sverker and Käller, Max},
 title = {MultiQC: summarize analysis results for multiple tools and samples in a single report},
 journal = {Bioinformatics},
 volume = {32},
 number = {19},
 pages = {3047},
 year = {2016},
 doi = {10.1093/bioinformatics/btw354},
 URL = { + http://dx.doi.org/10.1093/bioinformatics/btw354},
 eprint = {/oup/backfile/Content_public/Journal/bioinformatics/32/19/10.1093_bioinformatics_btw354/3/btw354.pdf}
}
```

## Contributions & Support

Contributions and suggestions for new features are welcome, as are bug reports!
Please create a new [issue](https://github.com/ewels/MultiQC/issues) for any
of these, including example reports where possible. MultiQC has extensive
[documentation](http://multiqc.info/docs) describing how to write new modules,
plugins and templates.

There is a chat room for the package hosted on Gitter where you can discuss
things with the package author and other developers:
<https://gitter.im/ewels/MultiQC>

If in doubt, feel free to get in touch with the author directly:
[@ewels](https://github.com/ewels) (phil.ewels@scilifelab.se)

### Contributors

Project lead and main author: [@ewels](https://github.com/ewels)

There are a lot of other code contributors though!
See the [Contributors Graph](https://github.com/ewels/MultiQC/graphs/contributors) for details.

MultiQC is released under the GPL v3 or later licence.
