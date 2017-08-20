# purge-old-kernels-2
Fork of Ubuntu's 'purge-old-kernels' (part of the byobu package), with a few minor changes in the notes. It's a shell script, meant for Ubuntu and its derivatives like Linux Mint.<br>
<br>
Main reason for its existence: 'purge-old-kernels' has been deprecated since Ubuntu 16.04, because 'apt autoremove' should do the same job.<br>
<br>
But 'apt autoremove' (apt-get autoremove) does much more than just deleting old kernels. This might be undesirable, which is why some may prefer this precision instrument for removing only old kernels.<br>
<br>
Finally, this script is entirely independent from the byobu package, which is an additional advantage: you don't have to install any superfluous software.<br>
<br>
This script will <b><i>always</b></i> keep the currently running kernel and its headers, which should make it safe to use.<br>
The default is 2, which means that it keeps one spare kernel besides the currently running kernel.<br>
<br>
<b>Before you can use it, you need to make this shell script executable. See the usage instruction below.</b><br>
<br>
Usage:<br>
1. Launch a terminal window.<br>
2. Move the script from the folder Downloads to the folder /opt, with this command line (use copy/paste to transfer it):<br>
sudo mv -v ~/Downloads/purge-old-kernels-2.sh /opt<br>
3. Set the permissions right (also making it executable), with the following command (use copy/paste to transfer it):<br>
sudo chmod -v 755 /opt/purge-old-kernels-2.sh<br>
4. Launch it with the command below (use copy/paste to transfer it):<br>
sudo sh /opt/purge-old-kernels-2.sh<br>
<br>
You can change the number of kept kernels with '--keep N'. For example: sudo sh purge-old-kernels-2.sh --keep 3<br>
