notmuch-address-cache(1)                                                                                                                notmuch-address-cache(1)



NAME
       notmuch-address-cache - caches the result from notmuch-address and search within this cached version.


SYNOPSIS
       notmuch-address-cache [ COMMAND ] [ ARG ]


DESCRIPTION
       notmuch-address-cache is basically a cache in front of the notmuch-address command.

       notmuch-address-cache caches all sender and recipients you communicated with. It expect the notmuch tag tag:all on all messages to extract the sender and
       recipients from there. You can configure notmuch to apply the tag:all to all messages. This is basically done if you edit the file ~/.notmuch-config,  go
       into section [new] and add the value all to the key tags.


Commands
       help, --help, -h
              Show help text.

       version, --version, -v
              Show the version.

       rebuild, --rebuild, -r [--json | --text]
              Uses  notmuch-address  to  find  all sender/recipient you communicated with and print them out to the file ~/.notmuch-address-cache/addresses. The
              format of the cached addresses are stored in json, if you rebuild your cache with option --json. The format of the cached addresses are stored  in
              text, if you rebuild your cache with option--text. Format text is recommended if you want to query the cache with mutt. Format json is recommended
              if you want to query the cache with alot.

       query, --query, -q
              greps bla bla



version v0.1                                                                Sep 2017                                                    notmuch-address-cache(1)
