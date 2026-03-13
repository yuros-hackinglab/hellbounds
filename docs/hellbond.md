# Hellbound

# 1. Background

Project Hellbound aims to provide a comprehensive technical guide for building a self-hosted music server on Linux using the Music Player Daemon (MPD), addressing the need for data privacy and total control over personal audio libraries in an era of commercial streaming dominance. By leveraging the lightweight and stable architecture of MPD, this documentation offers a structured approach to configuring a high-performance, resource-efficient environment that allows users to manage and stream their media assets with complete digital sovereignty.

---

# 2. Spesification

For this research, we are utilizing devices with the following specifications:

| Type    | Spesification                                                |
| ------- | ------------------------------------------------------------ |
| RAM     | 4GB DDR4 SDRAM                                               |
| CPU     | Intel Celeron® N5100 Quad-core (4 Core™) 1.10 GHz            |
| Storage | 256 GB NVMe                                                  |
| Graphic | Intel® UHD Graphics                                          |
| Screen  | 14 inch, Full HD (1920 x 1080)                               |

For this research, we are using some distros linux for testing:

| Distro       |
| ------------ |
| Arch Linux   |
| Alpine Linux |
| Alma Linux   |
| Debian Linux |
| Ubuntu Linux |

The following applications were used to support this research on linux:

| Apps     | Version                 |
| -------- | ----------------------- |
| MPD      | 0.24.9-1                |
| mpc      | 0.35-1                  |
| rmpc     | 0.11.0-2                |
| pms      | 2.3.0                   |
| ncmpcpp  | 0.10.1-6                |
| inori    | 3.0.0                   |
| gomp     | 1.0.9                   |
| clerk    | 4.0.5-1                 |
| vimpc    | 0.09.2                  |
| mmtc     | 0.3.2                   |
| nncmpp   | 2.1.1                   |
| ncmpy    | 1.5.7                   |

---

# 3. Methods

The team executed a two-phase research process: document analysis, video research, and field research to validate the gathered data.

## 3.1. Research Data

1. Collecting information installation OS via documents.
2. Collecting information installation MPD on OS via documents.
3. Collecting information configuration video content.

## 3.3. Implementation Phase

1. Alpha development
2. Alpha testing
3. Beta development
4. Beta testing
5. Documentation

---

# 4. Result

In this chapter, we present the results of our comprehensive testing and research to inform our system development.

## 4.1. Research Data

### 4.1.1 Installation OS Research

The table below summarizes the findings from our document research on OS installation for minimun MPD server.

