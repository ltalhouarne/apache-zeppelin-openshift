# Apache-zeppelin-openshift
Openshift DIY cartridge for Apache's zeppelin

1) rhc app-create zeppelin diy-0.1

2) rhc cartridge-storage -a zeppelin -c diy-0.1 --set 2GB

3) cd zeppelin
git remote add zeppelin 
git pull -s recursive -X theirs zeppelin master
git push

rhc app-create zeppelin diy-0.1 --from-code https://github.com/ltalhouarne/apache-zeppelin-openshift.git
