---
title: Abstract
---

# Abstract

Music Player Daemon (MPD) is a lightweight and flexible server-based audio system designed to manage and play music through a client–server architecture. This research aims to implement and evaluate MPD as a self-hosted music server across several Linux distributions, including Arch Linux, Alpine Linux, AlmaLinux, Debian Linux, and Ubuntu Linux. The experiment focuses on installation procedures, directory preparation, configuration of the `mpd.conf` file, and service management using systemd.

The implementation process begins with installing the required packages and preparing the necessary directory structures for storing music files, playlists, and runtime database information. Afterward, the MPD configuration is defined to determine music directories, metadata storage, and network communication settings. Audio output integration is configured using PipeWire to ensure compatibility with modern Linux audio systems. Service management is handled using systemd, allowing MPD to run in user mode for direct access to the user's music library.

Experimental verification is conducted by connecting to the MPD server using Music Player Client (MPC) and executing playback commands such as updating the music database, listing available tracks, adding songs to playlists, and starting playback. The results show that MPD operates consistently across different Linux distributions despite variations in package management systems and directory structures.

The study concludes that MPD provides an efficient, lightweight, and distribution-independent solution for building a personal music server. By leveraging the client–server architecture and open-source Linux ecosystem, users can maintain full control over their music libraries while ensuring stable and scalable audio playback management.

