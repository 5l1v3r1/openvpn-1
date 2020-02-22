# openvpn
openvpn

VPN Sunucusu Oluşturma Ubuntu / Root Yetkisi Verme Ayarları .

usermod -aG sudo nomekboys
sudo passwd root
sudo nano /etc/ssh/sshd_config   // Dosyanın içindeki PermitRootLogin without-password satırını PermitRootLogin yes ile değiştirin.
service ssh restart
ve sonrasında çıkıp giriyoruz oluyor root.

Dosyayı Linux'a indirme
scp root@231231231:/root/nomekboys.ovpn /root
çalıştırma :
openvpn --config nomekboys.ovpn

-- Tshark ile Paketleri Yakala
-tshark -i wlan0 -w capture-output.pcap


güvenlik duvarı komutları:
sudo ufw status
sudo ufw enable

Belirli bir ip adresini engellemek için :

sudo ufw deny IP_no

azure ....
https://github.com/Nyr/openvpn-install  // ilk burdaki installation'u kuracagım ubuntu sunucuma
wget https://git.io/vpn -O openvpn-install.sh && bash openvpn-install.sh
https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-16-04
https://www.digitalocean.com/community/tutorials/how-to-set-up-an-openvpn-server-on-ubuntu-16-04
