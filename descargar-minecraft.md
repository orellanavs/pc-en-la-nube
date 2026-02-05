# 🎮 Instalar TLauncher (Minecraft) en tu Linux VM

## 📂 PASO 1 — Ir a Descargas
```bash
cd ~/Downloads
```

## 📦 PASO 2 — Instalar el .deb de TLauncher
```bash
sudo dpkg -i tlauncher-linux-installer.deb
```

## 🧩 PASO 3 — Corregir dependencias
```bash
sudo apt-get -f install -y
```

## ✅ PASO 4 — Verificar que quedó instalado
```bash
which tlauncher
```
