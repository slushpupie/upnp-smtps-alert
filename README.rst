
SMTPS Alerts for Vera
=====================


Installation
------------

Upload the following files to your Vera (Apps -> Develop Apps -> Luup files)

  * ``D_SmtpsAlert.xml``
  * ``I_SmtpsAlert.xml``
  * ``S_SmtpsAlert.xml``
  * ``smtps.lua`` (found in the smtps directory)

Create a new Device (Apps -> Develop Apps -> Create device) with the following fields:

  * Device type: ``urn:slushpupie-com:device:SmtpsAlert:1``
  * Upnp Device Filename: ``D_SmtpsAlert.xml``
  * Upnp Implementation Filename: ``I_SmtpsAlert.xml``
  * Ip Address:  The hostname of your SMTPS server (e.g. ``smtp.gmail.com``)
  

After creating the device, go to the Advanced tab in the device settings. At the bottom, you need to set three new variables (one at a time):

  * ``user`` : This should be the username you log into the SMTPS server with (e.g.  ``example@gmail.com``).
  * ``pass`` : This should be the password you log into the SMTPS server with (Note: this is stored and displayed in plain text, so use at your own risk).
  * ``FromEmail`` : This should be the email address of the sender.

How to use it
-------------

 1. When configuring a scene you wish to be alerted about, click on the Advanced tab, select the SmtpsAlert device from the device list. 
 2. Select the ``SendEmail`` action.
 3. Fill in the ``Message`` and ``Recipient``.  Note: The message with be both the Subject and Body of the email.

