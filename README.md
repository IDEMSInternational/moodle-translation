# moodle-translation

All courses stored in this repository can be used directly or a Moodle mbz file for the course content can be [requested by email](mailto:smborio@idems.international).

Full details on how to use this repo coming soon.

# Local setup

0. Make sure to have java installed (e.g. `apt-get install default-jre`)
1. Download [Okapi](https://okapiframework.org/binaries/main/) and extract it into the `okapi` folder
2. To extract strings of a file to XLIFF: Run `./okapi/tikal.sh -x [inputfile.xml] -sl en -tl fr -fc okf_xml@moodle.fprm`
	- In windows, run `okapi\tikal.exe` or similar instead
	- `-tl` specifies the target language
	- `-fc` specifies a file with rules to filter out only those XML tags whose content we are interested in. We can modify this file as appropriate, e.g. to include STACK tags
3. Reimport translated strings: TBD

# Options

## Okapi + Crowdin (see above)

- Requires import/export
	- cannot update existing courses
	- monolingual courses (unless extra scripting)
- Have to ensure configuration extracts the correct set of strings
- Does not play nicely with already existing `mlang` tags

## [Moodle local_coursetranslator](https://github.com/jamfire/moodle-local_coursetranslator)

- One page within moodle with all course strings and their status
- Not officially released plugin (see github issues and [plugin directory comments](https://tracker.moodle.org/browse/CONTRIB-8927))
- Allows for translation as the course is being developed
- Does not include text from quiz questions
	- May be reasonably easy to modify to make it work
- With more work could **possibly** be modified to generate/import json files with translation strings, for a potential crowdin integration

## [Moodle content translation plugin set](https://moodle.org/plugins/filter_translations)

- [Documentation](https://docs.moodle.org/311/en/Content_translation_plugin_set)
- Should show a symbol for every string in the course indicating its status (translated, untranslated, outdated translation)
- Allows for translation as the course is being developed
- Includes text from quiz questions etc (TODO: confirm)
- GO: Have been unable to successfully enable the plugin

# TODO

* SB to investigate crowdin integration further
* SB to check if crowdin works well with `*.xlf` files - It looks likt it is. The [Documentation](https://store.crowdin.com/xliff2.0) suggests it requires *.xliff files so will require testing.
* SB and GO to present options to DS for a decision
* SB to investigate content translation plugin set (maybe try to disable/uninstall `local_coursetranslator`)

# Questions

* How does STACK fit into this?
* How does importing back work and what are the limitations?
* With okapi we can automatically create copies of courses in different languages rather than multi-lingual courses. Is this OK or should we write scripts to create multi-lingual instead?