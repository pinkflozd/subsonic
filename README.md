Subsonic
========

What is Subsonic?
-----------------

Subsonic is a free, web-based media streamer, providing ubiqutious access to your music. Use it to share your music with friends, or to listen to your own music while at work. You can stream to multiple players simultaneously, for instance to one player in your kitchen and another in your living room.

Subsonic is designed to handle very large music collections (hundreds of gigabytes). Although optimized for MP3 streaming, it works for any audio or video format that can stream over HTTP, for instance AAC and OGG. By using transcoder plug-ins, Subsonic supports on-the-fly conversion and streaming of virtually any audio format, including WMA, FLAC, APE, Musepack, WavPack and Shorten.

If you have constrained bandwidth, you may set an upper limit for the bitrate of the music streams. Subsonic will then automatically resample the music to a suitable bitrate.

In addition to being a streaming media server, Subsonic works very well as a local jukebox. The intuitive web interface, as well as search and index facilities, are optimized for efficient browsing through large media libraries. Subsonic also comes with an integrated Podcast receiver, with many of the same features as you find in iTunes.

Based on Java technology, Subsonic runs on most platforms, including Windows, Mac, Linux and Unix variants.
GPL

Subsonic is open-source software licensed under GPL. 

About
-----

Subsonic is developed by [Sindre Mehus](mailto:sindre@activeobjects.no). He lives in Oslo, Norway and works as a Java software consultant.

This repository is maintained by [K and H Research Company](https://khresear.ch) and provides an unofficial version of Subsonic which does not contain the Licensing code checks present in the official builds. In addition, some minor changes to the repository have been made to assist in the building of a fully-free version for your own use. Any downloads associated with this repo are provided without warranty or guarantee, and your use of such files is at your own risk.

The official homepage of Subsonic can be found [here](http://www.subsonic.org/).

Building
--------

First, make sure you have a relatively recent version of [Maven](http://maven.apache.org/) and a JDK. The 1.6.x series of OpenJDK and the official Oracle JDK(Java 6) have both been tested to work. Ensure that `mvn` can be found in one of the directories listed in your $PATH and that $JAVA_HOME is set to your JDK:

```
$ which mvn
/usr/local/bin/mvn
$ echo $JAVA_HOME
/usr/lib/jvm/java-1.6.0-openjdk.x86_64
$
```

Now you can clone a copy of this repository and switch to the `release` branch if it is not automatically checked out:

```
$ git clone git://github.com/KHresearch/subsonic.git
$ cd subsonic
$ git checkout release
$
```

At this point you are ready to build the basic Subsonic WAR. The maintainer of this repository does not use any of the other build targets (Windows EXE installer, Android app, standalone RPM, etc), and documentation for them is only provided as contributed by others (Pull Requests welcomed).

```
$ mvn package
<lots of buildspam>
[INFO] Building war: /path/to/repo/subsonic/subsonic-main/target/subsonic.war
<more buildspam>
$
```

### Instructions for Tomcat

You can now copy this WAR into your Tomcat server's webapps/ directory and deploy it from the Tomcat Manager. If you are feeling adventurous you can attempt to install the Official Subsonic Windows application and then switch the provided WAR with the one you just built(or grabbed from the [Downloads page](https://github.com/KHresearch/subsonic/downloads)).

```
$ cp subsonic-main/target/subsonic.war /var/lib/tomcat6/webapps/
$
```

### Instruction for building a package for Debian and Ubuntu

The following commands will build and install Subsonic on Debian and Ubuntu. You can probably substitute rpm for debian and the corresponding rpm installing command on rpm-based systems.

```
$ mvn -P full -pl subsonic-booter -am install
$ mvn -P full -pl subsonic-installer-debian/ -am install
$ sudo dpkg -i ./subsonic-installer-debian/target/subsonic-*.deb
```

Good luck!
