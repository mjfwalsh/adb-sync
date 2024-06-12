# adb-sync
This project originally started out as a patch of Google's [adb-sync](https://github.com/google/adb-sync/) but then morphed into a completely different program. Thanks to toybox, this version of adb-sync is considerably faster than Google's!

### Differences
* This program only accepts one source folder and one destination folder.
* It doesn't try to copy rsync's [trailing slash behaviour](https://serverfault.com/questions/529287/rsync-creates-a-directory-with-the-same-name-inside-of-destination-directory). The contents of the source and destination folders are synced. The source folder itself is never copied into the destination folder.
* File and directories can be excluded from sync by using wildcards, eg `--exclude '.*'`
* Unicode normalisation is performed on MacOS filenames.

### Requirements
* A working [adb command](https://www.xda-developers.com/install-adb-windows-macos-linux/) on you pc.
* An Android device which [adb debugging enabled](https://developer.android.com/studio/debug/dev-options).
* An Android device which a reasonably recent version of [toybox](https://github.com/landley/toybox) (>= 0.8.1).
* Python 3

### Installation
* Just copy the script to somewhere in your path

### Usage
* Run `adb-sync --help`
