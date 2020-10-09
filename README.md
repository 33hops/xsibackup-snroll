# xsibackup-snroll
(c)XSIBackup Snapshot Roll

This Bash script allows to set a predefined number of snapshots per virtual machine. 
Just try the script on the command line and then call it from the ESXi crontab.
It can be combined with (c)XSIBackup-Free and Pro to keep a fixed number of snapshots.
Every time you call it a new snapshot will be generated and the eldest snapshot 
in the VM will be deleted if the predefined number of snapshots to keep is reached.

This tool is of special interest to test engineers that need to keep multiple states 
of a given VM. It can also be used to keep multiple restore points per backup.

----------------------------------------------------------------------
(c)33HOPS Snapshot Roll 1.0.0.0
----------------------------------------------------------------------

  Usage:

  ./xsibackup-snroll <VM Name> <Num of Snapshots> <Quiesce> <Include memory>

  VM Name:              Name of VM as seen with 'vim-cmd vmsvc/getallvms'
  Num of Snapshots:     Number of snapshots to rotate
  Quiesce:              Boolean, acepts 0|1, yes|no, true|false
                        Sets whether the snapshot will be quiesced
                        Quiescing is not a trivial task, you must
                        make sure VMWare Tools are installed and
                        all required services properly configured
  Include memory:       Boolean, acepts 0|1, yes|no, true|false
                        Includes the guest's memory in the snapshot

