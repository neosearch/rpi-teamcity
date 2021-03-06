Based on the awesome work by [PixelStik](https://github.com/pixelistik/rpi-teamcity) 
this is a clean Python implementation with some minor tweaks and use of Alpine-ARM for the JDK.

It uses Hypriot OS (a Raspbian variant) for a working Docker environment on your
Raspberry Pi.

Download the latest installation from here:

http://blog.hypriot.com/downloads/

Copy the image to your SD card and boot.

Default logins:

    Username: pi
    Password: raspbery

or for root:

    Username: root
    Password: hypriot


Update the packages in the install after booting initially with:

    $ sudo apt-get update && sudo apt-get upgrade

Then install docker-compose separately:

    $ sudo apt-get install python-pip
    $ sudo pip install docker-compose

Now everything should come together:

    $ docker-compose up

will build and start three different Docker containers

- Teamcity server
- Teamcity build agent
- Python base installation

Open http://<host>:8111 to access Teamcity. There are some remaining steps
that you need to do in the web UI, especially authorising the build agent.
