# ❌ errores-comunes.md — Problemas típicos y solución

Aquí están los errores más comunes al crear la PC en la nube en Codespaces.

---

## 🛑 Error: `dpkg: error: requested operation requires superuser privilege`

### Causa

Estás intentando instalar un `.deb` sin permisos de administrador.

### Solución

```bash
sudo dpkg -i archivo.deb
sudo apt -f install -y
```

---

## 🛑 Error: El puerto 3000 no abre / no aparece la interfaz

### Causa

El contenedor no está corriendo.

### Solución

Verifica:

```bash
docker ps
```

Si no aparece `pc-nube`, enciéndelo:

```bash
docker start pc-nube
```

Luego revisa la pestaña **Ports**.

---

## 🛑 Error: `port is already allocated`

### Causa

Ya existe un contenedor usando el puerto.

### Solución

```bash
docker rm -f pc-nube
```

Y vuelve a crear la PC con el comando principal.

---

## 🛑 Error: Codespaces se quedó sin espacio

### Causa

Docker guarda mucha caché.

### Solución

```bash
docker system prune -a -f
```

---

## 🛑 Error: Cerré Codespaces y pensé que se borró todo

### Explicación

NO se borra. Solo se apaga.

### Solución

```bash
docker start pc-nube
```

---

## 🛑 Error: `Cannot connect to the Docker daemon`

### Causa

Docker no está iniciado.

### Solución

```bash
sudo service docker start
```

---

## 🛑 Error: Se borró el Codespace

### Explicación

Sí, aquí sí se borra todo.

### Solución

Vuelve a crear el Codespace y ejecuta otra vez el comando de creación.

---

## 🛑 Error: La pantalla va lenta

### Causa

XFCE consume recursos y Codespaces es limitado.

### Solución

Cierra programas dentro del Ubuntu y evita abrir muchas pestañas.
