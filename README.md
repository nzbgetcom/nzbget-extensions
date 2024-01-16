# NZBGet extensions

## This repository contains a list of NZBGet extensions, which is used by the Extension manager to download and update them.

## If you want to add your extension to this list, you will need

 1. Create a new repository in the [nzbgetcom](https://github.com/nzbgetcom) organization with such name Extension-{YourExtensionName}.

 2. Add brief information about your extension in JSON format to the "extensions.json" file.

Example:

	{
		"name": "VideoSort",
		"homepage": "https://github.com/nzbgetcom/Extension-VideoSort",
		"displayName": "Video Sort",
		"version": "9.0.0",
		"author": "Andrey Prygunkov",
		"license": "GNU",
		"about": "Sorts movies and tv shows.",
		"url": "https://github.com/nzbgetcom/Extension-VideoSort/releases/download/v9.0/videosort-9.0-dist.zip"
	}

Contacts:
 - [luckedea](lucky@nzbget.com)
 - [phnzb](pavel@nzbget.com)
 - [dnzbk](denis@nzbget.com)