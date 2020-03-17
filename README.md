# Frank!Manual

This project documents the Frank!Framework for software integration. The Frank!Framework itself is hosted on GitHub at https://github.com/ibissource/iaf. The audience for this manual about the Frank!Framework is developers, testers and system administrators. Please read this manual on http://frank-manual.readthedocs.io to learn more about the Frank!Framework.

This project contains restructured text files with explanations and Frank configs that complements these explanations. Restructured text files are plain text files with extension .rst. These files should be processed by the Sphinx tool to produce the formatted manual. This is achieved using the website http://www.readthedocs.io. This GitHub repository has a Git hook pointing to that site, triggering an automated build each time a commit is added. The result can be read at https://frank-manual.readthedocs.io/.

The Frank configs that complement the explanations have three purposes. First, Frank configs are provided as the solutions of tutorials. Some sections of the manual request the reader to create a Frank config and try it. These sections provide a download link for the expected result. Second, editors of the manual should check statements about the Frank!Framework using examples. These examples also appear within this git project. Finally, system administrators and testers need to work with the Frank!Framework without writing Frank configs themselves. Tutorials for testers and system administrators therefore provide Frank configs to exercise with.

Here is the directory structure:

    frank-manual: The checkout directory.
    |- docs: Files processed by ReadTheDocs.
       |- make.bat: Build script for Windows.
       |- Makefile: Read by UNIX tool "make", used bo build the Frank!Manual with Linux.
       |- source: reStructuredText source files.
          |- conf.py: Sphinx configuration file.
          |- index.rst: Top-level documentation text file, references other .rst files.
          |- gettingStarted: Sub-directory with .rst files and images.
          |- testing: Other sub-directory with .rst files and images.
          |- ...
          |- build: Not checked in. Holds the result of building the Frank!Manual with make.bat or Makefile.
          |- downloads: Download zip files, generated by buildDownloadZips.py. Checked in.
          |- snippets: Snippets to include, generated by TutorialSteps. Checked in.
    |- src: Subdirectory with complementing Frank code. Not processed by TutorialSteps.
    |- srcSteps: Snapshots of Frank configs, processed by TutorialSteps.
    |- generateAll.py: Runs buildDownloadZips.py and TutorialSteps.
    |- buildDownloadZips.py: Script to builds .zip files for download links in manual. Do not call this directly.
    |- buildDownloadZips.txt: Configuration file for buildDownloadZips.py.
    |- createSnippets.py: Calls TutorialSteps. Do not call this script directly.
    |- TutorialSteps: Python module to create .rst include files (snippets). See CONTRIBUTING.md.
    |- README.md: This README file.
    |- CONTRIBUTING.md: Explains how to contribute to this manual.
    |- buildspec.yml: It is not clear whether this file is really needed.

To contribute to this project, see CONTRIBUTING.md
