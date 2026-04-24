---
hide:
  - path
---

## General usage documentation

ISSCloud is an self-hosted server of Nextcloud framework.

Nextcloud related information can be found in the following places:  

* [NextCloud User manual](https://docs.nextcloud.com/server/latest/user_manual/en/)
* [NextCloud Forum](https://help.nextcloud.com/)
* [NextCloud Blog](https://nextcloud.com/blog/)
* [NextCloud organization GitHub repository](https://github.com/nextcloud)

## Access end-points/Clients

* Main access point [https://isscloud.spacescience.ro/](https://isscloud.spacescience.ro/)
* Clients for Windows,Linux,MacOS: [https://nextcloud.com/install/#desktop-files](https://nextcloud.com/install/#desktop-files)
* Clients for Android,iOS: [https://nextcloud.com/install/#files-mobile](https://nextcloud.com/install/#files-mobile)

## 2FA activation for account security

see [Official documentation for two-factor authentication usage](https://docs.nextcloud.com/server/latest/user_manual/en/user_2fa.html)  

The [CERN official documentation](https://cern.service-now.com/service-portal?id=kb_article&n=KB0006587) state the following:  

!!! info ""
    The most optimal way is using a dedicated app like "[Aegis Authenticator](https://getaegis.app/)" (for Android)
    or "[Ente Auth](https://github.com/ente-io/auth?tab=readme-ov-file#-download)" (for iOS and Android) on your smartphone.  
    Both are for free and do not need any registration, so be careful of pay-for copy-cats or clones.  
    These apps produce every 30 seconds a new six-digit code
    (a so-called "One-Time Password" or OTP) which you are asked for at login.  
    Those apps do not need any other resources on your phone nor any privacy-impacting accesses.  
    Actually, any application supporting TOTP (RFC6238) should technically be compatible.  
    However, we do not recommend "Google Authenticator" as it comes with some security drawbacks.  

!!! note "Prerequisite"
    In order to register your smartphone, ensure that it is well synchronized with "world-time".  
    On iOS devices, go to "Settings" -> "General -> "Date & Time". "Set Automatically" should be ON.  
    On Android devices, go to "Settings" -> "System" -> Date & time" and have "Set time automatically" on ON.  
    Compare your time with this "world-time".  

!!! note "**Follow the NextCloud documentation for 2FA configuration**"
    **Continue with [Configuring two-factor authentication](https://docs.nextcloud.com/server/latest/user_manual/en/user_2fa.html#configuring-two-factor-authentication)**

!!! note "**Using client applications with two-factor authentication**"
    **Once you have enabled 2FA, your clients will no longer be able to connect with just your password**  
    unless they also have support for two-factor authentication.  
    To solve this, you should generate device specific passwords for them. See [Manage connected browsers and devices](https://docs.nextcloud.com/server/latest/user_manual/en/session_management.html) for more information on how to do this.


## Creation of application password

For various usages it is possible to define an application password
see [Manage connected browsers and devices](https://docs.nextcloud.com/server/latest/user_manual/en/session_management.html)  
that would allow setting up access without using the account password.  
The steps:

1. On the User settings (up-right corner) go to `Personal settings` --> then on left menu go to `Security`
2. In the lower part in the `Devices & sessions` define a new app password
    1. In the lowest dialogue set a app name like `WEBDAV` and click on `Create new app password`
    2. Write down the password (*IT WILL NOT BE SHOWN AGAIN!*), then close the dialogue
    3. Click on `***` section of this new device and make sure the `Allow filesystem access` is checked


## Usage of web public folders

There is possibility to make available *ReadOnly* a folder of the user named `PUBLIC`.  
This will become available as `https://isscloud.spacescience.ro/isspublic/<FirstName><LastName>`  
Steps towards this goal:  

1. One needs to create a folder named PUBLIC within it's own files
2. Go to Files and access the lower left corner item named `Files settings` and record the `WebDAV URL`
3. Create an `Application password` like in the section above. !!! NOTE DOWN THE PASSWORD
3. Contact the administrator with this information (WebDAV URL and password) for a local mount be setup for your PUBLIC WebDAV folder.


## Thunderbird e-mail client :: use FileLink feature to replace attachements with links

For attachements larger than a customizable size, there is an option to replace an attachement  
with an ISS-CLOUD link to a shared file/location. This has the effect that instead of sending  
5 Mb of attachement to 100 persons (with a net IO and space usage of 500 MB), the mail client  
will upload the attachement to ISS-CLOUD and share the link to the attachment in the email, thus  
drastically reducing the space and traffic required for this mail.  

There are 2 main steps:

1. Install the needed extension
    1. Thunderbird -> `Edit` -> `Settings` -> `Add-ons and Themes` -> `Find more add-ons` -> Search "nextcloud"
    2. Install `*cloud - FileLink for Nextcloud and ownCloud` (click on Add to Thunderbird)

2. Configure the extension
    1. Go to `Settings` -> `Composition` -> `Attachments` (last section)
    2. Enable/Check `Offer to share for files larger than` and choose a sensible value
       (1 MB is usefull if you send mail to many destinations)
    3. Click on `Add *cloud`
        1. Server url: `https://isscloud.spacescience.ro`
        2. User name: your ISS-CLOUD username
        3. App token (create and use here and application password like in the above section `Creation of application password`)
        4. Expand `Advanced options` and customize the properties and location of shares.

3. Usage
    1. for files larger than the above limit, the client will offer the conversion to a shared attachement
    2. if the file is smaller, there is the option of right-clicking on attachement and select `Convert to -> *cloud`


## NextCloud Tables

With this app you are able to create your own tables with individual columns. You can start with a template or from scratch and add your wanted columns.  
See [documentation](https://github.com/nextcloud/tables/wiki)

