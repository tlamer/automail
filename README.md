automail
========

This is a simple script for sending mails rendered from templates.

The default config location is `~/.automailrc`. Multiple servers can by defined
while the default is set in `[general]` section. For other servers use
`-s/--server` Default value for starttls is yes.

Configuration file example:

    [general]
    server = foobar

    [foobar]
    host = <smtp host>
    port = <smtp port>
    starttls = <yes/no>
    signature = <path to signature file>

Example template:

    To: foo@bar.com,foot@bar.com
    From: bar@bar.com
    Subject: Lorem ipsum {{ var0 }}

    Lorem {{ var1 }} dolor sit amet, consectetur adipiscing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
    quis nostrud {{ var2 }} ullamco laboris nisi ut aliquip ex ea commodo
    consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
    cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
    non proident, sunt in culpa qui officia deserunt mollit anim id {{ var3 }}
    laborum.
