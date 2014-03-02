Swift Mailer WireMail module for ProcessWire CMF/CMS
====================================================

Copyright (c) 2013-2014 Teppo Koivula

This module extends WireMail base class, integrating the Swift Mailer mailing
library into ProcessWire.

## Getting started

In order to use WireMailSwiftMailer, you'll just have to install the module and
use ProcessWire's wireMail() function. For extensive instructions on that, take
a look at /wire/core/Functions.php.

Though Swift Mailer supports Mail Transport, i.e. using PHP's mail(), that's not
always sensible option. Real value of Swift Mailer is in it's Sendmail and SMTP
Transports.

If you're a Gmail user and only need to send a few mails now and then, following
DigitalOcean article is helpful for getting started with Gmail's SMTP server:
https://www.digitalocean.com/community/articles/how-to-use-google-s-smtp-server

## Basic usage

Basic usage is very close to how one would use PHP's native mail() function, but
the order of arguments is slightly different:

```
$number_of_recipients = wireMail($to, $from, $subject, $body);
```

Like PHP's mail(), wireMail() also returns the number of recipients accepted for
delivery. Note that this is *not* necessarily the number of recipients actually
receiving your message, just the number of addresses it was sent to.

## Word of warning

While this module should be fully functional, at least regarding the features it
currently includes, it's also very rough, doesn't handle more complex things and
definitely isn't intended for serious production use yet.

Another important thing to note is that as of this writing, WireMail is still a
feature of ProcessWire's dev brach.

## Swift Mailer

Swift Mailer is a powerful component based mailing library for PHP. If you want
to learn more about Swift Mailer and the things it can achieve you should visit
http://swiftmailer.org/.

Swift Mailer is copyright Fabien Potencier and released under the MIT license.

## License

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.

(See included LICENSE file for full license text.)