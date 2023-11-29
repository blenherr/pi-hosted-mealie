# Install and setup instructions for scrutiny

- [Introduction](#introduction)
- [Installation](#installation)
- [Post installation](#post-installation)
- [Acknowledgment / Troubleshoot](#acknowledgment--troubleshoot)


## Introduction

![Scrutiny](https://github.com/AnalogJ/scrutiny) is an WebUI for smartd S.M.A.R.T monitoring with ![InfluxDB](https://www.influxdata.com) backend. 


## Installation

- Goto App Templates and click on "scrutiny".
- Click on "Show advanced options"
- Change host port to your needs
- Deploy the container


## Post installation

- Edit scrutiny container
- Click on "Capabilities"
- Enable "SYS_RAWIO"
- Click on "Runtime & Resources"
- Click on "add device"
- For example put "/dev/sda" in host and container field
- Add as many devices as you like
- Deploy the container and replace


## Acknowledgment / Troubleshoot

- GitHub: [https://github.com/AnalogJ/scrutiny](https://github.com/AnalogJ/scrutiny)
