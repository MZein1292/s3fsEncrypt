HOW TO COMPILE THE NEW MODIFIED SOURCE CODE: 


1- modify the key pass .passkey.txt on the first line inside /src and enter your own key pass

2- run these 3 commands to compile:

> ./configure
> make
> sudo make install


3- once compiled, cd into src

if the mount directory was already mounted, run:

> sudo fusermount -u /mnt/s3 

if not jump to step 4

4- once unmouted, run the mount command from the new executable generated by the make file using this command:

> sudo ./s3fs <bucketname> /mntDir/ -o allow_other

5- cp a text file and an image inside the mount directory



6- Open the files in amazon console to ensure they are encrypted, and open the files inside mount directory to ensure the files gets decrypted on the local machine


