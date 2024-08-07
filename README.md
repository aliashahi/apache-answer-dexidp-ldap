# apache-answer-dexidp-ldap

an example setup of [apache/incubator-answer](https://github.com/apache/incubator-answer) with [Dex](https://github.com/dexidp/dex) A federated OpenID Connect provider to support LDAP.


### getting started!

first run two compose.yml files:

```bash
    docker compose up
```
and 
```bash
    cd mock-ldap
    docker compose up
```
then go to `http://localhost`

- setup database like this
![](images/setup-database.png)

- then setup some configs like this
![](images/setup-admin.png)

- then login with admin email and password, go to admin page and go to plugins
![](images/plugins.png)

- then activate oauth2.0 basic plugin
![](images/active-plugin.png)

- now setup dex parameters:
![](images/setup-oauth-basic1.png)
![](images/setup-oauth-basic2.png)

- now try to login with diffrent user:
![](images/login.png)


- click connect with example app, this login with your ldap credential(eg. `janedoe@example.com` with pass: `foo`):
![](images/login-dex.png)

- and you can now update your profile:
![](images/profile.png)

