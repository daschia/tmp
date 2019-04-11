<iframe scrolling="no" id="hearthis_at_track_1431588" width="90%" height="130" src="https://hearthis.at/embed/1431588/transparent/?hcolor=&color=&style=2&block_size=2&block_space=1&background=0&waveform=0&cover=0&autoplay=0&css=" frameborder="0" allowtransparency allow="autoplay"><p>Listen to <a href="https://hearthis.at/bdrcmpwp/the-brotherhood-of-house-109-ft-reece-johnson-mr-shadow/">The Brotherhood Of House 109 ft Reece Johnson &amp; Mr Shadow</a><span>by</span><a href="https://hearthis.at/bdrcmpwp/">THE BROTHERHOOD OF HOUSE</a> <span>on</span> <a href="https://hearthis.at/">hearthis.at</a></p></iframe>

## Web : Server : Access server w/ reverse proxy and Let's Encrypt

[Franz Geffke](https://f-a.nz/about/) shows code lines at [Gitea behind NGINX](https://f-a.nz/dev/install-gitea-behind-nginx-on-debian/)
and [Syncthing with NGINX reverse proxy](https://f-a.nz/dev/setup-syncthing-on-debian-server-with-nginx-reverse-proxy/) 
which might help us reaching docker containers w/ installed SSL certs.

Tags:  certbot, LE, Let's Encrypt, nginx, SSL, 

.


## Surf : Secure : via Proxy : Zend2.com

<form action="http://zend2.com/includes/process.php?action=update1" method="post" id="frm">
 <input type="text"     name="u" value=""   id="id_url"                        />
 <input type="checkbox" name="encodeURL"    id="encodeURL"    checked="checked"/>
 <input type="checkbox" name="encodePage"   id="encodePage"                    />
 <input type="checkbox" name="allowCookies" id="allowCookies" checked="checked"/>
 <input type="checkbox" name="stripJS"      id="stripJS"      checked="checked"/>
 <input type="checkbox" name="stripObjects" id="stripObjects" checked="checked"/>
</form>

https://jolygram.com/profile/ladydabbs710/285903122  
https://de..com/view_video.php?viewkey=ph5b3a0cf4c6f4e  
https://syndication.exoclick.com/splash.php?idzone=1775026&type=8&cb=1055  

.


## Web : Tool : Static : Convert : Staticman
![Logo of Staticman](https://www.google.com/s2/favicons?domain=staticman.net) [Staticman](https://staticman.net) <!-- https://staticman.net/assets/images/icons/favicon-16x16.png --> transforms user-generated content into Github. Keep your data - no third-party platforms.

.

## Web : Tool : E-Commerce : Shop : SnipCart.com
![Logo of SnipCart](https://www.google.com/s2/favicons?domain=snipcart.com) [Snipcart](https://snipcart.com) <!-- https://snipcart.com/images/favicons/favicon-16x16.png --> adds a cart platform to your blog, CMS, framework, ... .

.

## Web : Script : Popup-watch in nice words via browser and cron

The website https://7070.org says s.th. like: "Es ist fünf vor zwölf - every 300 sec.
What if it pops up and fills the screen regularly to show you that knocking-off time is comin soon?
Executable line instead of interactive _crontab -e_:
```
(crontab -l 2>/dev/null ; echo "*/2 * * * * pidof firefox && DISPLAY=:0 firefox --new-tab 7070.org") | crontab
```
WTF:  
**2>/dev/null**: Prevents this possible stdout: "no crontab for user". (https://stackoverflow.com/a/878647)  
**pidof**: To prevent FF from hosing all your 1000 open tabs use a running instance.  
**DISPLAY=:0** doesn't work? Check display number with /usr/bin/w.

.

## Cloud : Hosting : diverse

instantview, up download
- ![Logo of userscloud.com](https://www.google.com/s2/favicons?domain=https://userscloud.com) [UsersCloud.com](https://userscloud.com) <!-- https://userscloud.com/avatar/logo_s.jpg -->
- ![Logo of sendit.cloud](https://www.google.com/s2/favicons?domain=https://sendit.cloud/) [SendIt.cloud](https://sendit.cloud) <!-- https://sendit.cloud/favicon.ico -->

stream, instantview, up download
- ![Logo of openload.co](https://www.google.com/s2/favicons?domain=https://openload.co) [OpenLoad.co](https://openload.co) <!-- https://openload.co/favicon.ico -->

.

## Backup : cloud &amp; on premise (via CLI) : encrypted : Duplicacy

![Logo of Duplicacy](https://www.google.com/s2/favicons?domain=duplicacy.com) <!-- https://duplicacy.com/img/duplicacy.png -->
[Duplicacy.com](https://duplicacy.com)

- deduplication
- incremental
- encryption
- migration

.

## GNU/Linux : CMD : 'free' in %
```
free -ht | grep Mem | awk '{print $7/$2 * 100.0}'
55.45

free -ht | grep Mem | awk '{print $4/$2 * 100.0}'
26.3158

echo Free memory: $(free | grep Mem -h | awk '{print $3/$2 * 100}' | cut -d. -f1)%
Free memory: 4%
```

https://stackoverflow.com/questions/10585978/

.

## GNU/Linux : Maintain : Root dir '/'  is full

Only greenhorns have /var residing in /  
If elsewhere is plenty of space - then move 'n' bind.

#### Why 'mount --bind' instead of symlinks? 

|        | mount --bind | symlinks |
|--------|:------------:|:--------:|
| chroot |       1      |     0    |
| webdav |       1      |     0    | <!-- https://www.tablesgenerator.com/markdown_tables -->

https://askubuntu.com/questions/205841/

#### Example: Docker didn't accept new images cause:
```
$ df -hT	
Filesystem   Type      Size  Used Avail Use% on
-------------------------------------------------------
/dev/sda2    ext4      1.9G  1.4G  408M  78% /
```

```
$ systemctl cat docker
$ docker ps -a
$ sudo systemctl stop   docker
$      systemctl status docker
$ sudo du -h /var/lib/docker
$ sudo du -h /var/lib/docker | less
$ sudo du -h /var/lib/docker | grep 'M'
$ sudo mkdir                   /lvbtr/+var+lib+docker
$ sudo mv -v /var/lib/docker/* /lvbtr/+var+lib+docker
$ sudo mount --bind            /lvbtr/+var+lib+docker /var/lib/docker
$ echo                        '/lvbtr/+var+lib+docker /var/lib/docker none bind' | sudo tee -a /etc/fstab
$ sudo systemctl start docker
```
.

## Program : Server : Webserver : Netcat
```
while true; do sudo echo -e "HTTP/1.1 200 OK\r\n\r\n<h1>$(hostname) is live>/h1<$(date +%F)" | sudo nc -vl -p 80 ; done &
```
.

## Program : Media : Player : CLI : Music

*5 CLI music player*  
https://www.bettertechtips.com/linux/cli-music-player/

*Command*
```
play(){ gnome-mpv $(wget -O- -U'Mozilla/4.0' $1 | grep 'streamUrl' | grep -m1 -Eo 'http://[^"]*'); }; play https://www.radio.net/s/relaxingjazz
```
- korea        https://www.radio.net/s/freenorthkorea http://media.fnkradio.com/radio/bc_00/1002satFNKR1300.mp3
- chicago      https://www.radio.net/s/chfmhouse      http://38.107.243.218:8218/stream
- relaxingjazz https://www.radio.net/s/relaxingjazz

*Mplayer low on cache?*
```
mplayer -cache 8192 -cache-min 80 $URL   # https://askubuntu.com/questions/189440/
```
*Radio: mplayer + python = *  
http://www.coderholic.com/pyradio/

*Recorder / player for ALSA: avconv + arecord*
https://askubuntu.com/questions/291910

*URL / IP search*  
- https://www.radio.net/genre
- https://www.xatworld.com/radio-search

.

## NET : Portscan : Test Online

![Logo of My-Addr.com](https://www.google.com/s2/favicons?domain=ports.my-addr.com) [Ports.My-Addr.com](http://ports.my-addr.com/check-all-open-ports-online.php)  
![Logo of IPFingerPrints](https://www.google.com/s2/favicons?domain=www.ipfingerprints.com) [IPFingerPrints.com](http://www.ipfingerprints.com/portscan.php)

Tags: IP, net, network, online, port, scan, security

.

## Program : Media : Media Server
https://alternativeto.net/software/xbmc-media-center/

#### Ampache
https://alternativeto.net/software/ampache/

#### AirSonic or LibreSonic Docker
https://airsonic.github.io/docs/install/docker/  
https://hub.docker.com/r/airsonic/airsonic/  
https://forums.unraid.net/topic/52140-support-linuxserverio-libresonic/  
https://github.com/tonipes/libresonic-docker  

#### Test-Media
```
while read line , do wget -U 'Mozilla/4.0' $line ; done <<'EOF'
 https://images.pexels.com/photos/1295138/pexels-photo-1295138.jpeg
 https://images.pexels.com/photos/443391/pexels-photo-443391.jpeg
EOF
```
<!--
http://www.swiatobrazu.pl/zdjecie/artykuly/350404/waclaw-wantuch-1-akt-w-polskiej-fotografii-.jpg
http://view.stern.de/de/picture/nsfw/3549778/akt-model-woman-art-female-black-and-620.jpg
http://view.stern.de/de/picture/2919441/akt-art-highkey-black-white-sculpture-grey-940.jpg
http://www.lowbird.com/data/images/2011/01/0065.jpg
http://www.swiatobrazu.pl/zdjecie/artykuly/116294/akt-w-suwalkach.jpg
https://heikole-art.net/wp-content/uploads/photo-gallery/IMG_6401.jpg
https://iso.500px.com/wp-content/uploads/2015/06/dancer_cover-1500x1000.jpeg
http://1.bp.blogspot.com/-rd0UFCCRSNs/TtpmDAE8XYI/AAAAAAAAHJ4/fs2NzAr-b_g/s1600/120508.jpg
http://1.bp.blogspot.com/-kE7HnbtZIA4/VqZV1IImBNI/AAAAAAAD-x8/A1DXGEKD4Xg/s1600/espalda-modelo-desnuda-waclaw-wantuch.JPG
http://thefappeningblog.com/wp-content/uploads/2017/11/Hunter-McGrady-Nude-5-thefappeningblog.com_.jpg
http://s2.glbimg.com/7qyaG8qVlo3FYR2hn1yaFzfC_es=/smart/e.glbimg.com/og/ed/f/original/2015/03/23/goddess2-1247x1247.jpg
https://get.pxhere.com/photo/black-and-white-girl-woman-model-darkness-monochrome-grace-hands-beauty-sexy-nude-body-posture-photoshoot-elegance-breast-nipple-erotica-beautiful-girl-naked-girl-without-clothes-sense-monochrome-photography-art-model-1191518.jpg
-->

#### Container: "AirSonic"
```
docker create --name=air -ePUID=1000 -eGUID=1000 -p4040:4040 \
 --restart unless-stopped -v/root/5:/media linuxserver/airsonic

curl ifconfig.io
40.117.119.219:4040

docker volume inspect data
```
.

## Web : Html : Markdown : Convert : "Pandoc"
![Logo of Pandoc.org](https://www.google.com/s2/favicons?domain=Pandoc.org) [Pandoc.org](http://pandoc.org/)  
Further links at ![Logo of c't](https://www.google.com/s2/favicons?domain=ct.de) [ct.de/y1nh](http://ct.de/y1nh)

```
apt install
echo "--\ntitle: MY_TITLE\nauthor:\n - author 1\n - author 2\ncopy: Kein Copyright" >> test.md
pandoc \
 -o [https://]test.html \
 [-s]                   \
 [--template=tmpl.html] \
 [--toc [--toc-depth=XXX]]                \
 test.md[doc|...]          # /s = standalone: inkl. skeleton
echo "<title>$title$</title></head><body><header>$if (toc)$\n$toc$\n$endif$</header>$body$<footer>$copy$</footer>" >> tmpl.html
```

Tags: app, CLI, convert, html, markdown, tool

.

## Media : Photos & Videos: Free : "Pexels"

The best stock photos & videos shared by talented creators at ![Logo of Pexels.com](https://www.google.com/s2/favicons?domain=pexels.com) [Pexels](https://www.pexels.com/): All free for commercial use too.

Tags: designer, free, photograph, pictures

.

## GFX : Photos : HQ : "Vast Photos"

![Logo of VastPhotos.com](https://www.google.com/s2/favicons?domain=vastphotos.com) <!-- https://vastphotos.com/files/uploads/favicon.png --> 
[VastPhotos](https://vastphotos.com) 

Tags: black & white, colorful, incredible, light, photos, photograph, pictures

.

## Program : Sync : Cloud : Odrive : control via bash
https://forum.odrive.com/t/bash-script-snippet-to-display-updating-sync-state-with-pause-and-quit/1588

Tags: app, backup, borg deduplicating archiver, monitor, tool, 

.

## Program : Backup : Deduplicated : "Borg Deduplicating Archiver"
![Logo of BorgBackup.org](https://www.google.com/s2/favicons?domain=www.borgbackup.org) [BorgBackup](https://www.borgbackup.org/)

Tags: app,  archiver, backup, compression, deduplicating, encryption, fuse,

.

## Net : Scy : VPN : HowTo
https://www.cyberciti.biz/faq/howto-setup-openvpn-server-on-ubuntu-linux-14-04-or-16-04-lts/

.

## Data : Convert : Online : "Online-Convert.com"

1001 possibilities at [Online-Convert](https://online-convert.com)

.

## Web : File Transfer : User 2 User : "Take A File"

Transfer files w/o intermediate cloud only via browser at [Take A File](https://takeafile.com). Any size, confidential, w/o registration, funded by EU.

.

## Program : Remote Filesystem : Google Drive : GUI : "ODrive"

ODrive = OpenDrive AppImage [Explanation on 2DayGeek](https://www.2daygeek.com/odrive-open-drive-google-drive-gui-client-for-linux/)

.

## Program : App : Web App : Link Collection : "App Scope"
![Logo of ](https://www.google.com/s2/favicons?domain=https://appsco.pe/) [App Scope](https://appsco.pe/) 

Tags: browser based, home screen, no download, progressive web app

.

## Web : Html : Badges : Shield.io
![Logo of Shield.io](https://www.google.com/s2/favicons?domain=shields.io) [Shield.io](https://shields.io)

Tags: button, dynamic, embedd, make, meta data, query string parameter, svg, tool, URL dependent

.

## Web : UIX : Link collection : Sans Francisco
![Logo of Sans Francisco](https://www.google.com/s2/favicons?domain=https://sansfrancis.co) [Sans Francisco](https://sansfrancis.co)

Tags: app, collaboration, color, design, foto, icon, inspire, layout, presentation, tool, typo, 

.

## Program : MultiMedia : Player : cmus
[C* cmus](https://cmus.github.io/)

Tags: AAC, bash script, CLI, fast, filter, FLAC, mp3, themes, WAV, vi-like

.

## Security : Credentials : Identity Leak Checker

- ![Logo of Have I Been Pwned (HIBP)](https://www.google.com/s2/favicons?domain=haveibeenpwned.com) [Have I Been Pwned (HIBP)](https://haveibeenpwned.com/) <!-- https://haveibeenpwned.com/favicon.ico -->   
- ![Logo of Hasso Plattner Institute](https://www.google.com/s2/favicons?domain=sec.hpi.uni-potsdam.de) [HPI Identity Leak Checker](https://sec.hpi.uni-potsdam.de/ilc/) <!-- https://sec.hpi.uni-potsdam.de/ilc/ico/favicon.ico --> 

Tags: credential-stuffing-list, hacked, Hasso-Plattner-Institut, Troy Hunt,

.

## Program : Web : Server : Cert : ACMA : "CertBot"
![Logo of CertBot](https://www.google.com/s2/favicons?domain=certbot.eff.org) [CertBot](https://certbot.eff.org/docs/using.html) EFF's tool to obtain certs from Let's Encrypt and auto-enable HTTPS on the server. Is too a client for any other ACME-CA.

```
cat <<'EOF' > /etc/apt/sources.list
 #   bwn for eff.org's certbot                                                                    
 # https://backports.debian.org/Instructions/                                                      
 deb http://deb.debian.org/debian stretch-backports main                                           
EOF
apt-get update                                                                                    
apt-get -t stretch-backports install certbot
```

Tags: ACME, Automatic Certificate Management Environment, CA, eff.org, Electronic Frontier Foundation, LE, Let's Encrypt, 

.

## Program : Backup : Snapshots : "Cya"
linux magazin 03/19 "Snapsch&uuml;sse"

- ![Logo of Qt-FSArchiver](https://www.google.com/s2/favicons?domain=sourceforge.net) [Qt-FSArchiver](https://sourceforge.net/projects/qt-fsarchiver/)
- ![Logo of CyberWS.com](https://www.google.com/s2/favicons?domain=CyberWS.com) [Cya](https://CyberWS.com/bash/cya)
- ![Logo of GitHub](https://www.google.com/s2/favicons?domain=gitub.com) [Cya on GitHub](https://gitub.com/cleverwise/cya)

.

## Program : Web : Webserver : static : "WebOrf"
https://ltworf.github.io/weborf
```
weborf --basedir MY_WWW [-i INTERFACE               \   # default: all interfaces
       --index   LIST_OF_FILES_INTERPRETED_AS_INDEX \   # default: directory indexing; index.htm ignored
        -p       PORT                               \   # default: 8080
        -V       VIRT_HOSTS]                            # for multiple dirs
```
Tags: apt, CLI, local, static, virt. hosts, webdav

.

## Program : Web : Webserver : static : "Boa"
http://www.boa.org/documentation/
http://www.boa.org/documentation/boa-2.html

Tags: chroot no, CLI, compile, static

.

## Program : Web : Webserver : static : "DarkHTTP"
https://unix4lyfe.org/darkhttpd/

no .deb etc

Tags: chroot, CLI, compile, resuming, static, streaming, 

.

## WEB : html : fonts
## Program : Filesystem : Remote : Google Drive : Fuse : "Ocamlfuse"

Google Drive Ocamlfuse [Explanation on 2DayGeek](https://www.2daygeek.com/mount-access-google-drive-on-linux-with-google-drive-ocamlfuse-client/)

.

## Machine : Config : Time : NetworkTimeProtocol
```
   # control
$ timedatectl   # or
$ systemctl status systemd-timesyncd

   # Find timeserver: [NtpPool.org](https://NtpPool.org/zone)
$ MY_TIMESERVER=europe.pool.ntp.org

   # delete, dry-run and then execute (with '-i')
$ sed -e "/^[#]NTP=/d" -e "s/Time]/Time]\nNTP=${MY_TIMESERVER}/" /etc/systemd/timesyncd.conf

   # restart
$ systemctl restart systemd-timesyncd
```

.

## Machine : Maintain : Container : Docker : Remotely : "ssh-docker"

![Logo of PyPi.org](https://www.google.com/s2/favicons?domain=pypi.org) <!-- https://pypi.org/static/images/logo-small.6eef541e.svg --> from [PyPi.org](https://pypi.org/project/ssh-docker/)

.

## Machine : Config : ScreenRC : 1001 Tips

ServerFault users [https://serverfault.com/questions/3740/](screenrc)

.

## Program : Office : Mail : CLI : diverse

Via ![Logo of Tecmint.com](https://www.tecmint.com/wp-content/themes/tecmint/images/favicon.ico) [TecMint](https://www.tecmint.com/best-commandline-email-clients-for-linux/)

.

## Program : Android : Apps : Building : "App Inventor"

[Tutorial](http://appinventor.mit.edu/explore/tutorials.html) for the MIT [App Inventor](http://appinventor.mit.edu/appinventor-sources/) 


<!-- 
## WEB.VRW..video+mobile+etc  https://bespohk.com/
<video class="masthead__video" id="feature" loop autoplay preload="auto" poster="/img/headers/video-cover.jpg">
 <source src="//static.bespohk.com/video/home.mp4" type="video/mp4">
</video>
--> 

.

## Web : Hosting : Temporary : For Backup, sharing, webpublishing, etc up to 10 GB

Upload via SHell-Yeah for 14 days to [Transfer.sh](https://www.transfer.sh/). Markdown appears beautily formatted.


###################################################################################
## TMP


```
alias screenhelp='echo "Rename session: C-a :sessionname NEWNAME \n Show, create, rename, next window-title: C-a \", c, A, n \n 

https://unix.stackexchange.com/questions/20989/

(`echo ${STY} | sed -e 's/[0-9]*\.//g'`:${WINDOW}:`screen -Q title`)   # compiled w/ 'query'


(${STY}:${WINDOW})

PS1='@\h::${STY#[0-9]*.}:${WINDOW} '

removes the process number from ${STY}
includes the window number (as mentioned "at creation time")
includes the window title (as returned from screen -Q title)

```
