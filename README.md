# ddnotes - drop down notes

DDNotes opens a drop down terminal window to edit your notes.

![notes](https://raw.githubusercontent.com/umurgdk/ddnotes/master/screenshots/notewindow.png)

## Features

* Listing notes with dmenu
* Creating new notes with dmenu
* Open/Hide last opened note with `ddnotes last`

## Dependencies

* `xdotools`
* `wmutils`
* `dmenu`
* `bash`
* An editor application which supports setting custom window titles. Most of the terminal emulators are supporting custom titles with a custom command to run (e.g vim). Otherwise this script should be able to work with GUI applications too.

## Usage

Right now the terminal emulator is hardcoded in the script, so you have to change it yourself by editing the file. You need to make sure the editor application (e.g terminal emulator) can be run with custom title argument. ddnotes depending on custom window titles.

```bash
$ mkdir ~/notes

# Show a list of notes with dmenu to open or create
$ ddnotes

# Open/Toggle the last opened note window
$ ddnotes last

# Open ddnotes with different notes folder
$ NOTES_DIR=$HOME/secret/notes ddnotes
```

### Configuring `i3wm`

You need to configure `i3wm` to always keep note windows as floating. This way this script can change to size and position freely. Since I don't know the configurations of other tiling window managers please checkout their documentations to how to define floating rules for windows.

Add this line to your i3 configuration file. If you want to keep borders delete the part `border none`

```
for_window [title="^notes:"] floating enable border none
```

## Screenshots

![listing](https://raw.githubusercontent.com/umurgdk/ddnotes/master/screenshots/listing.png)
![create new](https://raw.githubusercontent.com/umurgdk/ddnotes/master/screenshots/create-new.png)
