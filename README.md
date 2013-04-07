Patch vzdump on Debian squeeze
=============

This script creates an alternate vzdump script which works around the tar issue 'Cannot rmdir: Directory not empty' on Debian Squeeze.


The issue
-------
tar 1.23 used in Debian Squeeze has a known bug with --remove-files option and fails to process some files. 
'Cannot rmdir: Directory not empty' appears in logs. 

See : http://lists.debian.org/debian-user/2011/06/msg00177.html

This option is used by vzdump, which breaks when using --suspend on Debian. If you don't want to update to testing or use another repository, you can disable this option in vzdump.

Solution based on : 

http://opennodecloud.com/forum/index.php?topic=123.0


Contributing
------------

Want to contribute? Great! Improve the script and share your changes.


How to run 
-----------

    ./vzdumpfixed

then use vzdumpfixed instead of vzdump

    /usr/sbin/vzdumpfixed



Disclamer
-------

Use this script at your risks. 

Review the content before running the script.


Tested on Debian squeeze



