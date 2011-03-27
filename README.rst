=======
postman
=======

``postman`` is a simple command line working with Amazon AWS, leveraging the
``boto`` library.


Usage
=====

::

    $ postman -h
    usage: postman [-h] [--version] [--verbose]
               
                   {show_stats,verify,send,show_quota,delete_verified,list_verified}
                   ...

    send an email via Amazon SES

    positional arguments:
      {show_stats,verify,send,show_quota,delete_verified,list_verified}

    optional arguments:
      -h, --help            show this help message and exit
      --version
      --verbose


Commands
========

``poastman`` has 6 different commands, in line with the various API calls available
for Amazon SES.


verify
------

verifies an email for sending (and in the case of the sandbox environment for
receiving as well)


delete_verified
---------------

removes a verified email address from your account


list_verified
-------------

print out a list of all verified email addresses on your account


send
----

sends an email, the content of the email is a raw email piped in very stdin, the
only option is ``-f`` which takes a single email address that the email is sent
from, following by 1 or more arguments that are email addresses that are the
the destination for the email.


show_quota
----------

print out the email quota and rate limits for you account


show_stats
----------

print out the stats for the Amazon SES account
