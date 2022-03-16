PPP Files
===
Copyright &copy; CodeZoo 2022

Description
===
This repo contains example PPP files for various Skywire modems on Linux. These files provide direction on setting up a PPP connection, but they may need to be adapted to the specific embedded design developed by the customer. Each end customer embedded design is different.

We recommend reviewing the PPPD manual page for more information and options:

	man pppd

Usage
===
Copy the script file and its associated chat file (or all of the files) into:

    /etc/ppp/peers/

If you have a Skywire modem that uses a SIM card, follow instructions in your

    *-chat

file to set the APN.

Run your respective command:

    sudo pppd call [script file]

or

    sudo pon [script file]

Example
===
To use the CodeZoo LTE CatM1 Embedded Modem, copy the following files:

    vodafone-Type1SC
    vodafone-Type1SC-chat

to "/etc/ppp/peers/".

Edit the file:

    vodafone-Type1SC-chat

to insert the APN. In this example, replace:

    [apn]

with:

    simplio.apn

Finally, issue the following command:

    sudo pon vodafone-Type1SC
