Axel's Sinfest RSS Generator
============================

This is a Perl written replacement for the
[broken/stale RSS feed](http://www.sinfest.net/rss.php) of the
daily webcomic [Sinfest](http://www.sinfest.net/).

Their RSS feed is stale since their site got a new design around the
8th of June 2014.

Usage
-----

By default it generates an RSS feed for the past 7 days and fetches
all titles from the website for that.

# Liferea

The script can be used as command-type source in
[Liferea](http://liferea.sf.net/). Actually it was written for exactly
that purpose.

Options
-------

* `-n`: Don't download anything from the Sinfest website, just generate
  a feed with dummy titles.
  
* `-d <number>`: Generate a feed for the past _<number>_ days.

  Setting this value high enough for one run may give you all feed
  entries you missed since 8th of June 2014.

  But remember to do this only once as it fetches every page for every
  day since then per run to get the comic title for that day. You may
  get banned if you do that too often.

Requirements
------------

Besides modules from the Perl core distribution, the following Perl
module are required and can be found at least on CPAN as well as
packages on Debian:

* [POSIX::strftime::Compiler](https://metacpan.org/release/POSIX-strftime-Compiler)
* [Date::Calc](https://metacpan.org/release/Date-Calc)
* [LWP::UserAgent](https://metacpan.org/pod/LWP::UserAgent) from the
  [libwww-perl](https://metacpan.org/release/libwww-perl) distribution

License
-------

Copyright (C) 2015 Axel Beckert

Licensed under the _DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE_. See
the file [LICENSE](LICENSE) or http://www.wtfpl.net/txt/copying/ for the full
license text.
