# pterodactyl-daemon-auto-installer

I suggest installing an SSL for your daemon over at LetsEncrypt ( This will make your node able to support SSL requests )

- Ubuntu 18.04 letsencrypt apache2 install: https://certbot.eff.org/lets-encrypt/ubuntubionic-apache
- Ubuntu 16.04 letsencrypt apache2 install: https://certbot.eff.org/lets-encrypt/ubuntuxenial-apache

These scripts help automate the daemon install process by only having the user run the script input a token generated by the panel and then they run the 2nd script and the daemon should be online and running without problems :)


Made for Ubuntu 16.04 & Ubuntu 18.04
Made with <3 by Brad

# Get the scripts by doing. 
1. sudo wget https://github.com/NanoNode/pterodactyl-daemon-auto-installer/archive/master.zip

# Unzip the file.
2. sudo unzip master.zip

# Go to the scripts directory.
3. cd /pterodactyl-daemon-auto-installer-master

# Give the script the correct permissions to run.
4. sudo chmod +x auto-daemon-setup.sh

# Run the script.
5. sudo ./auto-daemon-setup.sh

Once completed it'll tell you to put in your token which you get from creating your node.
Navigate to https://domain.ltd/admin/nodes/view/1 then Configuration.
Select " Generate Token " then copy and paste the one liner into the terminal.

# Give the service script the correct permissions.
6. sudo chmod +x auto-service-setup.sh

# Run the script.
7. sudo ./auto-service-setup.sh

After you've completed the following steps. The daemon should be online and working properly :)


WARNING: The script doesn't check for anything. Currently it doesn't check if there is an existing configuration of the service file or anything else. All it does is automatically run a few commands and completes the service process.

NOTE: This script was made to make my life easier when installing daemons on new machines for a network I am working on. Setting up the daemon on new machines every other day was getting annoying coping and pasting commands into the terminal. So I put these two scripts together. I hope they help you all. You can do what ever you want with these scripts but I'll plan on updating them when ever a new version of the daemon gets released. I haven't attempted to create a panel script yet because it's a monster task but these two scripts should make creating a daemon from a fresh operating system a lot easier!
