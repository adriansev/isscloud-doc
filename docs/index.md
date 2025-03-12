---
hide:
  - navigation
  - toc
  - path
---

# ISS Cloud howto and usage documentation

ISSCloud is an self-hosted server of Nextcloud framework.

Nextcloud related information can be found in the following places:  

* [NextCloud User manual](https://docs.nextcloud.com/server/latest/user_manual/en/)
* [NextCloud Forum](https://help.nextcloud.com/)
* [NextCloud Blog](https://nextcloud.com/blog/)
* [NextCloud organization GitHub repository](https://github.com/nextcloud)


## Usage of web public folders

There is possibility to make available *ReadOnly* a folder of the user named `PUBLIC`.  
This will become available as `https://isscloud.spacescience.ro/isspublic/<FirstName><LastName>`  
Steps towards this goal:  

1. One needs to create a folder named PUBLIC within it's own files
2. Go to Files and access the lower left corner item named `Files settings` and record the `WebDAV URL`
    1. if 2FA is enabled follow the instruction
3.  Contact the administrator with this information in order that a local mount be setup for your PUBLIC WebDAV folder.

