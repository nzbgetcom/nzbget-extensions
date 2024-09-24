## NZBGet extensions

This repository contains a list of NZBGet extensions, which is used by the Extension manager to download and update them.

## If you want to add your extension to this list, you will need

1. Make your extension compatible with NZBGet spec v23+. 
[Documentation](https://github.com/nzbgetcom/nzbget/blob/develop/docs/extensions/EXTENSIONS.md).

2. Make sure that yours extension repository contains the required and possibly optional workflows:

Mandatory:
- Prospector Python Static Analysis check
- Manifest check

Optional:
- Tests check (availability of tests is highly recommended)
- Release workflow

Reusable workflows can be used from the current repository, an example of use is in the Example extensions repository (see below).

3. Once your extension is ready, please contact NZBGet maintainers to get it added into the extension manager.
We will create a fork of your extension repository, mirror your release to include it in the extension manager, and make a PR to that repository.

## Example extension (can be used as quickstart):

https://github.com/nzbgetcom/Extenson-Example

Demonstrates:
- Using extension parameters
- Using Tests
- Using workflows:
    - Prospector check
    - Manifest check
    - Tests check
    - Release workflow

## Questions
You can use [issues](https://github.com/nzbgetcom/nzbget/issues) for any questions.

## Maintainers:
 - [luckedea](https://github.com/luckedea)
 - [phnzb](https://github.com/phnzb)
 - [dnzbk](https://github.com/dnzbk)
