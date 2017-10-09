## notmuch-address-cache

This program can be use to query contacts (names and email addresses) coming from notmuch. Querying sender directly with notmuch is fast. But querying for recipient are much slower. See [notmuch-address-1](https://notmuchmail.org/manpages/notmuch-address-1).

notmuch-address-search can be use to be fast when searching for recipient.


## Dependencies

[notmuch](https://notmuchmail.org), [sed](http://sed.sourceforge.net/), [awk](https://www.gnu.org/software/gawk/manual/gawk.html)


## Usage

[Manual](https://raw.githubusercontent.com/mbauhardt/notmuch-address-cache/master/manual)


## Installation

[Download](https://github.com/mbauhardt/notmuch-address-cache/releases/latest) the script in one of your PATH folders.


## Tested With

    [Mon 9, 5:40] 0 % sw_vers                                      
    ProductName:    Mac OS X
    ProductVersion: 10.11.6
    BuildVersion:   15G31 

    [Mon 9, 5:42] 1 % notmuch --version                                               
    notmuch 0.25.1

    [Mon 9, 5:43] 2 % awk --version
    awk version 20070501

    [Mon 9, 5:46] 0 % sed --version
    sed: illegal option -- -


