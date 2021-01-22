<!--
*** Thanks for checking out the Ender-README-Template. This repository was forked
*** from othneildrew's Best-README-Template available at
*** https://github.com/othneildrew/Best-README-Template
***
***
***
*** To avoid retyping too much info. Do a search and replace for the following:
*** Durishn, Durnry-Assistant, Lawrence - Home Assistant / Robo-butler, project_description, project_url
-->
<!-- To change the stability level, replace 'stable' with 'stable', 'unstable', 'experimental', or 'deprecated'-->
![Project State][stable-shield]
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![HA Version](https://img.shields.io/badge/Home%20Assistant-2021.1.1%20-darkblue)](https://github.com/home-assistant/core/releases/tag/2021.1.1)
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/Durishn/Durnry-Assistant">
    <img src="https://www.home-assistant.io/images/home-assistant-logo.svg" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Lawrence - Home Assistant / Robo-butler</h3>

  <p align="center">
    Home automation system - integrations, dashboards, and automations for home IoT devices 🏠 🤖
    <br />
    <br />
    <a href='https://www.buymeacoffee.com/nicdurish' target='_blank' style='margin-top:50px;'><img height='30' src='https://az743702.vo.msecnd.net/cdn/kofi1.png?v=0' border='0' alt='Buy Me a Coffee' /></a>
    <br />
    <br/ >
    <a href="https://github.com/Durishn/Durnry-Assistant/issues">Report Bug</a>
    ·
    <a href="https://github.com/Durishn/Durnry-Assistant/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li><a href="#overview">Overview</a>
      <ul>
        <li><a href="#front-end-screenshots"Front-End Screenshots</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#authors">Authors</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#acknowledgements-and-inspiration">Acknowledgements and Inspiration</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][product-screenshot]](https://project_url)

This repository contains the configuration code for 'Lawrence', my virtual butler, built using [Home Assistant](https://home-assistant.io/). I got fed-up quickly with the lack of platform to connect the growing variety of 'smart' home equipment I had, and Lawrence was the solution! The first iteration of Lawrence was born in 2016 on a Raspberry Pi 1 (B) running Hass.IO. Today Lawrence is running within a Docker container on a Synology DS918+.

### Built With

This project was built with the use of the following frameworks. For add-ons, plugins and resources, please see the acknowledgements section
* [Home Assistant](https://www.home-assistant.io/)
* [Docker](https://docker.com)
* [HA Supervisor](https://github.com/home-assistant/supervisor)


<!-- USAGE EXAMPLES -->
## Overview

### Front-End Screenshots
#### Home:
<p align="center">
  <img src="https://raw.githubusercontent.com/Durishn/Durnry-Assistant/master/www/img/docs/1.png">
</p>

#### Floorplan (Styles to be updated):
<p align="center">
  <img src="https://raw.githubusercontent.com/Durishn/Durnry-Assistant/master/www/img/docs/2.png">
</p>

#### Profiles:
<p align="center">
  <img src="https://raw.githubusercontent.com/Durishn/Durnry-Assistant/master/www/img/docs/3.png">
</p>

#### Network:
<p align="center">
  <img src="https://raw.githubusercontent.com/Durishn/Durnry-Assistant/master/www/img/docs/4.png">
</p>

#### Setting:
<p align="center">
  <img src="https://raw.githubusercontent.com/Durishn/Durnry-Assistant/master/www/img/docs/5.png">
</p>

#### Cameras (Deprecated):
<p align="center">
  <img src="https://raw.githubusercontent.com/Durishn/Durnry-Assistant/master/www/img/docs/6.png">
</p>

### Automations
- Porch light on at sunset & off at night
- Office light off when no motion (I always forget to turn off my office)
- Unlock computer(script outside of HA) and turn on office lights when I scan the NFC chip implanted in my hand on the reader in my desk [FAQ](https://www.youtube.com/watch?v=5tCyVfcFOG0)
- All Off when house 'away'
- 'Bright' on arrival
- Nightlight if sense motion at night
- Climate is 100% tied to house state based on 'Home', 'Away' or 'Vacation'
- Notify if motion on house 'away'
- notify if temperature too low or high
- notify on arrival if I'm not home (I creepily like to know who comes and goes from my home)
- Welcome message on arrival
- Allow Hue switches to also control switches  
- Turn on Chicken Coop Power if temperature is below 0 degrees (turns on water and space heater)
- Notify me if Bitcoin prices drop below a certain rate-of-change threshold

## Hardware
- Synology DS918+
- 2 iPhone 4 (security cameras)
- 3 Google Home
- 1 Chromecast Ultra
- 2 Roku Streaming Sticks
- 3 Hue Coloured Lightbulbs
- 1 Hue Edison Bulb
- 5 Hue White Temperature-controllable lightbulbs
- 1 Hue LED strip
- 2 TP-Kasa Smart Plugs
- Ecobee Thermostat 2.0 with 2 sensors


<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple steps.

### Prerequisites

Before using this Home Assistant configuration file, you'll need an instance of Home Assistant (minimum version 2021.1.1) running locally. For more information on getting Home Assistant setup, please review the [Home Assistant Documentation](https://www.home-assistant.io/docs/)


### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/Durishn/Durnry-Assistant.git
   ```

2. Replace your `config` directory within your HA instance with this config!

<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/Durishn/Durnry-Assistant/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<!-- Authors -->
## Authors
Nic Durish - [@Durishn](https://twitter.com/Durishn) - [mail@nicdurish.ca](mailto:mail@nicdurish.ca)

See the [contributors](https://github.com/Durishn/Durnry-Assistant/contributors) page for an updated list of contributors to this project



<!-- LICENSE -->
## License
Distributed under the MIT License. See [`LICENSE`][license-url] for more information.



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements and Inspiration
- [Matt8708's config](https://github.com/matt8707/hass-config)
- [basnijholt's config](https://github.com/basnijholt/home-assistant-config/)

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->


[stable-shield]: https://img.shields.io/badge/stability-stable-green.svg
[unstable-shield]: https://img.shields.io/badge/stability-unstable-yellow.svg
[deprecated-shield]: https://img.shields.io/badge/stability-deprecated-orange.svg
[experimental-shield]: https://img.shields.io/badge/stability-experimental-red.svg

[contributors-shield]: https://img.shields.io/github/contributors/Durishn/Durnry-Assistant.svg
[contributors-url]: https://github.com/Durishn/Durnry-Assistant/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Durishn/Durnry-Assistant.svg
[forks-url]: https://github.com/Durishn/Durnry-Assistant/network/members
[stars-shield]: https://img.shields.io/github/stars/Durishn/Durnry-Assistant.svg
[stars-url]: https://github.com/Durishn/Durnry-Assistant/stargazers
[issues-shield]: https://img.shields.io/github/issues/Durishn/Durnry-Assistant.svg
[issues-url]: https://github.com/Durishn/Durnry-Assistant/issues
[license-shield]: https://img.shields.io/github/license/Durishn/Durnry-Assistant.svg
[license-url]: https://github.com/Durishn/Durnry-Assistant/blob/master/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-Github-black.svg?logo=github&colorB=555
[linkedin-url]: https://github.com/Durishn
[product-screenshot]: www/img/docs/demo.gif
