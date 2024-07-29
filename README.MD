This is a fork of SonLVL that makes it compatible with 64x64 chunks and word-sized entries in the layout file

List of changes:
- Added the changes in Devon's pull request, allowing for chunk flipping
- SonLVL now uses words to store chunks rather than bytes
- Fixed bug with 64x64 chunks where the window would be one chunk short
- Chunk editor is zoomed in by 2x

Things I'd like to change or see changed in the future:
- Allow for the limiting of the number of bytes the layout can take up when layouts are much larger than the expected 0x1000 bytes (currently trying to enable this creates a crash)
- Allow the Usage Counts window to be open without preventing the use of the program
- Allow SonLVL to be closed without use of task manager after clicking "continue" after a crash while loading a level
- Improvements to importing
  - When there are two of the same color in a palette line and one is transparent, give priority to the color that isn't transparent
  - Option to disable specific colors/palette lines during import process rather than have to modify the colors manually beforehand and then reset them
  - Default to collision FF when there is no collision rather than 00
  - Do more checks for mirroring blocks when no valid collision block is detected
- Have "remove duplicates" function ignore differences in palette for tile 0 and collision for block 0
- Allow files to be loaded individually rather than requiring project files
- Allow chunk, block, and tile edits to be undone/redone
- When multiple tile, block, or chunk files are loaded (e.g. Green Hill Zone, Sonic 3 & Knuckles), put them in separate categories
  - Allow catagories to be added, removed, or merged
- Add tabs in the layout editor for blocks and tiles. Clicking on a block or tile will highlight it in the layout