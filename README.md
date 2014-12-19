Dell Inspiron 2-in-1 Screen Rotation Script for Linux
=====================================================

Tested successfully with Dell Inspiron 13 i7347 2-in-1 Laptop

usage: inspironRotateScreen [option]

options

        left            - rotates screen 90 degrees to the left from the normal mode

        right           - rotates screen 90 degrees to the right from the normal mode

        inverted        - rotates screen 180 degrees from the normal mode

        normal          - resets the screen orientation to normal mode

Script with option could be attached to Keyboard shortcuts as well as Operating System Events

The intention is to apply the script to system events that respond to the laptops internal gyroscope to automatically rotate the screen

Tested successfully using systemd under ArchLinux

Instructions for systemd
------------------------

Ensure /etc/systemd/user.conf has the following line:

	DefaultEnvironment=DISPLAY=:0

Copy inspironAutoRotateScreen.service to ~/.config/systemd/user folder

Start the service using the following command

	systemctl --user start inspironAutoRotateScreen.service

Enable the service to auto-start using the following command

	systemctl --user enable inspironAutoRotateScreen.service

Author: Karim Lalani - jimmy00784@gmail.com

