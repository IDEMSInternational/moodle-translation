# moodle-translation

All courses stored in this repository can be used directly or a Moodle mbz file for the course content can be [requested by email](mailto:smborio@idems.international).

Full details on how to use this repo coming soon.

# Local setup

0. Make sure to have java installed (e.g. `apt-get install default-jre`)
1. Download [Okapi](https://okapiframework.org/binaries/main/) and extract it into the `okapi` folder
2. To extract strings of a file to XLIFF: Run `./okapi/tikal.sh -x [inputfile.xml] -sl en -tl fr -fc okf_xml@moodle.fprm`
	- In windows, run `okapi\tikal.exe` or similar instead
	- `-tl` specifies the target language
	- `-fc` specifies a rule that filters out only those XML tags whose content we are interested in. We can modify this file as appropriate.
3. Reimport translated strings: TBD

# Options

## Crowdin
pros and cons?

## Moodle local_coursetranslator
pros and cons?

## Moodle content translation plugin set
pros and cons?

# TODO
* SB to investigate crowdin integration further
* SB to check if crowdin works well with *.xlf files
* SB and GO to present options to DS for a decision
* SB to investigate content translation plugin set

# Questions
* How does STACK fit into this?
* How does inporting back works and what are the limitations?
* With okapi we can automatically create copies of courses in different languages rather than multi-lingual courses. Is this OK or should we write scripts to create multi-lingual instead?