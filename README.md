# permission-
# ad groups provide access to the following Linux servers

vim /etc/sudoers.d/linux_hosting
%NA\ CTS\ LINUX\ HOSTING\ \(Universal\) ALL=(ALL) NOPASSWD: ALL

vim /etc/sssd/sssd.conf
, americas\NA CTS LINUX HOSTING (Universal)

service sssd restart



## ...........................
## adding new  user and password in server and change uid for new-mount

login to the  server using ssh 

sudo su
vim /etc/.cifscreds   #add a user and password
su username    #login with user you added
id    #for id we will do this and copy the uid and we will pase in fstab file
exit  # we havwe to exit from current user 

vim /etc/fstab    #edit the uid 

df -h    # check which server is mounted with directory and we will umount the directory
umount dir-name   #which already mounted
mount -a          # mount the dir


#check with ll /dir-name/

##.....................................................
server umount/ mount task with new-path
ssh server-name
sudo su
df -h 
df -h | grep old-mount    ## for checking
vim /etc/fstab     ## edit there 
umount old-mount
mount -a   ## for new
df -h | grep old-mount ## for checking 
ll old-mount





