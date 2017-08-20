# purge-old-kernels-2
Fork of Ubuntu's 'purge-old-kernels', with a few minor changes in the notes.<br>
It's a shell script, meant for Ubuntu and its derivatives like Linux Mint.<br>
<br>
Main reason for its existence: 'purge-old-kernels' has been deprecated since Ubuntu 16.04.<br>
But the intended replacement 'apt autoremove' (apt-get autoremove) does much more than just deleting old kernels.<br>
This might be undesirable, which is why some may prefer this precision instrument for removing only old kernels.<br>
<br>
This script will <b><i>always</b></i> keep the currently running kernel and its headers, which should make it safe to use.<br>
The default is 2, which means that it keeps one spare kernel besides the currently running kernel.<br>
<b>Before you can use it, you need to make this shell script executable. See the usage instruction below.</b><br>
<br>
Usage:<br>
1. Move the script from the folder Downloads to the folder /opt:<br>
sudo mv -v ~/Downloads/purge-old-kernels-2.sh /opt<br>
2. Set the permissions right (also making it executable):<br>
sudo chmod -v 755 /opt/purge-old-kernels-2.sh<br>
3. Launch it:<br>
sudo sh /opt/purge-old-kernels-2.sh<br>
<br>
You can change the number of kept kernels with '--keep N'. For example: sudo sh purge-old-kernels-2.sh --keep 3<br>
