# 🎵 R&A Downloader

> Parte del ecosistema **Ritmo & Algoritmo** — donde la programación se encuentra con el sonido.

**R&A Downloader** es una herramienta portable para Windows que permite disponer de audio sin conexión desde YouTube y cientos de plataformas más. Interfaz gráfica, sin instalación, sin configuración, sin dependencias. Descomprimís y ejecutás.

<!-- 📸 CAPTURA SUGERIDA: screenshot de la ventana principal de la app mostrando la interfaz completa — campo de URL, opciones de formato/calidad, barra de progreso y log de salida -->

---

## ✨ ¿Qué hace?

- 🌐 Descarga audio desde **YouTube, SoundCloud, Twitch, Twitter/X, Instagram** y [cientos de plataformas más](https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md)
- 🎵 Exporta en **MP3, M4A, FLAC, WAV u OGG** con control de calidad (máxima, alta, media, baja)
- 📋 Soporta **playlists completas** o descarga individual
- 🏷️ Incrusta **metadatos y miniaturas** automáticamente en el archivo
- 📁 Recuerda la **última carpeta de descarga** usada
- 📊 Muestra **barra de progreso en tiempo real** con velocidad y ETA
- 📦 **100% portable** — los tres ejecutables van juntos, sin tocar el sistema
- 🪟 Compatible con **Windows 10 y Windows 11** (64 bits)

---

## 📦 Contenido del paquete

```
RyA-Downloader-vX.X.X.zip
│
├── ra_downloader.exe   ← Aplicación principal (interfaz gráfica)
├── yt-dlp.exe          ← Motor de descarga
├── ffmpeg.exe          ← Procesador y conversor de audio
├── r_a.ico             ← Ícono de la aplicación
└── RyA-Downloader-Instructivo.pdf  ← Guía de instalación y uso
```

> ⚠️ Todos los archivos deben estar **siempre en la misma carpeta**. Si movés solo el `ra_downloader.exe`, la app no va a encontrar a `yt-dlp` y `ffmpeg` y no va a funcionar.

---

## 🚀 Descarga e instalación paso a paso

### 👉 [⬇ Descargar última versión](https://github.com/juandejunin/ra-downloader/releases/latest)

---

### Paso 1 — Descargar el `.zip`

