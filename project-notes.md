## References
 - multiple bin in project: 
   https://doc.rust-lang.org/cargo/reference/cargo-targets.html#binaries
 - id3 gat crate:
   https://docs.rs/id3/latest/id3/

## Main tasks

### Read ID3 Tag from file and print it out.

Additional options:
 - file name as input parameter
 - file name from stdio (to allow pipe processing)
 - if selected file is a file - try to read ID3 tag, if it is directory read all files from it.
   Additional flag: recursively all sub directories or current directory only

### Update ID3 Tag in single file
 - manual update of single file
 - update via stdio or command line args

### Traverse whole music collection (all files) to read id3 tags
 - Select root directory and go through all subdirectories - whole tree
 - use config file for music directory and eventually exclusions

## Config
 - root directory for music files (overwritten by param)
 - use recursive flag by default (overwritten by param)
 - exclude/include directories or files, or file types
 - output format
 - output file (if not specified output to the screen)
 - all options present - on/off with commenting line '//'

After running above functionality every file found should produce a line on screen (stdio)
with values separated by commas - data from ID3 plus full filepath:
- full file path
- artist
- title
- record
- cd number
- number of CDs
- track number

- struct Config
- struct DataOutput
- struct ID3Data (set of tags I am using)