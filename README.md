# Trans Pay for Yunohost [![Donate with Trans Pay](https://dons.xn--transposes-i7a.eu/static/donate-with-transpay.png)](https://dons.transposées.eu/) 

## Overview

Trans Pay is developed by [Collectif Trans Posé·e·s](https://transposées.eu) for our own use and that of other associations. This tool is used to receive and manage donations:
* Supports one-time and monthly donations 
* Process cards with Stripe 
* Flexible and customizable 

## Demo

https://transpay.transposées.eu/

## Important notes

- For now you should need to tweak your dovecot / postfix configuration according to this pending PR https://github.com/YunoHost/yunohost/pull/815 and create the corresponding `/etc/postfix/sender_login_maps` to allow the user `transpay` to send emails as `transpay@domain.tld` (or the url of your choice, but gotta be consistent with what's in config.ini). Otherwise `transpay` won't be able to send email and that'll break stuff.
- More generally, you might want to tweak config options in `config.ini` after installing.
- You should make sure to test that everything's working fine before actually telling people about your transpay instance. For this, you can use test token APIs (available in Stripe's interface) and the [test card numbers](https://stripe.com/docs/testing#cards)
