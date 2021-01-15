# Lawrence Assistant (v4.0)
version: 4.0
date: 21.01.16

This repository contains the configuration code for 'Lawrence', our virtual butler, built using [Home Assistant](https://home-assistant.io/). I got fed-up quickly with the lack of platform to connect the growing variety of 'smart' home equipment I had, and Lawrence was the solution! The first iteration of Lawrence was born in 2016 on a Raspberry Pi 1 (B) running Hass.IO. Today Lawrence is running within a Docker container on a Synology DS918+.

# Front End Screen Shots:
## Home
<p align="center">
  <img src="https://raw.githubusercontent.com/Durishn/Durnry-Assistant/master/www/img/home.png">
</p>

## History
<p align="center">
  <img src="https://raw.githubusercontent.com/Durishn/Durnry-Assistant/master/www/img/hist.png">
</p>

## Rooms
<p align="center">
  <img src="https://raw.githubusercontent.com/Durishn/Durnry-Assistant/master/www/img/rooms.png">
</p>

## Network
<p align="center">
  <img src="https://raw.githubusercontent.com/Durishn/Durnry-Assistant/master/www/img/net.png">
</p>

## Setting
<p align="center">
  <img src="https://raw.githubusercontent.com/Durishn/Durnry-Assistant/master/www/img/sett.png">
</p>

# Front-End - Sensors and Controllers:
- Presence Detection for residents using Bayesion Probability (TOP CENTER)- The state of 'Nic' and 'Emma' change between [Home, Away, Just Left, Just Arrived, Extended Away, Work] using probabilistic weights based on the state of the bluetooth and wifi of our phones.  If we've been 'Away' for longer than 24 hours we go into 'Extended Away Mode'. There are two groups, the household, which is always tracked and shown on screen, and guests which are only shown when one is 'Home'. If a guest is 'Home', the house will go into 'Guest Mode' which supersedes some automations that might leave them in the dark when we leave, but more on that later.
- Guest Detection (TOP CENTER)- guests that I've given access to our guest WiFi are put into a group, which tells the house whether we currently have guests over (keeps the house from going to sleep if guests are home alone)
- House States (TOP LEFT)- The state of the house changes between [Home, Away, GuestMode, Vacation, Asleep] based on Presence Detection, Guest Detection and Motion Detection. Climate from our thermostat is also shown below here, clicking this allows you to manually change things, but our automations handle all that for us anyway.
- Local weather (TOP RIGHT)- is pretty self-explanatory.
- Scenes (MIDDLE LEFT) - turn on lighting scenes and playlists throughout the house. Cabin mode also turns on a fireplace on the TV. I try to keep these basic, they are used a lot.
 - Family Calendar (BOTTOM LEFT) - Also pretty self-explanatory, we all have individuals calenders that share one 'Family' Calender, only these events are shown here, basic chores, family reminders etc.
- Speedtest Data (BOTTOM) - can be clicked to view graph.

- Motion, Temperature & Humidity Detection - 2 ecobee multisensors detect whether a room has had motion in the last 30 minutes, the current temperatures and humidity levels
- Cameras - 2 old iphones 4s are currently set up as mpeg IP cameras
- Lights - 3 ecobee lightbulbs
- Switches - 2 smart switches currently attached to floor lamps
- TV's - 2 roku's and 1 chromecast
- Speakers/Voice-Commands - 2 googlehomes, 1 chromecast, and 1 desktop
- Network Detection - constant surveillance of current devices connected to WiFi as well as speeds

# Automations
- Porch light on at sunset & off at night
- Office light off when no motion (i always forget to turn off my office)
- Unlock computer(script outside of HA) and turn on office lights when I scan the NFC chip implanted in my hand on the reader in my desk
- All Off when house 'away'
- 'Bright' on arrival
- Nightlight if sense motion at night
- Climate is 100% tied to house state based on 'Home', 'Away' or 'Vacation'
- Notify if motion on house 'away'
- notify if temperature too low or high
- notify on arrival if I'm not home (I creepily like to know who comes and goes from my home)
- Welcome message on arrival

# Hardware
- Raspberry Pi3 Model B+
- 2x iPhone 4
- 2x Google Home
- Chromecast Ultra
- 2x Roku
- 3 Coloured Hue Lightbulbs & Hub
- Ecobee Thermostat 2.0 with 2 sensors

#Inspirations

- https://github.com/matt8707/hass-config
- https://github.com/basnijholt/home-assistant-config/


# Final Notes
Security: I am far from a security expert, however, I have taken some important steps and considerations into account in this project and in my cyber-life in general. Make sure you are only serving your assistant over https:// and using a secure password with a limited number of attempts and blocking IPs. Anything that doesn't need to be connected to the internet isn't. Keep systems seperate with tight permissions and seperate users. Test your security, and test it often.
