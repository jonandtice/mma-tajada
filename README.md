# La Tajada's MMA Stuff

This repository holds a collection of MMA ([Musical Midi Accompaniment](https://www.mellowood.ca/mma/)) grooves, songs, and patterns used by the author for his own practice purposes. They are shared here in the hopes that others may find them usefull.

## Installation

Except for the _songs_ folder (that can go wherever you want), the folders in here are meant to follow the same structure as the default distribution of mma. The folders in _lib_ (grooves) can go in mma's _lib_ folder and the folders in _includes_ (patterns) can go in mma's _include_ folder.

Usage and more detailed descriptions of the grooves, songs, and patterns are in each folder.

## MMA Tips for VS Code

I use VS Code to edit MMA files and I use _tasks_ in VS Code to run mma commands.

### Syntax Hilighting

See https://github.com/jonandtice/mma-support for my syntax hilighting plugin. This is my first plugin and improvements and suggestions are welcome.

### Running MMA Commands

See [.vscode/tasks.jason](https://github.com/jonandtice/mma-tajada/blob/master/.vscode/tasks.json) for how to use VS Code _tasks_ to run mma commands.
The two tasks are _play_ and _build_.

#### Play

Runs `mma -P $(relativeFile)` $(relativeFile) becomes the file the task is run from.

This depends on your default midi player being correctly configured in MMA's preferences. Suggestion is to add ```SetMIDIplayer fluidsynth -ni -a pulseaudio``` to the `~/.mmarc` file (which is one of the files mma uses to load configurations).

#### Build

Runs `mma ${relativeFile}` which generates a midi file.