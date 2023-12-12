# install Minecraft server

## Requirement
Openjdk

## Cara install Minecraft Server
## 1. membuat direktori 

<code>mkdir Minecrarft</code>

<code>cd mindecraft</code>

## 2. menginstall minecraft server
1. download minecraft server terlebih dalulu disini saya menggunakan nama minecrefft_server.jar sebagai nama server 

<code>wget -o minecreft_server.jar https://piston-data.mojang.com/v1/objects/5b868151bd02b41319f54c8d4061b8cae84e665c/server.jar</code>

![satu](img/Minecraft%20server/1.png)

2. cek ufw firewall jika status inactive maka aktifkan terlebih dahulu

<code>sudo ufw status</code>

3. izinkan firewall untuk ssh dan juga minecraft server

<code>sudo ufw allow OpenSSH</code>
<code>sudo ufw allow 25565</code>

4. aktifkan firewall

<code>sudo ufw enable</code>

lalu ketik y

5. cek kembali firewall dengan command sebelunnya

6. mengizinkan eula

<code>nano eula.txt</code>

7. jalan kan server

<code>java -jar minecreft_server.jar nogui</code>
kita bisa mengatur batas minimu dan maximum ram yang digunakan dengan menam bagkan <code>-Xmx</code> untuk maximu dan <code>-Xms</code> untuk minimu
contoh:

<code>java -Xmx1024M -Xms4G -jar minecreft_server.jar nogui</code>

8. optional
- jika ingin menjalankan di backrond. kita bisa mengunakan mengunakan screen
<code>screen</code>

- jika ingin mengubah settingan server seperti menggubah difficulty level atau semacamnya.
<code>nano server.properties</code>

