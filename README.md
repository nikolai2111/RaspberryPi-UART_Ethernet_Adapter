<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/nikolai2111/RaspberryPi-UART_Ethernet_Adapter"></a>

<h3 align="center">Raspberry Pi UART to Ethernet Adapter</h3>

  <p align="center">
    This adapter board enables the creation of a stand-alone, network-compatible device using any Raspberry Pi compatible UART daughterboard.
    <br />
    <a href="https://github.com/nikolai2111/RaspberryPi-UART_Ethernet_Adapter"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/nikolai2111/RaspberryPi-UART_Ethernet_Adapter">View Demo</a>
    ·
    <a href="https://github.com/nikolai2111/RaspberryPi-UART_Ethernet_Adapter/issues/new?labels=bug&template=bug-report---.md">Report Bug</a>
    ·
    <a href="https://github.com/nikolai2111/RaspberryPi-UART_Ethernet_Adapter/issues/new?labels=enhancement&template=feature-request---.md">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#Configure WIZ750SR">Configure WIZ750SR</a></li>
        <li><a href="#Confgure Z-Wave JS UI">Confgure Z-Wave JS UI</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

This adapter board enables the creation of a stand-alone, network-compatible device using any Raspberry Pi compatible UART daughterboard. The adapter board is used to connect the daughterboard of the Raspberry Pi and [WIZ750SR](https://docs.wiznet.io/Product/S2E-Module/WIZ750SR)-TTL. The adapter board connects the daughterboard of the Raspberry Pi to the [WIZ750SR](https://docs.wiznet.io/Product/S2E-Module/WIZ750SR)-TTL. It also provides a 5V and 3.3V power supply where necessary.

The adapter board was initially designed to connect the [RaZberry 7 Pro](https://z-wave.me/products/razberry/#slide-1) to [Home Assistant](https://www.home-assistant.io/) via TCP, without using a Raspberry Pi as a server. It can also be used with any Raspberry Pi daughterboard that only needs the TTL-UART interface. However, the following README refers to the use of the [RaZberry 7 Pro](https://z-wave.me/products/razberry/#slide-1) with [Home Assistant](https://www.home-assistant.io/). It is possible to map three GPIOs to the header, although this has not been tested yet.

The board or as a kit (incl. [WIZ750SR](https://docs.wiznet.io/Product/S2E-Module/WIZ750SR)) can be purchased [here](https://www.tindie.com/products/nikolai2111/raspberry-pi-uart-to-ethernet-adapter/). The board is available with three power supply options (power supply not inlcuded):
* [Barrel Jack 2.1x5.5 mm](https://www.digikey.com/en/products/detail/cui-devices/PJ-037A/1644545)
* [USB Micro](https://www.digikey.de/de/products/detail/amphenol-cs-fci/10118194-0001LF/2785389)
* [USB C](https://www.digikey.ch/de/products/detail/gct/USB4125-GF-A/13547388)

![Front](doc/images/Front.jpg)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Built With

* [<img src="https://upload.wikimedia.org/wikipedia/commons/5/59/KiCad-Logo.svg" alt="drawing" width="50"/>][Kicad-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

### Prerequisites
* [Home Assistant](https://www.home-assistant.io/) is running
* [Z-Wave JS UI](https://www.home-assistant.io/integrations/zwave_js/) installed
* [WIZnet-S2E-Tool-GUI](https://github.com/Wiznet/WIZnet-S2E-Tool-GUI) downloaded

### Configure WIZ750SR
1. Open the [WIZnet-S2E-Tool-GUI](https://github.com/Wiznet/WIZnet-S2E-Tool-GUI)
2. Click `Device Search`
3. Select device with double click
4. Set the `Basic Settings` as shown in the picture below
   
![Basic Settings](doc/images/WIZnet-S2E-Tool-GUI.png)

### Confgure Z-Wave JS UI
1. Open [Home Assistant](homeassistant.local)
2. Open `Add-ons`
3. Click on `Z-Wave JS UI`
4. Start the add-on, if it's not running yet
5. Click on `OPEN WEB UI`
6. Go to `Settings`
7. Go to `Z-Wave`
8. And enter the IP and port below the `Serial Port` as shown in the picture blow. Use the scheme `tcp://your-ip:port`

![Serial Port](doc/images/Serial-Port.png)



<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

* [ ] Test more than one device
* [ ] Offer [WIZ750SR](https://docs.wiznet.io/Product/S2E-Module/WIZ750SR) in the shop
* [ ] Offer PoE adapter in the shop

See the [open issues](https://github.com/nikolai2111/RaspberryPi-UART_Ethernet_Adapter/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the [CERN-OHL-P](LICENSE) License. See `LICENSE` for more information. The license for all other sources remains the same and is still valid.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Nikolai Zoller - [nikolai.zoller@hotmail.com](mailto:nikolai.zoller@hotmail.com)

Project Link: [https://github.com/nikolai2111/RaspberryPi-UART_Ethernet_Adapter](https://github.com/nikolai2111/RaspberryPi-UART_Ethernet_Adapter)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

The main concept was initially proposed by an anonymous colleague. The development, production, and sale are carried out with their consent.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

Source: [Best-README-Template](https://github.com/othneildrew/Best-README-Template)

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/nikolai2111/RaspberryPi-UART_Ethernet_Adapter.svg?style=for-the-badge
[contributors-url]: https://github.com/nikolai2111/RaspberryPi-UART_Ethernet_Adapter/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/nikolai2111/RaspberryPi-UART_Ethernet_Adapter.svg?style=for-the-badge
[forks-url]: https://github.com/nikolai2111/RaspberryPi-UART_Ethernet_Adapter/network/members
[stars-shield]: https://img.shields.io/github/stars/nikolai2111/RaspberryPi-UART_Ethernet_Adapter.svg?style=for-the-badge
[stars-url]: https://github.com/nikolai2111/RaspberryPi-UART_Ethernet_Adapter/stargazers
[issues-shield]: https://img.shields.io/github/issues/nikolai2111/RaspberryPi-UART_Ethernet_Adapter.svg?style=for-the-badge
[issues-url]: https://github.com/nikolai2111/RaspberryPi-UART_Ethernet_Adapter/issues
[license-shield]: https://img.shields.io/github/license/nikolai2111/RaspberryPi-UART_Ethernet_Adapter.svg?style=for-the-badge
[license-url]: https://github.com/nikolai2111/RaspberryPi-UART_Ethernet_Adapter/blob/master/LICENSE.txt
[Kicad-logo]: https://upload.wikimedia.org/wikipedia/commons/5/59/KiCad-Logo.svg
[Kicad-url]: https://www.kicad.org/
