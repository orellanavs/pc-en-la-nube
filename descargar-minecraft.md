🎮 Instalar TLauncher (Minecraft) en tu Linux VM
📂 PASO 1 — Ir a Descargas
bashcd ~/Downloads
📦 PASO 2 — Instalar el .deb de TLauncher
bashsudo dpkg -i tlauncher-linux-installer.deb
🧩 PASO 3 — Corregir dependencias
bashsudo apt-get -f install -y
✅ PASO 4 — Verificar que quedó instalado
bashwhich tlauncher
