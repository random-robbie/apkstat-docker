# apkstat-docker
APKStat in docker...

This docker container has a slight change to it.

You can download the APK direct and extract the details using apk stat

Example
---
```
docker run -it txt3rob/apkstat-docker
apkstat apkstat com.facebook.katana
```

[![Capture.png](https://s1.postimg.org/19eou117cv/Capture.png)](https://postimg.org/image/91fttnu5x7/)



It uses https://github.com/matlink/gplaycli to download the APK.

You can search for an apk inside the docker by issues the command

```
gplaycli -s "name of app"
```

get the appId and then type

```
apkstat com.whatever.com
``

and apkstat will get to work!



FROM https://github.com/hexabin/APKStat
-------

# APKStat
Save time during your initial analysis of an Android APK file. APK Stat will grab most of the information you need in your initial assessment right away and output the information in an easy to read set of text files.

<h2><strong>APK Stat - Automated Information Retrieval From APKs For Initial Analysis</strong></h2>

APK Stat will use APK Tool to decompress and decode your APK file. APK Stat Will:
<ul>
<li> Breaks Permissions, Activities, Activity Aliases, Services, Providers and Receivers Into Easily Readable Groups</li>
<li> Scours All Files After Decoding For Hardcoded IP Addresses and Domain Names</li>
<li> Single Out The Launcher Activity </li>
<li> Automatically Creates a Strings.txt file</li>
</ul>

<h4><strong>Download Instructions:</strong></h4>
<i>Linux:</i> 

```
git clone https://github.com/hexabin/APKStat.git
cd APKStat
wget "https://raw.githubusercontent.com/iBotPeaches/Apktool/master/scripts/linux/apktool" -O /usr/local/bin/apktool
wget "https://bitbucket.org/iBotPeaches/apktool/downloads/apktool_2.2.4.jar" -O /usr/local/bin/apktool.jar
chmod 777 /usr/local/bin/apktool
```

Place your Analysis APK file in the APKStat directory before running

<strong>USAGE</strong>: python apkstat.py yourapkfile.apk

<strong><i>Dependancy:</i></strong> APKTool - <a href="https://ibotpeaches.github.io/Apktool">https://ibotpeaches.github.io/Apktool/</a>