Andá a la sección **[Releases](https://github.com/juandejunin/ra-downloader/releases)** y descargá el archivo **`RyA-Downloader-vX.X.X.zip`**.

<!-- 📸 CAPTURA SUGERIDA: screenshot de la página de Releases en GitHub mostrando el .zip para descargar -->

---

### Paso 2 — Descomprimir

Hacé clic derecho sobre el `.zip` → **"Extraer todo..."** y elegí la carpeta donde querés tener la app (por ejemplo `C:\Programas\RyA-Downloader`).

> ✅ No hace falta instalador. No escribe nada en el registro de Windows. No necesita permisos de administrador.

<!-- 📸 CAPTURA SUGERIDA: screenshot del explorador de Windows mostrando los archivos ya descomprimidos en su carpeta -->

---

### Paso 3 — Ejecutar (y qué hacer si Windows lo bloquea)

Doble clic en **`ra_downloader.exe`** para abrir la app.

#### ⚠️ Windows SmartScreen puede bloquear la app — esto es normal

La primera vez que ejecutés el `.exe`, es probable que Windows muestre una pantalla azul de advertencia que dice **"Windows protegió su PC"**. Esto **no significa que la app sea peligrosa**.

Ocurre porque el ejecutable fue generado con PyInstaller y no está firmado con un certificado de pago. Es un comportamiento normal en aplicaciones independientes que no provienen de una tienda oficial.

**¿Cómo saltear el bloqueo?**

1. En la pantalla azul, hacé clic en **"Más información"**

<!-- 📸 CAPTURA SUGERIDA: screenshot de la pantalla azul de SmartScreen mostrando el botón "Más información" -->

2. Aparece el botón **"Ejecutar de todas formas"** — hacé clic ahí

<!-- 📸 CAPTURA SUGERIDA: screenshot del segundo paso de SmartScreen con el botón "Ejecutar de todas formas" visible -->

3. La app abre normalmente. Windows no vuelve a preguntar para ese archivo.

> 🛡️ Si tu **antivirus** también lo marca: es un falso positivo muy común en `.exe` generados con PyInstaller. Podés agregar la carpeta de la app como excepción en tu antivirus.

---

### Paso 4 — ¡Listo para usar!

Al abrir la app verás primero una pantalla de bienvenida breve, y luego la interfaz principal.

<!-- 📸 CAPTURA SUGERIDA: screenshot del splash screen de R&A Downloader -->

---

## 🖥️ Cómo usar la app

1. **Pegá la URL** del video o audio que querés descargar (o usá el botón *Pegar*)
2. **Elegí el formato** de audio: `mp3`, `m4a`, `flac`, `wav` u `ogg`
3. **Elegí la calidad**: máxima (0), alta (2), media (5) o baja (7)
4. **Seleccioná la carpeta** de destino (se recuerda entre sesiones)
5. Activá las opciones que necesitás: metadatos, miniatura, playlist
6. Hacé clic en **Descargar** y seguí el progreso en la barra y el log

<!-- 📸 CAPTURA SUGERIDA: screenshot de la app en plena descarga, con la barra de progreso activa y el log mostrando la salida de yt-dlp -->

---

## 🔧 Requisitos del sistema

| Requisito | Detalle |
|-----------|---------|
| Sistema operativo | Windows 10 / Windows 11 (64 bits) |
| Instalación | ❌ No requerida |
| Permisos de administrador | ❌ No requeridos |
| Espacio en disco | ~50 MB para la app + espacio para tus descargas |
| Conexión a internet | ✅ Requerida para obtener los archivos |

---

## ❓ Preguntas frecuentes

**¿Puedo mover la carpeta de lugar después de descomprimir?**
Sí, podés mover la carpeta entera donde quieras. Solo no separes los archivos entre sí.

**¿Funciona sin internet?**
La app abre sin internet, pero necesitás conexión para obtener los archivos. Al abrir también intenta cargar configuración remota — si no hay internet, usa valores por defecto sin problema.

**¿La URL que pegué no funciona?**
Verificá que el sitio esté en la [lista de plataformas soportadas por yt-dlp](https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md). Si está en la lista y sigue fallando, fijate en el log de salida que muestra el error exacto y abrí un [Issue](https://github.com/juandejunin/ra-downloader/issues) con ese mensaje.

**¿Por qué solo descarga audio y no video?**
Esta versión está enfocada en audio. El soporte de video puede sumarse en una versión futura.

**¿Puedo descargar una playlist entera?**
Sí — pegá la URL de la playlist y activá la opción **"Es una playlist"** antes de descargar.

---

## 🗺️ Roadmap

- [x] Interfaz gráfica con tema oscuro
- [x] Múltiples formatos de audio
- [x] Barra de progreso en tiempo real
- [x] Soporte de playlists
- [x] Incrustación de metadatos y miniaturas
- [ ] Compatibilidad con Windows 7 (en evaluación)
- [ ] Descarga de video (MP4/MKV)
- [ ] Selector de calidad de video
- [ ] Soporte para subtítulos
- [ ] Versión en inglés del README

---

## 🤝 Reportar un problema

Este repositorio es exclusivamente de distribución — solo se publican los releases descargables.

¿La app no funciona como esperás? ¿Encontraste un bug? Abrí un [Issue](https://github.com/juandejunin/ra-downloader/issues) describiendo el problema e incluí el mensaje de error que aparece en el log de salida de la app. Lo reviso en cuanto pueda.

---

## 📜 Licencia

Este proyecto se distribuye bajo la licencia **MIT**.

Las herramientas incluidas tienen sus propias licencias:
- **yt-dlp** — [Unlicense](https://github.com/yt-dlp/yt-dlp/blob/master/LICENSE)
- **FFmpeg** — [LGPL 2.1+](https://ffmpeg.org/legal.html)

---

## 🎛️ Sobre Ritmo & Algoritmo

**R&A Downloader** es parte de **Ritmo & Algoritmo**, un proyecto personal que explora los puntos de contacto entre la programación y el sonido — herramientas, experimentos y utilidades donde el código y la música se cruzan.

📺 [Visitá el canal en YouTube](https://www.youtube.com/@ritmoyalgoritmo-p1z)

---

<p align="center">
  Hecho con 🎵 y 🐍 &nbsp;·&nbsp;
  <a href="https://github.com/juandejunin/ra-downloader/releases/latest">⬇ Descargar última versión</a>
  &nbsp;·&nbsp;
  <a href="https://www.youtube.com/@ritmoyalgoritmo-p1z">▶ Canal de YouTube</a>
</p>

