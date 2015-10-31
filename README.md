<!--
# README.md
# EugeneKay/subsonic
-->
Subsonic
========

What is Subsonic?
-----------------

Subsonic is a free, web-based media streamer, providing ubiqutious access to your music. Use it to share your music with friends, or to listen to your own music while at work. You can stream to multiple players simultaneously, for instance to one player in your kitchen and another in your living room.

Subsonic is designed to handle very large music collections (hundreds of gigabytes). Although optimized for MP3 streaming, it works for any audio or video format that can stream over HTTP, for instance AAC and OGG. By using transcoder plug-ins, Subsonic supports on-the-fly conversion and streaming of virtually any audio format, including WMA, FLAC, APE, Musepack, WavPack and Shorten.

If you have constrained bandwidth, you may set an upper limit for the bitrate of the music streams. Subsonic will then automatically resample the music to a suitable bitrate.

In addition to being a streaming media server, Subsonic works very well as a local jukebox. The intuitive web interface, as well as search and index facilities, are optimized for efficient browsing through large media libraries. Subsonic also comes with an integrated Podcast receiver, with many of the same features as you find in iTunes.

Based on Java technology, Subsonic runs on most platforms, including Windows, Mac, Linux and Unix variants.


License
-------

Subsonic is free software and licensed under the [GNU General Public License version 3](http://www.gnu.org/copyleft/gpl.html).


About
-----

Subsonic is developed by [Sindre Mehus](mailto:sindre@activeobjects.no). He lives in Oslo, Norway and works as a Java software consultant.

This repository is maintained by [Eugene E. Kashpureff Jr](mailto:eugene@kashpureff.org) and provides an unofficial version of Subsonic which does not contain the Licensing code checks present in the official builds. In addition, some minor changes to the repository have been made to assist in the building of a fully-free version for your own use. Any downloads associated with this repo are provided without warranty or guarantee, and your use of such files is at your own risk.

The official homepage of Subsonic can be found [here](http://www.subsonic.org/).

Usage
-----

A WAR compiled from the latest tag is provided on the [Releases page](https://github.com/EugeneKay/subsonic/releases), which can be installed to a Tomcat webapps/ directory, and should "just work". Please see the [INSTALL document](https://github.com/EugeneKay/subsonic/blob/release/INSTALL.md) for instructions on building from source and installation.
