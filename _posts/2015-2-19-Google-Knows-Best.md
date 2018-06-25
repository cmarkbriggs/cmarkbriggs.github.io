---
layout: post
title: Hello, Again
---
I manage the digital certificates for our company. I've used [DigiCert](https://www.digicert.com/) for years and have been very happy with them. We have wildcard certificates with them, and the ease with which one can get duplicate certificates to install on different servers is really nice.

A colleague happened to bring to my attention yesterday that one of our sites with a DigiCert certificate no longer appeared as completely secure when viewed in Chrome. As I do not use Chrome on a regular basis, I never noticed this. The site showed as secure, like it is supposed to, in Safari and Firefox. So I then brought up the site in Chrome and saw the little yellow caution sign where one would expect to see a green lock in the address bar. A little research brought me to [this post on the Chromium Blog from last September](http://blog.chromium.org/2014/09/gradually-sunsetting-sha-1.html):

> That’s why Chrome will start the process of sunsetting SHA-1 (as used in certificate signatures for HTTPS) with Chrome 39 in November. HTTPS sites whose certificate chains use SHA-1 and are valid past 1 January 2017 will no longer appear to be fully trustworthy in Chrome’s user interface.

So it doesn't matter to Chrome and Google that I have a valid certificate. It is not difficult to replace the certificate with one that uses SHA-2, but that is not the point. The point is that Google, because of their fervor for doing their own thing, will needlessly worry the people who won't bother to research the confusing message that is displayed when you click on the warning icon.

I wish Google would just adhere to standards. Yes, wishful thinking, I know.
