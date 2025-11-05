# Menjalankan aplikasi

## Install pm2
```sh
npm install pm2 -g
```

## File ecosystem.config.js
pastikan di tiap direktori terdapat file ecosystem.config.js.

biasanya source code melampirkan ecosystem.config.js.example sebagai contoh

salin file ecosystem.config.js.example ke ecosystem.config.js
```bash
cp ecosystem.config.js.example ecosystem.config.js
```
isi nilai sesuai dengan konfigurasi aplikasi

## Menjalankan pm2
```sh
pm2 start ecosystem.config.js
```
jalankan perintah ini di tiap direktori aplikasi

dokumentasi lengkap pm2: https://pm2.keymetrics.io/docs/usage/quick-start/
