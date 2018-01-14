## notmuch-address-cache

This program can be use to query contacts (names and email addresses) coming from notmuch. Querying sender directly with notmuch is fast. But querying for recipient are much slower. See [notmuch-address-1](https://notmuchmail.org/manpages/notmuch-address-1).

notmuch-address-cache can be use to be fast when searching for recipient.


## Installation

    brew tap mbauhardt/software
    brew install notmuch-address-cache


## Usage

Rebuild (initialize) the cache of all contacts you emailed with.

    % notmuch-address-cache rebuild --json

    Number of cached email addresses:        0
    Number of cached email addresses:      660
    Number of cached email addresses:      904
    Number of cached email addresses:     1136
    Number of cached email addresses:     1313
    Number of cached email addresses:     1806
    Number of cached email addresses:     2451
    Number of cached email addresses:     2561
    Your cache contains: 2589 email addresses.


Update your cache based on the notmuch tag `new`

    % notmuch-address-cache update --json 

    Found 0 (maybe new) email addresses.
    Found 11 (maybe new) email addresses.
    Found 11 (maybe new) email addresses. They will be merged to your cache right now.
    Your updated cache contains now 2600 email addresses.


Query contacts against your cache

    % notmuch-address-cache query github

    {"name": "Comment", "address": "comment@noreply.github.com", "name-addr": "Comment <comment@noreply.github.com>"},
    {"name": "Marko Bauhardt", "address": "notifications@github.com", "name-addr": "Marko Bauhardt <notifications@github.com>"},
    {"name": "GitHub", "address": "noreply@github.com", "name-addr": "GitHub <noreply@github.com>"},
    {"name": "GitHub", "address": "support@github.com", "name-addr": "GitHub <support@github.com>"},


See [Manual](https://raw.githubusercontent.com/mbauhardt/notmuch-address-cache/master/manual) for more details.


## Usage within alot

Open your `alot` config file `~/.config/alot/config` and add the shellcommand to the `abook` section.

    [accounts]
      [[your_account]]
        realname = 
        address = 
        sendmail_command = 
        draft_box = 
          [[[abook]]]
            type = shellcommand
            command = 'notmuch-address-cache query'
            regexp = '\[?{"name": "(?P<name>.*)", "address": "(?P<email>.+)", "name-addr": ".*"}[,\]]?'
            shellcommand_external_filtering = False


## Usage within mutt

Rebuild your cache with the `--text` option

    notmuch-address-cache rebuild --text

Open your `mutt` config file `~/.muttrc` and add the command into the `query_command`.

    set query_command = "notmuch-address-cache query '%s'"


