# Release Notes

<!-- MarkdownTOC autolink="true" bracket="round" -->

- [2019 March 14: Updated logic for generating mod files](#2019-march-14-updated-logic-for-generating-mod-files)
- [2019 January 28: GA](#2019-January-28-ga)

<!-- /MarkdownTOC -->

## 2019 March 14: Updated logic for generating mod files 
In this release, GoCenter has changed the logic of mod files generation. 
* GoCenter will no longer generate a populated go.mod file for Go projects that haven’t yet opted into modules and do not yet contain a go.mod file. Prior to this release, GoCenter was using a different approach to produce missing go.mod files, to achieve optimal reproducibility. However, after further discussion with the Go community, and considering that the initial approach may cause the go.mod file’s checksum to be different from what may have been recorded in a project’s go.sum before using GoCenter, GoCenter will now generate empty go.mod files for Go projects that haven’t yet opted into modules.
* As part of this release, go.mod files that were previously generated by GoCenter will be converted to be consistent with this new behavior.
* For Go projects that already have go.mod files, GoCenter will continue to keep these .mod files unchanged when processing them to be included in GoCenter.

## 2019 January 28: GA
* gocenter.io goes live!
* Basic ability to search for modules
* Basic ability to request new modules be added to GoCenter
* Basic ability to determine the status of a module/version



