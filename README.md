# You probably shouldn't use this
This repository contains files that allow [libwt](https://github.com/emweb/wt)
to be compiled into a package for [Debian](https://www.debian.org).

However, it's done quickly and not very well. The reason I did it is to allow
[ear](https://github.com/wijnen/ear) to compile. If that is what you want to
do, feel free to use these files. Otherwise, you may find that a lot of
optional features are not enabled due to missing dependencies.

While I'm open to pull requests, I think an easier way to a good package is to
take the existing packaging from ancient times (oldstable at the time of this
writing) and update it. The reason it was originally removed (the Haru PDF
library not working) is no longer true, so it shouldn't be very hard to do
this.

# How to use

1. Download a release or a zip of the current master from [libwt](https://github.com/emweb/wt). Unpack it, then repack it as .tar.gz and name it `libwt_4.7.2.orig.tar.gz` (but also keep the unpacked version)
1. Copy the files from this repository into the tree, in a directory named `debian`
1. Run `debuild -uc -us`
1. Install the `.deb`-files that were generated in the parent directory
