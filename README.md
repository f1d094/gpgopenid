gpgopenid
=========

An OpenId identity provider that verifies your identity through your openpgp key.
Works well with OpenPGP SmartCards such as the CryptoStick.
In your browser you need to install EnigForm that talks to gnupg.
On the server, mod_openpgp verifies the digital signature of the http header.

It is easiest if you install the debin package from my launchpad ppa when it gets ready.
If you want to install it manually, first follow all the steps at http://wiki.buanzo.org/index.php?n=Main.Wp-enigform-authentication and then come back here.

At the moment, you have to start gpgopenid.py manually. In the future, the package should set it up as a daemon. It only works, if it is reached throuch an apache reverse proxy, so that mod_openpgp can do it's magic with the html headers. See gpgopenid.test for the required apache configurations.


