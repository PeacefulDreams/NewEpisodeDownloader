# New Episode Downloader

**Disclaimer**

This script is a working proof of concept based on a Reddit discussion about the ability to have Sonarr download next episodes when nearing the end of a season. It may have some bugs and has been tested on a local instance with a single user; Your mileage may vary.

@gignsky has improved this script, and has a further developed version of this script with multi-user and monitoring support available at https://github.com/gignsky/plex-sonarr-auto-download-next-season.


**Project description**

New Episode Downloader is an automation script that connects to Plex and Sonarr to automatically
download the next season of a show you are watching based on the episode you are on.

It has been tested on a local environment with one active plex user, so your mileage may vary on larger installs.

The script can be installed in two ways: Via Docker or just as a plain Python script with cron.

**Docker install method**

1. ``cd`` into the folder of the script.
2. Open the script and adjust the variables to your setup (Plex URL, Token, Sonarr URL, Token)
3. In a terminal, type ``docker build .`` to build the docker container. At the end of the process, Docker will tell you the tag
  it has given to the resulting image.
4. In the same terminal, type:
5. ``docker run [NAME OF CONTAINER IMAGE HERE]``

**Python install method**

1. Copy the script anywhere you like. Be aware that their might be some permission issues with cron depending on where you put it.
2. Open the script and adjust the variables to your setup (Plex URL, Token, Sonarr URL, Token)
3. In a terminal, type ``crontab -e`` to add the script to cron and run it periodically
    You can take some inspiration from the crontab file that comes with the script for the docker container.
    Do however check if the path to your python executable is the same. You can do so by typing ``which python`` or ``which python3`` in a terminal.

