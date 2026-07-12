# byedpi-throne-linux
Linux'da Discord ve Roblox'u ByeDPI ile açmak için Throne kullanımı.

ByeDPI'ın sistem açılışında otomatik açılmasını kod içine yerleştirdim. Throne'u ise kendiniz menüsünden otomatik başlayacak şekilde ayarlayabilirsiniz.
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
