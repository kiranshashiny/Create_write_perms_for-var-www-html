# Create_write_perms_for-var-www-html


```
cat /etc/group

The webmasters should not be there
 
cat /etc/group|grep webmasters

The webmasters should not be there
 
addgroup webmasters

cat /etc/group

webmasters:x:1010:aayushman,amrith,shashi


usermod -a -G webmasters shashi
usermod -a -G webmasters amrith
usermod -a -G webmasters aayush

chgrp -R webmasters /var/www/html

chmod -R g+w /var/www/html
ls -al /var/www |grep html
root@atobs3:/var/www# sudo -u aayushman touch /var/www/html/test.txt
root@atobs3:/var/www# sudo -u shashi touch /var/www/html/test.txt
root@atobs3:/var/www# sudo -uamrith touch /var/www/html/test.txt


```
