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
[![Instagram][ig-shield]][ig-url]
[![Instagram][yt-shield]][yt-url]
[![PCBWAY][sponsor-shield]][sponsor-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://makingdevices.com/links/">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

<h3 align="center">Making Devices</h3>

  <p align="center">
    Open Source projects where we struggle with engineering, electronics, coding and who knows what else... MakerAxe-lite is the foundation for new BTC miners and exciting hardware in the future. 
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
      <a href="#Build-one">Build one</a>
      <ul>
      </ul>
    </li>
    <li><a href="#goals">Goals</a></li>
    <li><a href="#features">Features</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#tools">Tools</a></li>
    <li><a href="#Sponsor">Sponsor</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

[![Bytes Counter Shot][product-screenshot]](https://makingdevices.com/)

```
Open Source is Intrinsic to Bitcoin
```

This is the motto you will see at the top of the [Bitaxe repository](https://github.com/skot/bitaxe), and it’s the reason Why MakerAxe-Lite was created.

MakerAxe Lite is the first attempt to extract the essentials of Bitaxe, reduce it to the minimum, and create a foundation for building new and exciting hardware in the future.

The project modifies the original hardware with the following changes:

1. The screen is not needed, as you now have AxeOS. Therefore, the screen will be removed (DNP) to reduce energy consumption and costs.
2. The 4-layer PCB is reduced to a 2-layer PCB, decreasing the cost of the PCB.
3. The 5V barrel input connector is replaced with USB PD. The voltage (20V, 15V, or 12V) is yet to be decided. This change ensures compatibility with recycled and reused phone or laptop chargers.
4. A LED has been added for blinking status and debug purposes.
5. Software compatibility with the stock [ESP-miner AxeOS](https://github.com/skot/ESP-Miner) (aside from the LED indicator).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

[![Microcontroller][ESP32]][ESP32-url]
[![](https://dcbadge.vercel.app/api/server/3E8ca2dkcC)](https://discord.gg/3E8ca2dkcC)
[![Kicad][kicad-shield]][kicad-url]
[![SPONSOR][sponsor-icon]][sponsor-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->

## Build one
The project is yet to be finished. Should you want to reproduce it, be careful. 

1. Get the gerber files for the latest version: [MakerAxe-lite V025](/Gerber/makeraxe-litev025.zip) 
2. Send them to a PCB manufacturer ([Our Sponsor is PCBWAY][sponsor-url])
3. Schematic (?)

YET TO BE COMPLETED.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GOALS -->
## Goals
- **Standalone**: can mine directly to your pool over WiFi. No External computer needed.
- **Embedded**: low cost, low maintenance, high availability, high reliability, low power.
- **ASIC**: based on the very, very efficient BM1366 from Bitmain.
- **Versatile**: solo/pool mining, autotune power/heat/efficiency.
- **Open Source**: All design files are provided.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- FEATURES -->
## Features
- **ESP32-S3-WROOM-1** wifi microcontroller on board
- **TI TPS40305** buck regulator steps down the input voltage to power the BM1366
- **Maxim DS4432U+** current DAC digitally adjusts the BM1366 core voltage from 0.04V to 2.4V
- **TI INA260** power meter measures the input voltage and current of the miner
- **Microchip EMC2101** PWM controls the fan and monitors tach output. BM1366 doesn't support die temp, but we have it placed super close to the ASIC so we can use the internal temp feature.
- Enjoy :D!

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ROADMAP -->
## Roadmap

- [X] Design the V025 prototype board.
- [ ] Complete the schematic and BoM files with LCSC&DK codes. 
- [ ] Order/Assembly the V025 prototype board.
- [ ] Validate V025 revision
  - [ ] Check that USB PD Works (12V, 15V, 20V)
  - [ ] Check the ESP32 can be programmed. 
  - [ ] AxeOS Self-testing is OK.
  - [ ] Solder the ASIC and check temperatures.
  - [ ] Characterice the overall efficiency.
  - [ ] Stress the buck converter to see if it is enough for next projects.
  - [ ] Explore alternatives to eliminate 5V rail.
  - [ ] Develop firmware so the LED can be used. Merge to ESP-miner if possible
- [ ] Validate the complete design + order PCBA 


See the [open issues](https://github.com/makingdevices/MakerAxe-lite/issues) for a full list of proposed features (and known issues).

State: Project <b>ONGOING</b> - 26/12/2024

Priority: <b>High</b>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- LICENSE -->
## License

Distributed under three licenses:
- [Hardware](/License/HW_cern_ohl_s_v2.pdf)
- [Software](/License/SW_GPLv3.0.txt)
- [Documentation](/License/Documentation_CC-BY-SA-4.0.txt)

OSHWA License: Not Finished

[![GPL v3 License][license-shield]][license-url] 
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

Making Devices - [@MakingDevices](https://www.instagram.com/makingdevices/)

Project Link: [https://github.com/makingdevices/MakerAxe-lite](https://github.com/makingdevices/MakerAxe-lite)

Other Links: [LinkTree](https://makingdevices.com/links/)

<!-- Tools -->
## Tools

During the realization of this project, you may need tools to assemble the PCB, solder components, and more.

These are the tools we've tested and currently have in our lab, so feel free to check them out if needed. Keep in mind that, even if prices are the same, you can support us in continuing to develop projects like this through the Amazon Influencer Program. Thank you!

- Microscope for smd soldering: [LinkMicro 246ms](https://amzn.to/408Ppbb)
- My solder paste: [ChipQuik LowTemp](https://amzn.to/3BA9Rsn)
- My soldering station with power supply: [Yihua 853D](https://amzn.to/4fzq3ry)


<!-- Sponsor -->
## Sponsors

[PCBWAY](https://www.pcbway.com/?from=makingdevices) is the most professional PCB manufacturer for prototyping and low-volume production to work with in the world. With more than a decade in the field, They are committed to meeting the needs of their customers from different industries in terms of quality, delivery, cost-effectiveness and any other demanding requests. As Sponsor of Making Devices, they will be in charge of all the PCBs for MDV, allowing both of us to grow together in a long term partnership. We hope you take them into account for your both personal and professional prototypes or products.

[![Sponsor Shot][sponsor-pcb-1]][sponsor-url]
[![Sponsor Shot][sponsor-pcb-2]][sponsor-url]


<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/makingdevices/MakerAxe-lite.svg?style=for-the-badge
[contributors-url]: https://github.com/makingdevices/MakerAxe-lite/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/makingdevices/MakerAxe-lite.svg?style=for-the-badge
[forks-url]: https://github.com/makingdevices/MakerAxe-lite/network/members
[stars-shield]: https://img.shields.io/github/stars/makingdevices/MakerAxe-lite.svg?style=for-the-badge
[stars-url]: https://github.com/makingdevices/MakerAxe-lite/stargazers
[issues-shield]: https://img.shields.io/github/issues/makingdevices/MakerAxe-lite.svg?style=for-the-badge
[issues-url]: https://github.com/makingdevices/MakerAxe-lite/issues
[license-shield]: /images/license.png
[license-url]: https://github.com/makingdevices/MakerAxe-lite/tree/main/License
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/company/making-devices/
[sponsor-shield]: https://img.shields.io/badge/SPONSOR-PCBWAY-black.svg?style=for-the-badge&colorB=1200
[sponsor-url]: https://www.pcbway.com/?from=makingdevices
[sponsor-screenshot]: /images/PCB_sponsor.png
[sponsor-pcb-1]: /images/pixelbytes_pcb1.JPG
[sponsor-pcb-2]: /images/pixelbytes_pcb2.JPG
[sponsor-wurth-1]: /images/wurth_1.gif
[sponsor-wurth-3]: /images/wurth_3.jpg
[sponsor-url-wurth]: https://www.we-online.com/en
[product-screenshot]: images/screenshot.jpg
[ESP32]: https://img.shields.io/badge/ESP32_S3-7c0a02?style=for-the-badge
[ESP32-url]: https://www.espressif.com/sites/default/files/documentation/esp32-s3-wroom-1_wroom-1u_datasheet_en.pdf
[kicad-shield]: https://img.shields.io/badge/kicad-0b03fc?style=for-the-badge&logo=kicad&logoColor=white
[kicad-url]: https://www.kicad.org/
[YT-screenshot]: images/YT_assembly.PNG
[sponsor-icon]:  https://img.shields.io/badge/-PCBWAY-black.svg?style=for-the-badge&colorB=1200
[ig-shield]: https://img.shields.io/badge/instagram-a83297?style=for-the-badge&logo=instagram&logoColor=white
[ig-url]: https://www.instagram.com/makingdevices/
[yt-shield]: https://img.shields.io/badge/youtube-ff0000?style=for-the-badge&logo=youtube&logoColor=white
[yt-url]: https://www.youtube.com/@MakingDevices
[MPLAB-C]: https://img.shields.io/badge/MPLAB%20C18-DD0031?style=for-the-badge&logo=C&logoColor=white
[Arduino]: https://img.shields.io/badge/ARDUINO-00878F?style=for-the-badge&logo=arduino&logoColor=white
[wurth-icon]: https://img.shields.io/badge/Wurth%20elektronik-FF0031?style=for-the-badge&logoColor=white
[Arduino-url]: https://www.arduino.cc/
[MPLAB-C-url]: https://www.microchip.com/en-us/development-tool/SW006011
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
