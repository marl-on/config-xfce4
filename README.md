# Dotfiles y configuración para Fedora Linux

Este repositorio lo he hecho con el propósito de compartir mis archivos para personalizar y configurar mi entorno de escritorio XFCE, especialmente usando la distribución de Fedora. También lo usare como un manual de como preparar y configurar mi entorno Fedora cuando haya cambiado de OS y quiera volver a utilizarlo.

#### Agradecimiento

Gracias a [rejarevaldy](https://github.com/rejarevaldy) porque este tema está fuertemente basado en su tema Lifeless para el entorno de escritorio XFCE y por proveer archivos que sirvieron como base para trabajar en mi propio tema.  
Para más temas visitar su [Repositorio](https://https://github.com/rejarevaldy/dotfiles).

## Contenido

* [1. Información del Sistema](#información-del-sistema)
* [2. Capturas](#capturas)
* [3. Dotfiles y archivos](#dotfiles-y-archivos)
* [4. Preparación inicial](#preparación-inicial)
* [5. Fuentes](#fuentes)
* [6. Tema](#tema)
* [7. Herramientas](#herramientas)
* [8. Atajos](#atajos)

## Información del Sistema

- **SO**: Fedora
- **Shell**: Zsh
- **Entorno de Escritorio**: [XFCE4](https://xfce.org/)
- **Panel**: XFCE-Panel
- **Fuente**: [Inconsolata](https://fonts.google.com/specimen/Inconsolata)
- **Fuente Monoespaciada**: JetBrains Mono
- **Editor de Texto:** [Helix](https://github.com/helix-editor/helix)
- **IDE**: [Visual Studio Code](https://github.com/Microsoft/vscode)
- **Navegador**: [Firefox](https://github.com/mozilla)
- **Tema Gestor de ventanas**: [Fluent Dark](https://github.com/vinceliuice/Fluent-gtk-theme)
- **Tema GTK**: [Graphite](https://github.com/vinceliuice/Graphite-gtk-theme)
- **Iconos**: [Papirus](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme)
- **Terminal**: [Terminator](https://gnome-terminator.org/)

## Capturas
![Escritorio](capturas/desktop.png)
![Escritorio con Ventanas y Fastfetch](capturas/fastfetch.png)

## Dotfiles y archivos

Estos son los archivos incluídos en este repositorio:
- Tema GTK: Graphite Dark
- Tema para Gestor de ventanas: Fluent Dark
- Iconos (Folders de color gris): Papirus, Papirus Dark, Papirus Light
- Configuración para interfaces GTK3-0 
- Configuración y temas para terminator
- Configuración para perfil de panel XFCE
- Configuración para Fastfetch
- Fondos de pantalla

## Preparación inicial

- Actualizar sistema, paquetes y repositorios

```
sudo dnf upgrade
```

- Agregar y habilitar repositorios RPM Fusion

```
sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```

```
sudo dnf config-manager setopt fedora-cisco-openh264.enabled=1
```

- Instalar git

```
sudo dnf install git
```

- Desinstalar dnfdragora y dnfdragora-updater

```
sudo dnf remove dnfdragora dnfdragora-updater
```

- Instalar gnome-software para flatpacks

```
sudo dnf install gnome-software
```

## Fuentes

```
sudo dnf install levien-inconsolata-fonts
sudo dnf install jetbrains-mono-fonts-all
```

## Tema

En mi experiencia, dependiendo del orden de la personlización de los elementos de XFCE4 (Ventanas, barras de título e ícono) pueden no aplicarse como esperado.   Este es el orden que me funcionó:

### Menú Apariencia
1.  Apartado de Estilo y aplicar Graphite-dark
2.  Apartado de Iconos y aplicar Papirus-Dark
3.  Apartado de Letra, en Fuente predeterminada aplicar Inconsolata Regular 11pt
4.  Apartado de Letra, en Fuente monoespaciada aplicar JetBrains Mono Regular 10pt

### Gestor de ventanas
1.  En Estilo, luego Tema y aplicar Fluent-Dark
2.  En Estilo, en Tipografía del título aplicar Inconsolata Regular 11pt
3.  En Estilo, en Alineación del título escoger Izquierda y en distribución de los botones colocar menú, título, minimizar, maximizar y cerrar.

## Herramientas

- Paquetes para manejo de archivos comprimidos

```
# archivos .rar solo pueden visualizarse y extraerse, no creados  
sudo dnf install zip unzip unrar p7zip pzip-plugins zstd
```

- LightDM GTK Greeter para interfaz de inicio e ingreso de credenciales

```
sudo dnf install lightdm-gtk-greeter-settings
```

## Atajos

- Historial portapapeles

```
# Super + V
# Comando para llamar ventana emergente
xfce4-popup-clipman
```

&nbsp;
