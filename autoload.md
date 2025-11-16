## About autoload
To automatically load elf files from internal `/data/elfldr/` or external USB `/mnt/usb0/elfldr/`\
It will read from USB, if not found then read from internal.\
if there is `autoload.cfg` file found, it will parse it and load defined elf files.\
if there is no `autoload.cfg` file found, no elf file will be load.

## autoload.cfg
Define an elf file per line\
`#` is used as comment\
`##wait` is special line for delay loading

For example `/data/elfldr/autoload.cfg`
```
#### ##wait [x]
#### wait x seconds (1 <= x <= 9)

# ftp server
##wait 1
ftpsrv.elf

# web server
##wait 1
websrv.elf
```
