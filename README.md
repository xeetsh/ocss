ocss
====

OwnCloud Screenshot Sharing (based on rage311's work)

Features:
  - Taking a screenshot from a selected window or area
  - Automatically uploading this screenshot to Owncloud/Nextcloud
  - Creating a shared link in Owncloud/Nextcloud
  - Shorting the link via Yourls
  - Copying the link in your clipboard

Dependencies:
-------------

Shared:
  - curl
  - grep

Linux:
  - maim
  - slop
  - notify-send
  - xclip
  - lynx

OS X:
  At the moment I can't test the OS X compatiblity so i don't know if the script is working there.
  A problem might occure if you use Yourls URL shorting because of Lynx. Maybe look into using Lynxlet for OS X.
  
  - terminal-notifier
  - screencapture
  - pbcopy


Instructions:
-------------

Get ocss.sh by either cloning this repo or downloading the zip.
Edit the CONFIG portion of ocss.sh and fill in your details/preferences.  By default, it's setup to save screenshots locally to $HOME/Pictures/ocss (config setting: file_dir), so either change that to a directory that exists or create that directory.  Also by default, it will upload the screenshots to a folder named "ocss" in your Owncloud root (config setting: oc_ocss_dir_name)... make sure that exists.  The default open command that opens a browser to display your new upload is chromium (config setting: open_command).

Run it with the "check" argument to check if all required dependencies exist.

`$ ./ocss.sh check`

I haven't tested this with OS X, but it's mostly the same code base as imgur-screenshot and that is purported to work in OS X, so it SHOULD work.
