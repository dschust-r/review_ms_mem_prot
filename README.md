## Community review on "Advances in Mass Spectrometry for Membrane Protein Pharmacology"

<!-- usage note: edit the H1 title above to personalize the manuscript -->

[![HTML Manuscript](https://img.shields.io/badge/manuscript-HTML-blue.svg)](https://dschust-r.github.io/review_MS_mem_prot/)
[![PDF Manuscript](https://img.shields.io/badge/manuscript-PDF-blue.svg)](https://dschust-r.github.io/review_MS_mem_prot/manuscript.pdf)
[![GitHub Actions Status](https://github.com/dschust-r/review_MS_mem_prot/workflows/Manubot/badge.svg)](https://github.com/dschust-r/review_MS_mem_prot/actions)

Please check the links ^^^ for the current version of the manuscript. 

<!-- usage note: edit this section. -->
# Review information

**Purpose.**
We are writing a community review, intended to summarize recent advances in the field of protein mass spectrometry. 
This review focuses on novel technologies and biological insights on membrane proteins, relevant for pharmacological research and is intended to be pulished in the Cell journal [Trends in Pharmacological Sciences (TIPS)](https://www.cell.com/trends/pharmacological-sciences/home). We will be using [Manubot](https://github.com/manubot/manubot) to write this manuscript and track changes. See below for guidelines on how to use Manubot.

The review was inspired by a [collaborative tutorial on proteomics](https://github.com/jessegmeyerlab/proteomics-tutorial) that was initiated by Jesse G. Meyer and became a great resource for anyone interested in mass spectrometry-based proteomics. 

**Authorship.**
I (Dina Schuster) will be leading the project and will ultimately decide the author order based on contributions recorded via GitHub. For this project, I am looking for a total of **4 additional co-authors**, ideally experts in the field of protein mass spectrometry and/or pharmacology of membrane proteins. The minimum contribution is one section, including relevant references. I do take the freedom to correct sections and make changes where necessary. Figures and tables will also be counted towards contributions. 

**TIPS guidelines.**

1. Ensure that the topic is introduced adequately so that non-experts can follow easily.
2. TIPS Reviews are typically shorter than others in the field. They stand at around **3500 words** at submission, with 80-100 references.
3. Keep most references **within the last 4 years**.
4. **The number of elements allowed for Reviews is a maximum of 6.** This includes Tables, Figures and Text Boxes.
5. Text boxes are typically used by authors to explain a sub-topic within the review, that might require more background for a non-expert/ expert from another field to understand. These are used many times by authors to expand the word limit of the review as the words inside do not count towards the 3500 word limit.
6. The use of a Glossary is encouraged. This is a collection of definition of terms that are used in the field but which a student/early learner/ expert from another field might not know.
7. The last section is a “Conclusions and Future Perspectives”. This section briefly lays out what the article covered, then discusses Outstanding Questions in the field (once that would ideally be answered in the next 5 years) before concluding the narrative. This is the place for authors to opine/hypothesize how they see the field developing too. Please put the Outstanding Questions that are discussed in this section as bullet points in a separate document called “Outstanding Questions” and call this document out in the main text by stating “(See Outstanding Questions)”.
8. Figures should be designed via Biorender. Please let me know if you do not have a license.

## How to contribute:


## Manubot

<!-- usage note: do not edit this section -->

Manubot is a system for writing scholarly manuscripts via GitHub.
Manubot automates citations and references, versions manuscripts using git, and enables collaborative writing via GitHub.
An [overview manuscript](https://greenelab.github.io/meta-review/ "Open collaborative writing with Manubot") presents the benefits of collaborative writing with Manubot and its unique features.
The [rootstock repository](https://git.io/fhQH1) is a general purpose template for creating new Manubot instances, as detailed in [`SETUP.md`](SETUP.md).
See [`USAGE.md`](USAGE.md) for documentation how to write a manuscript.

Please open [an issue](https://git.io/fhQHM) for questions related to Manubot usage, bug reports, or general inquiries.

### Repository directories & files

The directories are as follows:

+ [`content`](content) contains the manuscript source, which includes markdown files as well as inputs for citations and references.
  See [`USAGE.md`](USAGE.md) for more information.
+ [`output`](output) contains the outputs (generated files) from Manubot including the resulting manuscripts.
  You should not edit these files manually, because they will get overwritten.
+ [`webpage`](webpage) is a directory meant to be rendered as a static webpage for viewing the HTML manuscript.
+ [`build`](build) contains commands and tools for building the manuscript.
+ [`ci`](ci) contains files necessary for deployment via continuous integration.

### Local execution

The easiest way to run Manubot is to use [continuous integration](#continuous-integration) to rebuild the manuscript when the content changes.
If you want to build a Manubot manuscript locally, install the [conda](https://conda.io) environment as described in [`build`](build).
Then, you can build the manuscript on POSIX systems by running the following commands from this root directory.

```sh
# Activate the manubot conda environment (assumes conda version >= 4.4)
conda activate manubot

# Build the manuscript, saving outputs to the output directory
bash build/build.sh

# At this point, the HTML & PDF outputs will have been created. The remaining
# commands are for serving the webpage to view the HTML manuscript locally.
# This is required to view local images in the HTML output.

# Configure the webpage directory
manubot webpage

# You can now open the manuscript webpage/index.html in a web browser.
# Alternatively, open a local webserver at http://localhost:8000/ with the
# following commands.
cd webpage
python -m http.server
```

Sometimes it's helpful to monitor the content directory and automatically rebuild the manuscript when a change is detected.
The following command, while running, will trigger both the `build.sh` script and `manubot webpage` command upon content changes:

```sh
bash build/autobuild.sh
```

### Continuous Integration

Whenever a pull request is opened, CI (continuous integration) will test whether the changes break the build process to generate a formatted manuscript.
The build process aims to detect common errors, such as invalid citations.
If your pull request build fails, see the CI logs for the cause of failure and revise your pull request accordingly.

When a commit to the `main` branch occurs (for example, when a pull request is merged), CI builds the manuscript and writes the results to the [`gh-pages`](https://github.com/dschust-r/review_MS_mem_prot/tree/gh-pages) and [`output`](https://github.com/dschust-r/review_MS_mem_prot/tree/output) branches.
The `gh-pages` branch uses [GitHub Pages](https://pages.github.com/) to host the following URLs:

+ **HTML manuscript** at https://dschust-r.github.io/review_MS_mem_prot/
+ **PDF manuscript** at https://dschust-r.github.io/review_MS_mem_prot/manuscript.pdf

For continuous integration configuration details, see [`.github/workflows/manubot.yaml`](.github/workflows/manubot.yaml).

## License

<!--
usage note: edit this section to change the license of your manuscript or source code changes to this repository.
We encourage users to openly license their manuscripts, which is the default as specified below.
-->

[![License: CC BY 4.0](https://img.shields.io/badge/License%20All-CC%20BY%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by/4.0/)
[![License: CC0 1.0](https://img.shields.io/badge/License%20Parts-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

Except when noted otherwise, the entirety of this repository is licensed under a CC BY 4.0 License ([`LICENSE.md`](LICENSE.md)), which allows reuse with attribution.
Please attribute by linking to https://github.com/dschust-r/review_MS_mem_prot.

Since CC BY is not ideal for code and data, certain repository components are also released under the CC0 1.0 public domain dedication ([`LICENSE-CC0.md`](LICENSE-CC0.md)).
All files matched by the following glob patterns are dual licensed under CC BY 4.0 and CC0 1.0:

+ `*.sh`
+ `*.py`
+ `*.yml` / `*.yaml`
+ `*.json`
+ `*.bib`
+ `*.tsv`
+ `.gitignore`

All other files are only available under CC BY 4.0, including:

+ `*.md`
+ `*.html`
+ `*.pdf`
+ `*.docx`

Please open [an issue](https://github.com/dschust-r/review_MS_mem_prot/issues) for any question related to licensing.
