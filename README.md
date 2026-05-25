# byedpi-throne-linux
Linux'da Discord ve Roblox'u ByeDPI ile açmak için Throne kullanımı.

Açmak için tek komut:

```bash
{ sudo apt install -y unzip libopengl0 || sudo dnf install -y unzip libglvnd-opengl || sudo pacman -S --noconfirm unzip libglvnd || sudo zypper install -y unzip || sudo apk add unzip; } && (wget https://github.com/alimali54/byedpi-throne-linux/releases/download/dosyalar/byedpi_throne_linux.zip || curl -O -L https://github.com/alimali54/byedpi-throne-linux/releases/download/dosyalar/byedpi_throne_linux.zip) && unzip -o byedpi_throne_linux.zip && cd byedpi_throne_linux && chmod +x run.sh run-vf.sh && ./run.sh
```

Vodafone Alternatifi:

```bash
{ sudo apt install -y unzip libopengl0 || sudo dnf install -y unzip libglvnd-opengl || sudo pacman -S --noconfirm unzip libglvnd || sudo zypper install -y unzip || sudo apk add unzip; } && (wget https://github.com/alimali54/byedpi-throne-linux/releases/download/dosyalar/byedpi_throne_linux.zip || curl -O -L https://github.com/alimali54/byedpi-throne-linux/releases/download/dosyalar/byedpi_throne_linux.zip) && unzip -o byedpi_throne_linux.zip && cd byedpi_throne_linux && chmod +x run.sh run-vf.sh && ./run-vf.sh
```
