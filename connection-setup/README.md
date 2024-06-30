# connection between click hosuse and superset

* __step1__: connect to __super set__ with __minikube ip__:<superset nodeport number>
 * login into superset
    * default user name __admin__
    * default user name __admin__

* step2: On the right side corner, click on Data, --> connect to __database__
  * click on other options
  * identiy click house connet
  * note: we are connecting using __hostname__, __port number__, __user name__  and __password__
  * __hostname__ : <minikube ip>
  * __Port__ : 8123
  * username: Default
  * passwrd: clickhouse   ## Y2xpY2tob3VzZQ==     --> which we passed at __configmap__ at clickhouse