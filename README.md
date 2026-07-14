# Bienestar Vascular · Pausas Activas 🌿

Temporizador de **pausas activas**, ejercicios guiados y píldoras de salud para
trabajadores remotos y *gamers*. Cuida tu circulación sin salir del navegador.

Proyecto **híbrido**, sin frameworks y sin nube (**HTML + CSS + Vanilla JS**):

- 🌐 **Web / PWA** — se abre en cualquier navegador y se puede instalar como app
  (funciona offline). Es lo que se publica en **GitHub Pages**.
- 🧩 **Extensión de Chrome** (Manifest V3) — con recordatorios en segundo plano.

Toda la información se guarda **solo en tu dispositivo** (`localStorage` en la web,
`chrome.storage.local` en la extensión). Sin cuentas, sin servidores.

## Funciones
- 3 modos (Profundo / Pomodoro / Gaming) + **rutina personalizable**.
- **Ejercicios guiados** durante cada pausa.
- Estadísticas semanales, racha y **reporte PDF** de autoseguimiento (no diagnóstico).
- 120 píldoras de salud, sonidos configurables, **No molestar**, copia de seguridad JSON.
- **Bilingüe** (Español / English), tema claro/oscuro y `prefers-reduced-motion`.
- **Tour interactivo** de bienvenida. 

## Estructura
```
bienestar-vascular/
├── index.html              # entrada WEB/PWA
├── popup.html              # entrada de la EXTENSIÓN
├── popup.css               # estilos (compartidos)
├── popup.js                # UI y lógica (compartida)
├── core.js                 # lógica pura del temporizador (probada)
├── i18n.js                 # sistema de idiomas (es/en)
├── background.js           # service worker de la extensión (MV3)
├── offscreen.html/.js      # audio de la extensión (Web Audio)
├── sw.js                   # service worker de la PWA (offline)
├── manifest.json           # manifiesto de la extensión
├── manifest.webmanifest    # manifiesto de la PWA
├── icons/  img/            # iconos e imágenes
└── tests/  package.json    # pruebas (node --test)
```

## Usar la web (PWA)
Ábrela servida por HTTPS (p. ej. GitHub Pages). En móvil/PC puedes pulsar
**«Instalar app»**. Nota: en la web los avisos llegan con la pestaña abierta;
para recordatorios en segundo plano, usa la extensión.

## Instalar la extensión (modo desarrollador)
1. Ve a `chrome://extensions` y activa **Modo de desarrollador**.
2. **Cargar descomprimida** → selecciona esta carpeta.
3. Fija el icono y ábrela.

## Pruebas
```bash
npm test        # o: node --test
```

## Publicar en GitHub Pages
El sitio se sirve desde la raíz del repositorio (rutas relativas, listo para subruta).

---
*Herramienta de autocuidado y autorregistro. No sustituye el consejo de un profesional de la salud.*
