
sudo -i
wget http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1f-1ubuntu2_amd64.deb
sudo dpkg -i libssl1.1_1.1.1f-1ubuntu2_amd64.deb


sudo -i
root@s:~# apt --fix-broken install

sudo apt-get install build-essential  python3-numpy python3-matplotlib python3-pysam python3-htseq
