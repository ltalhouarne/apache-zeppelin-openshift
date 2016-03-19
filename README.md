# Apache-zeppelin-openshift

### Openshift DIY cartridge for Apache zeppelin

Follow the below steps to deploy your own Zeppelin onto an openshift server.

* ```rhc app-create zeppelin diy-0.1```

* Add an extra 1GB to your gear **temporarily** since Zeppelin is a large application (you can revert back after the installation - however this might cost you a cent or two)

* ```git clone``` your application's source code (source code url can be found on the client)

* Navigate to the repo's root directory: ```cd zeppelin```
* Add this repository as remote: ```git remote add zeppelin https://github.com/ltalhouarne/apache-zeppelin-openshift.git```
* Pull the changes: ```git pull -s recursive -X theirs zeppelin master```
* Push to start up the deployment: ```git push```
  
#### After a successful installation, Zeppelin will be available at the following url:

  ```https://zeppelin-YOURDOMAIN.rhcloud.com:8443/#/```
