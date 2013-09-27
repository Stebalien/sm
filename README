sm - a simple session manager
=============================

sm is a minimalistic session manager/launcher. It's actually just a set of
functions that make setting up/tearing down a session easier.

Config
------

Session config files go under `$XDG_CONFIG_DIR/sm/my_session_name`.

Actions
-------

login:

    sm my_session_name

logout (from within the session):

    kill $XDG_SESSION_PID

Commands
--------

Command       | Description
--------------|------------
`spawn   cmd` | execute `cmd` in the background
`respawn cmd` | execute `cmd` in the background and automatically restart it
`import  cmd` | execute `cmd` and evaluate the result (usefull for launching ssh agents and other programs that need to set environment variables)
`defer n cmd` | execute `cmd` after an `n` second delay
`online  cmd` | execute `cmd` when an internet connection has been extablished (requires network-manager)

Example
-------

    import  ssh-agent
    spawn   nitrogen --restore
    online  dropbox
    respawn bspwm
