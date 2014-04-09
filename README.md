Adopted from [Craig Emery's dotfiles](http://github.com/craigemery/dotFiles)

# Vim Ctags AutoTag

Updates the tags file for the current vim session when saving a file. This is done by walking up the directory tree from the file saved, looking for the generated ctags file. When the file is found all entries for the saved file are removed and then the ctags amend command is called, thus updating the entries for the saved file.

## Optional configurations for .vimrc

```
let g:autotagmaxTagsFileSize=<number>   " Max tags file size to strip (Default: 1024*1024*7)
let g:autotagExcludeSuffixes=<suffixes> " Does not run ctags when saving files with these extensions. ('.' separated list, Default: ".tml.xml.txt.txt")
let g:autotagVerbosityLevel=<level>     " Logging verbosity (as in Python logging module, Default: logging.WARNING)
let g:autotagCtagsCmd=<cmd>             " Name of ctags command (Default: "ctags")
let g:autotagTagsFile=<filename>        " Name of the generated tag file (supports ".git/tags" as recommended by many ctags/vim blogs, Default: "tags")
let g:autotagStopAt=<directory>         " Stops walking up the directory tree at this directory and make one (Default: $HOME)
let g:autotagDisabled=1                 " Disables autotaging on file save (Default: 0)
```
