## Setup for running emacsclient from the desktop and terminal more seamlessly.

### ``custom.emacsclient.desktop``
Copy this desktop shortcut into ``$XDG_DATA_HOME/share/applications``.

### ``app-emacs``
Copy this bash script from the repo into one of your ``$PATH``s. Please read the
script for the dependencies (should be fulfilled in almost every mainstream
linux distros).

What this script does is:

- Activate/Restart the emacsclient daemon when it's inactive.
- Create new emacsclient frames only when emacs has already started. NOTE: it can't differentiate emacs and emacsclient yet.
- Errors are logged to ``$XDG_DATA_HOME/share/nohup.txt``

### ``run-emacs``
Similar to ``app-emacs``, except that it's intended to run from the terminal.

### ``emacs.service``
Copy this file from your emacs installation into
``$XDG_CONFIG_HOME/systemd/user/``.

In Arch Linux and manjaro: the file is placed in ``/usr/share/emacs/27.1/etc/``
