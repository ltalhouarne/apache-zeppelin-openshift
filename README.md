# Apache-zeppelin-openshift

### Openshift DIY cartridge for Apache zeppelin

Follow the below steps to deploy your own Zeppelin application onto an openshift server.

* ```rhc app-create zeppelin diy-0.1``` (You can create it through Openshift's site directly if you don't have ```rhc``` installed)

* Add an extra 1GB to your gear **temporarily** since Zeppelin is a large application (you can revert back as soon as the installation completes - however this might cost you a cent or two). In order to do so, click on "1GB" in your application details in Openshift and by adding an extra GB:

![img](http://i.imgur.com/92P7aGE.png)

* ```git clone``` your application's source code. The source code url of your application can be found to the right of your application details in Openshift:

![img](http://i.imgur.com/5RR3bE6.png)

* Navigate to the repo's root directory: ```cd zeppelin```

* Add this repository as remote: ```git remote add zeppelin https://github.com/ltalhouarne/apache-zeppelin-openshift.git```

* Pull the changes: ```git pull -s recursive -X theirs zeppelin master```

* Push to start up the deployment: ```git push```
  
#### After a successful installation, Zeppelin will be available at the following url:

  ```
  https://zeppelin-YOURDOMAIN.rhcloud.com:8443/#/
  ```
