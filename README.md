# José Muñoz's Personal Ubuntu Repository

<br />

## How to use this repository

```
curl -s --compressed "https://jdmg94.github.io/ppa/ubuntu/KEY.gpg" | sudo apt-key add -
sudo curl -s --compressed -o /etc/apt/sources.list.d/josemunozdev.list "https://jdmg94.github.io/ppa/ubuntu/josemunozdev.list"
```

## How to refresh packages

```
dpkg-scanpackages --multiversion . > Packages
gzip -k -f Packages
apt-ftparchive release . > Release
gpg --default-key "${EMAIL}" -abs -o - Release > Release.gpg
gpg --default-key "${EMAIL}" --clearsign -o - Release > InRelease
```