| Distro          | Source                                                                                                                                                                                                                                                  |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Alma Linux      | [link](https://wiki.almalinux.org/documentation/installation-guide.html#installation) |
| Arch Linux      | [link](https://wiki.archlinux.org/title/Installation_guide), [link](https://www.tauceti.blog/posts/virtualization-with-archlinux-qemu-kvm-part-4/) |
| Debian Linux    | [link](https://www.wikihow.com/Install-Debian), [link](https://www.debian.org/doc/manuals/debian-handbook/sect.installation-steps.id.html)         |
| Ubuntu Linux    | [link](https://ubuntu.com/tutorials/install-ubuntu-desktop#1-overview), [link](https://www.nesabamedia.com/cara-install-linux-ubuntu/)             |

The table below summarizes the findings from our video research on OS installation for minimun MPD server.

| Distro          | Source                                                                                                        |
| --------------- | ------------------------------------------------------------------------------------------------------------- |
| Alma Linux      | [link](https://youtu.be/8WYgynP8VJ8?si=_5CIDYEHiMRDnFd9)                                                      |
| Alpine Linux    | [link](https://youtu.be/xavrc3am3h0?si=ADfB6oF5eN6Zj7qg)                                                      |
| Arch Linux      | [link](https://www.youtube.com/watch?v=cN_a7NgBWX8), [link](https://youtu.be/UJaPDeA1ouo?si=niSe1O4_6YnY8Wy1) |

### 4.1.2 Installation MPD Research

The table below outlines the findings from our document research regarding the installation MPD music server.

| Distro          | Source                                                                                                                                                                                                                                                  |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Alma Linux      | [link](https://computingforgeeks.com/how-to-configure-mpd-and-ncmpcpp-on-linux/), [link](https://mpd.fandom.com/wiki/Install#Fedora_Install_Procedure), [link](https://rhel.pkgs.org/8/rpmfusion-free-updates-x86_64/mpd-0.23.15-1.el8.x86_64.rpm.html) |
| Alpine Linux    | [link](https://ipv6.rs/tutorial/Alpine_Linux_Latest/mpd/)                                                                                                                                                                                               |
| Arch Linux      | [link](https://wiki.archlinux.org/title/Music_Player_Daemon)                                                                                                                                                                                            |
| Debian Linux    | [link](https://mpd.readthedocs.io/en/stable/user.html), [link](https://wiki.debian.org/mpd)                                                                                                                                                             |
| Ubuntu Linux    | [link](https://berdasi.blog.amikom.me/tutorial-install-ncmpcpp/), [link](https://gmpc.fandom.com/wiki/MPD_INSTALL_USER_SERVICE_UBUNTU)                                                                                                                  |

### 4.1.3 Configuration 

The table below summarizes the document research on MPD configuration.

| Distro          | Source                                                                                                                                                                                    |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Alma Linux      | [link](https://mpd.fandom.com/wiki/Configuration)                                                                                                                                         |
| Arch Linux      | [link](https://shendinotes.wordpress.com/2015/01/11/install-setup-mpd-ncmpcpp-di-arch-linux/), [link](https://forum.endeavouros.com/t/beginner-s-guide-to-setting-up-and-using-mpd/16831) |
| Debian Linux    | [link](https://wiki.debian.org/mpd#Configuration), [link](https://addy-dclxvi.github.io/post/configuring-ncmpcpp/)                                                                        |  
| Ubuntu Linux    | [link](https://help.ubuntu.com/community/MPD#Configuring_MPD_to_run_as_a_system_service), [link](https://gmpc.fandom.com/wiki/MPD_INSTALL_USER_SERVICE_UBUNTU)                            |

## 4.2. Pelaksanaan Eksperimen
This section explains the experimental implementation of MPD (Music Player Daemon) and MPC (Music Player Client). The purpose of this experiment is to test how MPD operates as an audio server and how MPC interacts with it as a command-line client.

The documentation in this section covers several main stages of the experiment, including installation, configuration, directory preparation, and service management.
### 4.2.1 Arch Linux
### 4.2.1.1 Installation Process

This stage explains the installation of required packages needed to run MPD with a modern Linux audio stack.

The packages installed during this experiment include:

| Package | Description |
|--------|-------------|
| **mpd** | Music Player Daemon used as the main music server |
| **pipewire** | Modern Linux audio server |
| **pipewire-pulse** | PulseAudio compatibility layer |
| **pipewire-alsa** | ALSA compatibility layer |
| **pipewire-jack** | JACK audio compatibility |
| **wireplumber** | PipeWire session manager |

Installation was performed using the Arch Linux package manager **pacman**.

### 4.2.1.2 Directory Preparation
MPD requires several directories to store music files and operational data such as playlists, logs, and database files. These directories were created manually within the user's home directory.

The following directory structure was used during the experiment:

Directory	Purpose
|path|function|
|---|---|
| /home/[user]/music |	Storage location for music files |
| /home/[user]/.config/mpd/playlists |	Storage location for playlists |
| /home/[user]/.config/mpd/logs |	Storage location for log files |


Example commands used to create the directories:

```
mkdir /home/[user]/music
```
```
mkdir /home/[user]/.config/mpd/playlists
```
```
mkdir /home/[user]/.config/mpd/logs
```
Replace [user] with the username used on your system.

Creating this directory structure allows MPD to properly manage the music library and store runtime information.
### 4.2.1.3 Configuration
MPD is configured using the mpd.conf configuration file. This file defines how MPD accesses the music library, where metadata is stored, and how the daemon communicates with client applications.

The configuration file was edited using a text editor.
```
nvim /home/[user]/mpd/mpd.conf
```
### Core Configuration Parameters

| Parameter | Description |
| :--- | :--- |
| `music_directory` | Location of the music library |
| `playlist_directory` | Directory used to store playlist files |
| `db_file` | Database file for indexing music |
| `log_file` | Log file used to record MPD activity |
| `pid_file` | Stores the process ID of the MPD daemon |
| `state_file` | Stores playback state information |
| `sticker_file` | Metadata storage used by MPD |
| `bind_to_address` | Network interface used by MPD |
| `port` | Port used for MPD client communication |

Example configuration used in the experiment:
```
music_directory "/home/[user]/music"
playlist_directory "/home/[user]/.config/mpd/playlists"
db_file            "/home/[user]/.config/mpd/database"
log_file           "/home/[user]/.config/mpd/log"
pid_file           "/home/[user]/.config/mpd/pid"
state_file         "/home/[user]/.config/mpd/state"
sticker_file       "/home/[user]/.config/mpd/sticker.sql"
bind_to_address    "any"
port               "6600"

audio_output {
        type            "pipewire"
        name            "PipeWire Sound Server"
}
```
This configuration enables MPD to output audio through the PipeWire sound server, which is commonly used in modern Linux audio environments.

### 4.2.1.3 Service Management

MPD services are managed using systemd, the default service manager used in Arch Linux.

MPD can operate in two different modes:

Mode	Description
User Mode	Runs under the user's session (recommended for desktop systems)
System Mode	Runs as a global system service (recommended for headless servers)

### 4.2.1.3.1 User Mode (Recommended)

User mode allows MPD to run under the current user environment. This mode gives MPD direct access to the user's home directory and music library.

Enable the service so it starts automatically when the user logs in:
```
systemctl --user enable mpd
```
Start the service immediately:
```
systemctl --user start mpd
```
Check the status of the service:
```
systemctl --user status mpd
```
Enable the required PipeWire audio services:
```
systemctl --user --now enable pipewire pipewire-pulse wireplumber
```
#### 4.2.1.3.2 System Mode

System mode allows MPD to run as a system-level service controlled by the operating system.

Enable the service to start automatically during system boot:
```

sudo systemctl enable mpd
```
Start the service manually:
```
sudo systemctl start mpd
```
Check the service status:
```
sudo systemctl status mpd
```
Enable PipeWire services globally:
```
sudo systemctl --global enable pipewire pipewire-pulse wireplumber
```
5. Experiment Verification

The final stage of the experiment involves verifying that the MPD server operates correctly.

Verification procedures include:

Checking that the MPD service is active

Ensuring that PipeWire audio services are running

Connecting to the MPD server using the MPC client

Testing playback commands from the terminal

Example commands used for testing:

mpc update
mpc listall
mpc add <music-file>
mpc play

If the commands execute successfully and audio playback occurs without errors, the MPD implementation is considered successfully deployed.

### 4.2.2 Alma Linux
### 4.2.2.1. Pre-Installation

Before installing MPD and the required audio components, several system preparation steps were performed to enable repositories and update the AlmaLinux release metadata.

These steps ensure that the system has access to the necessary repositories and updated package information.

Enable the CRB repository:

```
sudo dnf config-manager --set-enabled crb
```

Upgrade the AlmaLinux release package:
```
sudo dnf upgrade almalinux-release
```
Clean cached package metadata:
```
sudo dnf clean all
```
These steps prepare the system for installing additional repositories and dependencies.
### 4.2.2.2 Installation

The installation stage includes enabling additional repositories and installing the required packages.

### 4.2.2.2.1 Enable EPEL Repository

The Extra Packages for Enterprise Linux (EPEL) repository provides additional packages that are not included in the default AlmaLinux repositories.
```
sudo dnf update && sudo dnf install epel-release
```
### 4.2.2.2.2 Install Distribution GPG Keys

The system must verify packages using trusted GPG keys before installing packages from external repositories.
```
sudo dnf install distribution-gpg-keys
```
Import the RPMFusion GPG key:
```
sudo rpmkeys --import /usr/share/distribution-gpg-keys/rpmfusion/RPM-GPG-KEY-rpmfusion-free-el-$(rpm -E %rhel)
```
Verify the imported key:
```
gpg --show-keys --with-fingerprint /usr/share/distribution-gpg-keys/rpmfusion/RPM-GPG-KEY-rpmfusion-free-el-$(rpm -E %rhel)
2.3 Enable RPMFusion Repository
```
RPMFusion provides additional multimedia packages required for audio-related software.
```
sudo dnf --setopt=localpkg_gpgcheck=1 install https://mirrors.rpmfusion.org/free/el/rpmfusion-free-release-$(rpm -E %rhel).noarch.rpm
```
2.4 Install MPD and Audio Components

Once repositories are enabled, install MPD and PipeWire audio components.
```
sudo dnf update && sudo dnf install mpd pipewire pipewire-alsa pipewire-pulseaudio wireplumber
```
The installed components include:
| Package | Description |
| :--- | :--- |
| `mpd` | Music Player Daemon used as the main audio server |
| `pipewire` | Modern Linux multimedia server |
| `pipewire-alsa` | ALSA compatibility layer |
| `pipewire-pulseaudio` | PulseAudio compatibility |
| `wireplumber` | PipeWire session manager |
### 4.2.2.3 Configuration
### 4.2.2.3.1 Configuration File Locations
MPD requires several directories to store music files, playlists, and operational data.
During the experiment, the following directory structure was created inside the user home directory.

| Directory | Purpose |
| :--- | :--- |
| `/home/[user]/music` | Music library storage |
| `/home/[user]/.mpd/playlists` | Playlist storage |
| `/home/[user]/.mpd` | MPD configuration and runtime files |

Create the directories using the following commands:

```
mkdir /home/[user]/music
mkdir -p /home/[user]/.mpd/playlists
```
Create runtime files used by MPD:
```
touch /home/[user]/.mpd/{mpd.db,mpd.log,mpd.pid,mpdstate}
```
Berikut adalah format Markdown (.md) untuk bagian parameter konfigurasi dan contoh file mpd.conf yang Anda berikan:

### 4.2.2.3.1 Core Configuration Parameters

| Parameter | Description |
| :--- | :--- |
| `music_directory` | Directory containing music files |
| `playlist_directory` | Directory for storing playlists |
| `db_file` | Database file indexing the music library |
| `log_file` | File used for logging daemon activity |
| `pid_file` | Process ID file |
| `state_file` | Stores playback state |
| `bind_to_address` | Network interface for MPD |
| `port` | Port used by MPD clients |

Example configuration used in the experiment:

```
music_directory    "/home/[user]/music"
playlist_directory "/home/[user]/.mpd/playlists"
db_file            "/home/[user]/.mpd/mpd.db"
log_file           "/home/[user]/.mpd/mpd.log"
pid_file           "/home/[user]/.mpd/mpd.pid"
state_file         "/home/[user]/.mpd/mpdstate"
bind_to_address    "any"
port               "6600"

audio_output {
        type            "pipewire"
        name            "PipeWire Sound Server"
}
```
### 4.2.2.4 Service Management

MPD services are controlled using systemd, which is the default service manager in AlmaLinux.
MPD can operate in two modes:

| Mode | Description |
| :--- | :--- |
| User Mode | Runs under the user's session (recommended for desktop environments) |
| System Mode | Runs as a system-level service |

### 4.2.2.4.1 User Mode (Recommended)

In this experiment, MPD was executed in user mode so it can directly access the user music library.

Disable the default system socket:

```
sudo systemctl disable mpd.socket
```
Enable the user service:

```
systemctl enable --user mpd.socket
```
Start the user service:
```

systemctl start --user mpd.socket
```
Enable the PipeWire audio services:
```
Bash
systemctl --user --now enable pipewire wireplumber
```
This configuration ensures that MPD starts automatically when the user session begins.

### 4.2.3.4 Experiment Verification
The final stage of the experiment verifies that the MPD server is functioning correctly.
Verification steps include:

Ensuring the MPD socket service is active

Confirming PipeWire and WirePlumber services are running

Connecting to the MPD server using MPC

Testing playback commands

Example testing commands:
```
Bash
mpc update
mpc listall
mpc add <music-file>
mpc play
```
If the commands execute successfully and audio playback occurs, the MPD server implementation on AlmaLinux is considered successful.
### 4.2.3 Alpine Linux
### 4.2.3.1 Installation Process

The first stage of the experiment involves installing the required packages for MPD and the audio subsystem.

The following packages were installed using Alpine's **apk package manager**:

| Package | Description |
|--------|-------------|
| **mpd** | Music Player Daemon used as the main audio server |
| **pulseaudio** | Audio server responsible for sound processing |
| **pulseaudio-utils** | Utility tools for managing PulseAudio |
| **alsa-plugins-pulse** | ALSA compatibility plugin for PulseAudio |
| **neovim** | Text editor used to configure MPD |

Installation command used during the experiment:

```bash
sudo apk add mpd pulseaudio pulseaudio-utils alsa-plugins-pulse neovim
```
### 4.2.3.2 Directory Preparation

MPD requires a directory structure for storing music files, playlists, and runtime database information.
The following directories were created during the experiment:

| Directory | Purpose |
| :--- | :--- |
| `/home/[user]/music` | Storage location for music files |
| `/home/[user]/.config/mpd/playlists` | Playlist storage directory |
| `/home/[user]/.config/mpd` | MPD configuration and database files |

Create the directories using the following commands:

```bash
mkdir /home/[user]/music
mkdir -p /home/[user]/.config/mpd/playlists
```
Create the MPD database file:
```
Bash
touch /home/[user]/.config/mpd/mpd.db
```
-> Note: Replace [user] with the username used on your system.

These directories allow MPD to manage the music library and store metadata required for playback operations.
### 4.2.3.3 Configuration
MPD configuration is defined in the mpd.conf file. This configuration determines where music files are stored, how MPD manages its database, and how the server communicates with clients.Edit the configuration 
```
nvim /home/[user]/.config/mpd/mpd.conf
```
| Parameter | Description |
| :--- | :--- |
| `music_directory` | Directory containing music files |
| `playlist_directory` | Directory used to store playlists |
| `log_file` | Logging output location |
| `pid_file` | Process ID file |
| `state_file` | Playback state file |
| `sticker_file` | Metadata storage file |
| `bind_to_address` | Network address used by MPD |
| `port` | Communication port for MPD clients |<

Example configuration used in the experiment:
```
music_directory         "/home/[user]/music"
playlist_directory      "/home/[user]/.config/mpd/playlists"
log_file                "syslog"
pid_file                "/home/[user]/.config/mpd/mpd.pid"
state_file              "/home/[user]/.config/mpd/mpd.state"
sticker_file            "/home/[user]/.config/mpd/mpd.sticker"
bind_to_address         "any"
port                    "6600"
log_level               "default"
auto_update             "yes"

database {
    plugin "simple"
    path "/home/[user]/music/.config/mpd/mpd.db"
}

audio_output {
    type            "pulse"
    name            "Pulse"
}
```
In this configuration, MPD uses PulseAudio as the audio backend, allowing audio playback through the system's sound server.
### 4.2.4.4 Service ManagementMPD 
MPD services are controlled using systemd. MPD can operate in two modes:
| Mode | Description |
| :--- | :--- |
| User Mode | Runs under the user's session (recommended for desktop environments) |
| System Mode | Runs as a system-level service |
 
### 4.2.4.3.1 User Mode
In this experiment, MPD was executed in user mode so it can directly access the user music library.

Disable the default system socket:
```
Bash
sudo systemctl disable mpd.socket
```
Enable the user service:
```
Bash
systemctl enable --user mpd.socket
```
Start the user service:
```
Bash
systemctl start --user mpd.socket
```
Enable the PipeWire audio services:
```
Bash
systemctl --user --now enable pipewire wireplumber
```
This configuration ensures that MPD starts automatically when the user session begins.

### 4.2.3.5 Experiment Verification
The final stage of the experiment verifies that the MPD server is functioning correctly.
Verification steps include:

Ensuring the MPD socket service is active

Confirming PipeWire and WirePlumber services are running

Connecting to the MPD server using MPC

Testing playback commands

Example testing commands:
```
Bash
mpc update
mpc listall
mpc add <music-file>
mpc play
```
If the commands execute successfully and audio playback occurs, the MPD server implementation is considered successful.


# 5. Conclusion

- 

# 6. Reference
