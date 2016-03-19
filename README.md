# Apache-zeppelin-openshift
Openshift DIY cartridge for Apache's zeppelin

1) rhc app-create zeppelin diy-0.1

2) Add 1GB temporarily for downloading and extracting zeppelin (you can revert back after the installation - this might cost you a cent or two)

3) git clone your application's source code (source code url can be found on the client)

4) Follow the below steps to add the deployment code for the application:
  cd zeppelin
  git remote add zeppelin https://github.com/ltalhouarne/apache-zeppelin-openshift.git
  git pull -s recursive -X theirs zeppelin master
  git push
  
5) After a successful installation, Zeppelin will be available at the following url:

  https://zeppelin-<YOURDOMAIN>.rhcloud.com:8443/#/
