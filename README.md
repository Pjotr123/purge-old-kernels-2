# purge-old-kernels-2
Fork of Ubuntu's purge-old-kernels, with a few minor changes in the notes.<br>
Shellscript, meant for Ubuntu and its derivatives like Linux Mint.<br>
<br>
This script will ALWAYS keep the currently running kernel and its headers.<br>
Default is 2, which means that it keeps one spare kernel besides the currently running kernel.<br>
Before you can use it, you need to make this shell script executable.<br>
Usage: sudo sh purge-old-kernels-2.sh<br>
You can change the number of kept kernels with --keep N. For example: sudo sh purge-old-kernels-2.sh --keep 3<br>
Any unrecognized option will be passed straight through to apt.
