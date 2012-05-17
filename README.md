chnorm
======

Chnorm is a simple command line utility which makes one able to set the owner, group and the mode of the given files and directories on a per file / per directory basis, recursively. It is especially useful if you often copy files with braindead permission from filesystems not supporting the Unix permission scheme. chnorm detects executables based on their contents and sets their permissions accordingly.

```
$ ./chnorm 
Usage: chnorm [OPTION]... [FILE]...
Change the permissions of directories and files distinctively.
chnorm 0.4 is released under the GPLv3, hosted at https://github.com/mondalaci/chnorm

Options:
  --version             show program's version number and exit
  -h, --help            show this help message and exit
  -f FILEMODE, --file-mode=FILEMODE
                        set octal mode FILEMODE for files (default is 644)
  -d DIRMODE, --dir-mode=DIRMODE
                        set octal mode DIRMODE for directories (default is
                        755)
  -o OWNER, --owner=OWNER
                        set owner OWNER for every file and directory
  -g GROUP, --group=GROUP
                        set group GROUP for every file and directory
  -e, --exec-detect     detect executable files based on their content and
                        filename and set them executable accordingly [default]
  -n, --no-exec-detect  do not detect executable files based on their content
                        and filename and do not set them executable
                        accordingly
  -v, --verbose         verbose operation
```