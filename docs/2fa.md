---
hide:
  - path
---

# 2FA activation for account security

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


