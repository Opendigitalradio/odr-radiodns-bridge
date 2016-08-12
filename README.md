# odr-radiodns-bridge
Tools to bridge RadioDNS applications into the OpenDigitalRadio environment

This is beginnings of a toolset being developed to bridge RadioDNS applications (visuals, service and programme information)
into the OpenDigitalRadio environment.

Modules will provide functionality to:
* Read an odr-dabmux configuration file and locate RadioDNS applications for the services configured in it
* Bridge visuals from IP into DAB Slideshow
* Compile a DAB EPG for all services on the multiplex and transmit it as a packet mode channel

The current resolver takes the form:

  odr-radiodns-resolver configuration-file-name
  
and outputs a list of services that have RadioDNS visuals and service and programme information.
There are functions which return lists of services supporting slideshow, and lists of services for inclusion in a DAB EPG

Requirements:
- You'll need to install Sam Starling's pyradiodns library to locate the hosts providing RadioDNS services
python -m pip install pyradiodns

The resolver also uses a Boost Info file parser (from https://github.com/thecodemaiden/) and a RadioDNS SPI library
(from https://github.com/magicbadger/python-hybridspi) but these files are included.

