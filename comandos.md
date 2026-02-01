# 🧾 comandos.md — Todos los comandos de la PC en la nube

Este archivo es solo para **copiar y pegar** en la terminal de Codespaces.

---

## 🔧 Instalar Docker (solo la primera vez)

```bash
sudo apt update && sudo apt install docker.io -y
```

Verificar que Docker esté instalado:

```bash
docker --version
```

---

## 🖥️ Crear la PC en la nube (Ubuntu XFCE)

Este comando descarga y crea el escritorio Ubuntu completo.

```bash
docker run -d \
  --name pc-nube \
  -p 3000:3000 \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=America/El_Salvador \
  -e SUBFOLDER=/ \
  -e TITLE=PC-Cloud \
  --shm-size="1gb" \
  --restart unless-stopped \
  lscr.io/linuxserver/webtop:ubuntu-xfce
```

---

## 🌐 Abrir la PC

1. Ir a la pestaña **Ports**
2. Abrir el puerto **3000**

---

## ▶️ Encender la PC cuando Codespaces se apaga

```bash
docker start pc-nube
```

---

## ⏹️ Apagar la PC

```bash
docker stop pc-nube
```

---

## 🔄 Reiniciar la PC

```bash
docker restart pc-nube
```

---

## 🗑️ Borrar la PC completamente

```bash
docker rm -f pc-nube
```

Luego puedes volver a crearla con el comando de arriba.

---

## 📦 Instalar archivos .deb (ejemplo TLauncher, Chrome, etc.)

```bash
sudo dpkg -i archivo.deb
sudo apt -f install -y
```

---

## 🧹 Limpiar espacio (muy importante en Codespaces)

Ver cuánto pesa Docker:

```bash
docker system df
```

Limpiar caché y cosas que ya no sirven:

```bash
docker system prune -a -f
```

---

## 📂 Ver contenedores creados

```bash
docker ps -a
```

---

## 🧠 Ver si la PC está corriendo

```bash
docker ps
```

Si aparece `pc-nube`, está encendida.
