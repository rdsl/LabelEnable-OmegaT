# LabelEnable-OmegaT
Bash scripts providing labelling functionality to OmegaT projects.

## Author
Ramiro Duarte Simões Lopes

## Files
- makelabel (*creates label directory structure.*)
- initproject (*initializes translation project directory.*)

## Latest Version
[LabelEnable-OmegaT at GitHub](https://github.com/rdsl/labelenable-omegat)

## Licensing
Please, see LICENSE file.

## Overview

These two simple scripts allow you to easily reuse translation memories and
glossaries in OmegaT according to user-defined labels.

## How to use

All your OmegaT translation projects must reside in a folder named "project".
The LabelEnable scripts must reside in the parent folder of "project". A folder
named "label" will be created in this same directory. You can use this folder
to browse your projects, glossaries and tm by label. The following directory
structure is created: label/$lang-pair/$label/{project,glossary,tm}

### Memories
Add a "label" directory to each translation project directory. The name of
every file in this directory will be used as a label.

### Glossaries
End the comment field of each glossary entry you wish to label
with #insertlabel. Only the file ./glossary/glossary.txt will be used.

### Run
- makelabel - to create the label directory and compile the glossaries.
- initproject projectpath - to add the apropriate translation memories and
glossaries to the project directory, based on the project's labels.

## Requirements
- Linux
- Translation projects must reside in a directory named "project".
- Scripts must reside in the parent folder of "project".
- Project names must be unique, guaranteed by above.
- Project names must not have spaces.
- Glossary file must be default (i.e. ./glossary/glossary.txt)
- Comment field in glossary entries must end with #insertlabel.
- Glossary entries must not have other "#" characters.
- Labels must not have spaces

## Warning
A "label" directory will be created in the directory where the scripts reside.
If you already have a directory or file named "label" it will be removed.
