Descargar e instalar TLauncher en Linux (VM)

Estos son los únicos comandos necesarios para instalar TLauncher desde un archivo .deb y verificar que quedó instalado correctamente.

1) Ir a la carpeta de descargas
cd ~/Downloads


Este comando te mueve a la carpeta donde normalmente se descargan los archivos.

2) Instalar el archivo .deb de TLauncher
sudo dpkg -i tlauncher-linux-installer.deb


Instala el programa directamente desde el archivo descargado.

3) Corregir dependencias automáticamente
sudo apt-get -f install -y


Si faltan componentes necesarios, este comando los instala.

4) Verificar que TLauncher quedó instalado
which tlauncher


Si aparece una ruta (por ejemplo /usr/bin/tlauncher), significa que ya está listo para usarse.
