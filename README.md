# xsibackup-snroll
(c)XSIBackup Snapshot Roll

This Bash script allows to set a predefined number of snapshots per virtual machine. 
Just try the script on the command line and then call it from the ESXi crontab.
It can be combined with (c)XSIBackup-Free and Pro to keep a fixed number of snapshots.

https://33hops.com/xsibackup-vmware-esxi-backup.html

Every time you call it a new snapshot will be generated and the eldest snapshot 
in the VM will be deleted if the predefined number of snapshots to keep has been reached.

This tool is of special interest to test engineers that need to keep multiple states 
of a given VM. It can also be used to keep multiple restore points per backup.

Download the xsibackup-snroll file, give it execute permissions and run the following 
command to get the help on acreen.

./xsibackup-snroll --help


