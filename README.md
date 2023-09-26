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
