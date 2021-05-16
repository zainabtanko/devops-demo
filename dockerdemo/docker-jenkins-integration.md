# Enable jenkins to run sudo commands without password

Add below lines to sudoers file

`$ sudo visudo`

```
ALL     ALL=(ALL:ALL) ALL

jenkins   ALL=(ALL:ALL) NOPASSWD:ALL
```




# Jenkins Freestyle job to create docker iamge
* Execute shell :
``` mvn package
    cp <path_to_generated_addressbook.war_From above command> .
    echo "FROM bitnami/tomcat" > Dockerfile
    echo COPY addressbook.war /opt/bitnami/tomcat/webapps_default/addresssbook.war >> Dockerfile
    docker build -t addressbook:${BUILD_NUMBER} .
 ```
