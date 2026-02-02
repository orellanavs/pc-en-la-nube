# 💻 PC EN LA NUBE GRATIS con GitHub Codespaces + Ubuntu

> Sí. GitHub te presta una máquina virtual real en la nube.
> Con escritorio Ubuntu completo.
> Sin VirtualBox. Sin instalar nada en tu PC.

---

## 🎥 Video tutorial (TikTok)

👉 Mira el video paso a paso aquí:
**[https://vt.tiktok.com/ZSaboUWUC/]**

---

## 👤 Mis redes

* TikTok: **@j_eliseoo_v**
* Discord: **eliseo_2026**

---

## 🧠 ¿Qué es esto?

Este repositorio es una guía para crear tu propia **PC en la nube** usando:

* GitHub Codespaces
* Docker
* linuxserver/webtop (Ubuntu con escritorio XFCE)

Vas a poder:

✅ Usar Ubuntu desde el navegador
✅ Instalar programas (.deb, navegadores, etc.)
✅ Guardar tus cosas
✅ Apagarla y volverla a encender con un comando

---

## 🚀 PASO 1 — Crear Codespace

1. Entra a este repositorio
2. Clic en el botón verde **Code**
3. Clic en **Create Codespace**

Espera a que cargue la terminal.

---

## ⚙️ PASO 2 — Instalar Docker

Pega esto en la terminal:

```bash
sudo apt update && sudo apt install docker.io -y
```

---

## 🖥️ PASO 3 — Descargar Ubuntu con escritorio

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

## 🌐 PASO 4 — Abrir tu PC en el navegador

Cuando el contenedor esté corriendo:

1. Ve a la pestaña **Ports**
2. Abre el puerto **3000**
3. ¡Listo! Ya tienes Ubuntu con escritorio.

---

## 🔁 Encender y apagar tu PC

Cuando Codespaces se apague, NO se borra.

Solo usa:

### Encender

```bash
docker start pc-nube
```

### Apagar

```bash
docker stop pc-nube
```

---

## 🧹 Borrar todo y empezar de nuevo

```bash
docker rm -f pc-nube
```

Luego vuelves a ejecutar el comando del PASO 3.

---

## ❓ Preguntas frecuentes

### ¿Es gratis?

Sí, usando el plan gratuito de GitHub.

### ¿Se borra cuando cierro?

No. Solo se apaga.

### ¿Puedo instalar programas?

Sí. Es un Ubuntu real.

### ¿Funciona desde celular?

Sí, desde cualquier navegador.

### ¿Necesito saber Linux?

No. Solo copiar y pegar.

---

## 🧠 Errores comunes

### `dpkg: error: requested operation requires superuser privilege`

Solución:

```bash
sudo dpkg -i archivo.deb
```

---

## ⭐ Guarda este repo

Si el video te ayudó, guarda este repositorio.
Aquí tienes todos los comandos siempre.

---

Hecho para la comunidad 🧠💻
