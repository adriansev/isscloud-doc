---
hide:
  - path
---

# Creation of application password

For various usages it is possible to define an application password (see [here](https://docs.nextcloud.com/server/latest/user_manual/en/session_management.html))  
that would allow setting up access without using the account password.  
This means that for each client/application one can define a _**per application**_ password  
that can be removed/revoked any time for a given application that one want to remove the access.  

The steps:

1. On the User settings (up-right corner) go to `Personal settings` --> then on left menu go to `Security`
2. In the lower part in the `Devices & sessions` define a new app password
    1. In the lowest dialogue set a app name like `MYAPP` and click on `Create new app password`
    2. Write down the password (*IT WILL NOT BE SHOWN AGAIN!*), then close the dialogue
    3. Click on `***` section of this new device and make sure the `Allow filesystem access` is checked


