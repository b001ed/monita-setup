# INSTALASI
***pastikan curl sudah terinstall***

## download source code
- [sockelat](https://github.com/dbemonita/sockelat-main/releases)
- [loket](https://github.com/dbemonita/loket-main/releases)
---

## install nvm
```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
```
copy ke ~/.bashrc
```sh
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```
jalankan perintah untuk meload environment variable
```sh
source ~/.bashrc
```
[doc resmi nvm](https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating)

---

## install nodejs
```sh
nvm install 16 #versi untuk vismon
```
```sh
nvm install 18 #versi untuk loket
```
```sh
nvm install 20 #versi untuk sockelat
```

## install loket
```bash
curl -L -o "loket-main-latest.tar.gz" "https://api.github.com/repos/dbemonita/loket-main/tarball/HEAD"
```
```bash
tar -xvzf loket-main-latest.tar.gz --xform='s|dbemonita-loket-main-[^/]*|loket|'
```
gunakan node versi 18
```sh
cd loket
nvm use 18
rm package-lock.json
npm install
```
copy .env.example ke .env
sesuaikan nilai
```bash
mv .env.example .env
```


## install sockelat
```bash
curl -L -o "sockelat-main-latest.tar.gz" "https://api.github.com/repos/dbemonita/sockelat-main/tarball/HEAD"
```
```bash
tar -xvzf sockelat-main-latest.tar.gz --xform='s|dbemonita-sockelat-main-[^/]*|sockelat|'
```
gunakan node versi 18
```sh
cd sockelat
nvm use 20
rm package-lock.json
npm install
```
copy .env.example ke .env
sesuaikan nilai
```bash
mv .env.example .env
```

## install vismon
salin source code vismon-build (https://github.com/dbemonita/vismon5-release/releases), misal: vismon-build.gz
```bash
tar -xvzf vismon-build.tar.gz
mv build vismon
cd vismon
mv config.js.example config.js
```
