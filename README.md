# byedpi-throne-linux
Linux'da Discord ve Roblox'u ByeDPI ile açmak için Throne kullanımı.

Video anlatımı izlemeniz faydalı olur. 
https://youtu.be/8VA1ahFQrys

Videoda Throne açılışa ekleniyor ama ByeDPI'ın açılışa eklenmesini kendiniz halletmelisiniz demiştim, o konuda güncelleme yaptım ve sistem açılışında otomatik açılmasını kod içine yerleştirdim. Artık ByeDPI otomatik başlayacak ve Throne'u ise kendiniz menüsünden otomatik başlayacak şekilde ayarlayabilirsiniz.

ByeDPI'ın otomatik başlatılma ayarını kaldırmak için rm -f ~/.config/autostart/ciadpi.desktop komutunu kullanabilirsiniz.


Açmak için tek komut:

```bash
{ sudo apt install -y unzip libopengl0 || sudo dnf install -y unzip libglvnd-opengl || sudo pacman -S --noconfirm unzip libglvnd || sudo zypper install -y unzip || sudo apk add unzip; } && (wget https://github.com/alimali54/byedpi-throne-linux/releases/download/dosyalar/byedpi_throne_linux.zip || curl -O -L https://github.com/alimali54/byedpi-throne-linux/releases/download/dosyalar/byedpi_throne_linux.zip) && unzip -o byedpi_throne_linux.zip && cd byedpi_throne_linux && chmod +x run.sh run-vf.sh && mkdir -p ~/.config/autostart && (cat << 'EOF' > ~/.config/autostart/ciadpi.desktop
[Desktop Entry]
Exec=DIR/ciadpi -r 1+s
Icon=
Name=ciadpi
Path=DIR
Terminal=false
Type=Application
EOF
  ) && sed -i "s|DIR|$(pwd)|g" ~/.config/autostart/ciadpi.desktop && chmod +x ~/.config/autostart/ciadpi.desktop && ./run.sh
```

Vodafone Alternatifi:

```bash
{ sudo apt install -y unzip libopengl0 || sudo dnf install -y unzip libglvnd-opengl || sudo pacman -S --noconfirm unzip libglvnd || sudo zypper install -y unzip || sudo apk add unzip; } && (wget https://github.com/alimali54/byedpi-throne-linux/releases/download/dosyalar/byedpi_throne_linux.zip || curl -O -L https://github.com/alimali54/byedpi-throne-linux/releases/download/dosyalar/byedpi_throne_linux.zip) && unzip -o byedpi_throne_linux.zip && cd byedpi_throne_linux && chmod +x run.sh run-vf.sh && mkdir -p ~/.config/autostart && (cat << 'EOF' > ~/.config/autostart/ciadpi.desktop
[Desktop Entry]
Exec=DIR/ciadpi -s1 -At -d2 -f-1 -r1+s -An
Icon=
Name=ciadpi
Path=DIR
Terminal=false
Type=Application
EOF
  ) && sed -i "s|DIR|$(pwd)|g" ~/.config/autostart/ciadpi.desktop && chmod +x ~/.config/autostart/ciadpi.desktop && ./run-vf.sh
```

## Terminalden throne komutu ile çalıştırma
Kullandığınız shellin konfigürasyon dosyasına aşağıdaki komutu ekleyeceğiz. Genellikle bash kullanılır.
Hangi shelli kullandığınız bilmiyorsanız terminale ```echo $0``` komutunu yazıp çıkan shellin konfigürasyon dosyasını internetten arayabilirsiniz.
vodafone dışındaki ISS'ler için
```bash
alias throne='{ sudo apt install -y unzip libopengl0 || sudo dnf install -y unzip libglvnd-opengl || sudo pacman -S --noconfirm unzip libglvnd || sudo zypper install -y unzip || sudo apk add unzip; } && (wget https://github.com/alimali54/byedpi-throne-linux/releases/download/dosyalar/byedpi_throne_linux.zip || curl -O -L https://github.com/alimali54/byedpi-throne-linux/releases/download/dosyalar/byedpi_throne_linux.zip) && unzip -o byedpi_throne_linux.zip && cd byedpi_throne_linux && chmod +x run.sh run-vf.sh && mkdir -p ~/.config/autostart && (cat << 'EOF' > ~/.config/autostart/ciadpi.desktop
[Desktop Entry]
Exec=DIR/ciadpi -r 1+s
Icon=
Name=ciadpi
Path=DIR
Terminal=false
Type=Application
EOF
  ) && sed -i "s|DIR|$(pwd)|g" ~/.config/autostart/ciadpi.desktop && chmod +x ~/.config/autostart/ciadpi.desktop && ./run.sh'
```

vodafone için
```bash
alias throne='{ sudo apt install -y unzip libopengl0 || sudo dnf install -y unzip libglvnd-opengl || sudo pacman -S --noconfirm unzip libglvnd || sudo zypper install -y unzip || sudo apk add unzip; } && (wget https://github.com/alimali54/byedpi-throne-linux/releases/download/dosyalar/byedpi_throne_linux.zip || curl -O -L https://github.com/alimali54/byedpi-throne-linux/releases/download/dosyalar/byedpi_throne_linux.zip) && unzip -o byedpi_throne_linux.zip && cd byedpi_throne_linux && chmod +x run.sh run-vf.sh && mkdir -p ~/.config/autostart && (cat << 'EOF' > ~/.config/autostart/ciadpi.desktop
[Desktop Entry]
Exec=DIR/ciadpi -s1 -At -d2 -f-1 -r1+s -An
Icon=
Name=ciadpi
Path=DIR
Terminal=false
Type=Application
EOF
  ) && sed -i "s|DIR|$(pwd)|g" ~/.config/autostart/ciadpi.desktop && chmod +x ~/.config/autostart/ciadpi.desktop && ./run-vf.sh'
```

kaydettikten sonra terminali kapatıp tekrar açmanın ardından ```throne``` yazarak test edebilirsiniz.
