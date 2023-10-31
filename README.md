# KitMaker

KitMaker is a free and open-source environment for building executable Tcl interpreters (tclkits), with and without Tk.

It leverages [Bawt](https://www.tcl3d.org/bawt/index.html) in order to build tclkits for various operating systems, cpus and architectures.

## Acknowledgments

This project was made possible due to the hard work of a lot of people.
- All the [Tcl/Tk](https://www.tcl.tk/) developers.
- All the [Tclkit](https://www.equi4.com/tclkit/) developers.
- The developer of Bawt, Paul Obermeier.
- and many more...

## Install

Clone this repository.

```sh
git clone https://github.com/robertocalabrese/KitMaker.git
```

Follow the istruction for your operating system:

<details>

<summary>Linux</summary>

#### Requirements

Any Linux distribution should suffice.

#### Dependancies

Please note that some setups may require additional dependencies. If something is still found to be missing, please open an issue.

##### Arch Linux
```sh
pacman -S --needed base base-devel
pacman -S --needed cmake libx11 libxft libxss p7zip tcl
```

##### Debian/Ubuntu
```sh
apt install build-essential
apt install cmake libx11-dev libxft-dev libxss-dev p7zip tcl
```

##### Fedora
```sh
dnf group install "C Development Tools and Libraries" "Development Tools"
dnf install cmake libX11-devel libXft-devel libXscrnSaver-devel p7zip tcl
```

##### openSUSE
```sh
zypper install -t pattern devel_basis
zypper install cmake libX11-devel libXft-devel libXss-devel p7zip tcl
```

##### Other [^1]
If your distribution is derived from one of the above, follow the same instructions, otherwise use your distribution package manager to install the default building system (something equivalent to the `Ubuntu` package `build-essential`) and the `cmake`, `libx11`, `libxft`, `libxss`, `p7zip` and `tcl` packages (your distribution may call them differently, modifying them accordingly).

#### Usage

Open a terminal window, go inside the KitMaker folder and run one of the following command:

```sh
./linux.sh        # To display the help

./linux.sh 8.6.6  # To create tclkits at 32 or 64 bits that includes Tcl 8.6.6 (with and without Tk 8.6.6)
./linux.sh 8.6.7  # To create tclkits at 32 or 64 bits that includes Tcl 8.6.7 (with and without Tk 8.6.7)
./linux.sh 8.6.8  # To create tclkits at 32 or 64 bits that includes Tcl 8.6.8 (with and without Tk 8.6.8)
./linux.sh 8.6.9  # To create tclkits at 32 or 64 bits that includes Tcl 8.6.9 (with and without Tk 8.6.9)
./linux.sh 8.6.10 # To create tclkits at 32 or 64 bits that includes Tcl 8.6.10 (with and without Tk 8.6.10)
./linux.sh 8.6.11 # To create tclkits at 32 or 64 bits that includes Tcl 8.6.11 (with and without Tk 8.6.11)
./linux.sh 8.6.12 # To create tclkits at 32 or 64 bits that includes Tcl 8.6.12 (with and without Tk 8.6.12)
./linux.sh 8.6.13 # To create tclkits at 32 or 64 bits that includes Tcl 8.6.13 (with and without Tk 8.6.13)
./linux.sh 8.7.a5 # To create tclkits at 32 or 64 bits that includes Tcl 8.7.a5 (with and without Tk 8.7.a5)
./linux.sh 8.7.b1 # To create tclkits at 32 or 64 bits that includes Tcl 8.7.b1 (with and without Tk 8.7.b1)
```

Depending on your Linux architecture, the resulting tclkits will be located at:

```sh
build/Linux/x86/Release/Distribution/opt/Tcl/bin # For Linux environment at 32 bits
build/Linux/x64/Release/Distribution/opt/Tcl/bin # For Linux environment at 64 bits
```

#### Testing

KitMaker has been tested in the following Linux operative systems, cpus and architecture (from Tcl 8.6.6 to Tcl 8.7.b1):

| OS                  | CPU   | ARCHITECTURE |
|---------------------|-------|--------------|
| Archlinux           | Amd   | 64 bit       |
| Archlinux           | Arm   | 64 bit       |
| Archlinux           | Intel | 64 bit       |
| Debian 12           | Amd   | 64 bit       |
| Debian 12           | Arm   | 64 bit       |
| Debian 12           | Intel | 64 bit       |
| Fedora 38           | Amd   | 64 bit       |
| Fedora 38           | Arm   | 64 bit       |
| Fedora 38           | Intel | 64 bit       |
| openSUSE Leap 15    | Amd   | 64 bit       |
| openSUSE Leap 15    | Arm   | 64 bit       |
| openSUSE Leap 15    | Intel | 64 bit       |
| openSUSE Tumbleweed | Amd   | 32 bit       |
| openSUSE Tumbleweed | Amd   | 64 bit       |
| openSUSE Tumbleweed | Arm   | 64 bit       |
| openSUSE Tumbleweed | Intel | 32 bit       |
| openSUSE Tumbleweed | Intel | 64 bit       |
| Ubuntu 22.04 LTS    | Amd   | 64 bit       |
| Ubuntu 22.04 LTS    | Arm   | 64 bit       |
| Ubuntu 22.04 LTS    | Intel | 64 bit       |
| Ubuntu 23.10        | Amd   | 64 bit       |
| Ubuntu 23.10        | Arm   | 64 bit       |
| Ubuntu 23.10        | Intel | 64 bit       |

</details>

<details>

<summary>MacOS</summary>

#### Requirements

A MacOS Ventura operating system or later [^2].

#### Dependancies

If you are using `MacPorts` as package manager, run the following command inside a terminal:

```sh
port install tcl xorg-server-devel
```

If you are using `Homebrew` as package manager, run the following command inside a terminal:

```sh
brew install tcl-tk xorg-server
```

> [!WARNING]
> The macos script defaults to the Tcl location of the `MacPorts` package manager. If your package manager is `Homebrew`, edit the script and modify the Tcl location accordingly.

#### Usage

Open a terminal window, go inside the KitMaker folder and run one of the following command:

```sh
./macos.sh        # To display the help

./macos.sh 8.6.6  # To create tclkits at 32 or 64 bits that includes Tcl 8.6.6 (with and without Tk 8.6.6)
./macos.sh 8.6.7  # To create tclkits at 32 or 64 bits that includes Tcl 8.6.7 (with and without Tk 8.6.7)
./macos.sh 8.6.8  # To create tclkits at 32 or 64 bits that includes Tcl 8.6.8 (with and without Tk 8.6.8)
./macos.sh 8.6.9  # To create tclkits at 32 or 64 bits that includes Tcl 8.6.9 (with and without Tk 8.6.9)
./macos.sh 8.6.10 # To create tclkits at 32 or 64 bits that includes Tcl 8.6.10 (with and without Tk 8.6.10)
./macos.sh 8.6.11 # To create tclkits at 32 or 64 bits that includes Tcl 8.6.11 (with and without Tk 8.6.11)
./macos.sh 8.6.12 # To create tclkits at 32 or 64 bits that includes Tcl 8.6.12 (with and without Tk 8.6.12)
./macos.sh 8.6.13 # To create tclkits at 32 or 64 bits that includes Tcl 8.6.13 (with and without Tk 8.6.13)
./macos.sh 8.7.a5 # To create tclkits at 32 or 64 bits that includes Tcl 8.7.a5 (with and without Tk 8.7.a5)
./macos.sh 8.7.b1 # To create tclkits at 32 or 64 bits that includes Tcl 8.7.b1 (with and without Tk 8.7.b1)
```

Depending on your MacOS architecture, the resulting tclkits will be located at:

```sh
build/Darwin/x86/Release/Distribution/opt/Tcl/bin # For MacOS environment at 32 bits (only for intel cpu at 32 bits)
build/Darwin/x64/Release/Distribution/opt/Tcl/bin # For MacOS environment at 64 bits (for intel cpu at 64 bits and apple silicons cpus)
```

#### Testing

KitMaker has been tested in the following MacOS operative systems, cpus and architecture [^3]:

| OS            | CPU           | ARCHITECTURE |
|---------------|---------------|--------------|
| MacOS Sonoma  | Apple Silicon | 64 bit       |
| MacOS Ventura | Apple Silicon | 64 bit       |

</details>

<details>

<summary>Windows</summary>

#### Requirements

KitMaker requires Windows 10 operating system or later [^4].

#### Dependancies

Download one or both the `gcc` compiler(s) listed below depending on your Windows architecture [^5]:

- [gcc 7.2.0 at 32 bit](https://www.tcl3d.org/bawt/download/Bootstrap-Windows/gcc7.2.0_i686-w64-mingw32.7z)
- [gcc 7.2.0 at 64 bit](https://www.tcl3d.org/bawt/download/Bootstrap-Windows/gcc7.2.0_x86_64-w64-mingw32.7z)

#### Usage

Open a command shell window, i.e. powershell, go inside the KitMaker folder and run one of the following command [^6].

```sh
./windows.bat            # To display the help

# x86 means 32 bits
./windows.bat x86 8.6.6  # To create tclkits at 32 bits that includes Tcl 8.6.6  (with and without Tk 8.6.6)
./windows.bat x86 8.6.7  # To create tclkits at 32 bits that includes Tcl 8.6.7  (with and without Tk 8.6.7)
./windows.bat x86 8.6.8  # To create tclkits at 32 bits that includes Tcl 8.6.8  (with and without Tk 8.6.8)
./windows.bat x86 8.6.9  # To create tclkits at 32 bits that includes Tcl 8.6.9  (with and without Tk 8.6.9)
./windows.bat x86 8.6.10 # To create tclkits at 32 bits that includes Tcl 8.6.10 (with and without Tk 8.6.10)
./windows.bat x86 8.6.11 # To create tclkits at 32 bits that includes Tcl 8.6.11 (with and without Tk 8.6.11)
./windows.bat x86 8.6.12 # To create tclkits at 32 bits that includes Tcl 8.6.12 (with and without Tk 8.6.12)
./windows.bat x86 8.6.13 # To create tclkits at 32 bits that includes Tcl 8.6.13 (with and without Tk 8.6.13)
./windows.bat x86 8.7.a5 # To create tclkits at 32 bits that includes Tcl 8.7.a5 (with and without Tk 8.7.a5)
./windows.bat x86 8.7.b1 # To create tclkits at 32 bits that includes Tcl 8.7.b1 (with and without Tk 8.7.b1)

# x64 means 64 bits
./windows.bat x64 8.6.6  # To create tclkits at 64 bits that includes Tcl 8.6.6  (with and without Tk 8.6.6)
./windows.bat x64 8.6.7  # To create tclkits at 64 bits that includes Tcl 8.6.7  (with and without Tk 8.6.7)
./windows.bat x64 8.6.8  # To create tclkits at 64 bits that includes Tcl 8.6.8  (with and without Tk 8.6.8)
./windows.bat x64 8.6.9  # To create tclkits at 64 bits that includes Tcl 8.6.9  (with and without Tk 8.6.9)
./windows.bat x64 8.6.10 # To create tclkits at 64 bits that includes Tcl 8.6.10 (with and without Tk 8.6.10)
./windows.bat x64 8.6.11 # To create tclkits at 64 bits that includes Tcl 8.6.11 (with and without Tk 8.6.11)
./windows.bat x64 8.6.12 # To create tclkits at 64 bits that includes Tcl 8.6.12 (with and without Tk 8.6.12)
./windows.bat x64 8.6.13 # To create tclkits at 64 bits that includes Tcl 8.6.13 (with and without Tk 8.6.13)
./windows.bat x64 8.7.a5 # To create tclkits at 64 bits that includes Tcl 8.7.a5 (with and without Tk 8.7.a5)
./windows.bat x64 8.7.b1 # To create tclkits at 64 bits that includes Tcl 8.7.b1 (with and without Tk 8.7.b1)
```

Depending on the architecture chosen ('x86' or 'x64'), the resulting two tclkits will be located at:

```sh
build/Windows/x86/Release/Distribution/opt/Tcl/bin # If you have choosen to build for 32 bit architecture.
build/Windows/x64/Release/Distribution/opt/Tcl/bin # If you have choosen to build for 64 bit architecture.
```

#### Testing

KitMaker has been tested in the following Windows operative systems, cpus and architecture (from Tcl 8.6.6 to Tcl 8.7.b1):

| OS                     | CPU   | ARCHITECTURE |
|------------------------|-------|--------------|
| Windows 10 Pro Edition | Amd   | 64 bit       |
| Windows 10 Pro Edition | Intel | 64 bit       |
| Windows 11 Pro Edition | Arm   | 64 bit       |

</details>

&nbsp;

[^1]: If you use KitMaker on any other distribution (not listed directly here), I would love to hear about so this section of the README can be updated.
[^2]: KitMaker might work on previous versions of MacOS as well, but I have no way of testing it. Please, let me know if it does so this section of the README can be updated.
[^3]: I do not own an `Intel` based MacOS to properly test KitMaker on it, but it should work as expected (from Tcl 8.6.6 to 8.7.b1).
Support for `Apple Silicon` cpus starts instead from Tcl 8.7.b1.
[^4]: KitMaker might work on previous versions of Windows as well, but I have no way of testing it. Please, let me know if it does so this section of the README can be updated.
[^5]: Users with Windows at 32 bit should download just the gcc at 32 bit. Users with Windows at 64 bit can choose to download both of them (tclkits for both architectures will be buildable), or just one of them (only tclkits with the same gcc architecture will be buildable).
[^6]: Windows at 32 bit should only run the `x86` example commands.
