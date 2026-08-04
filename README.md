# 🎬 LACartoons Stremio Addon

Este proyecto es un complemento (addon) de código abierto para [Stremio](https://www.stremio.com/), diseñado para integrar de forma nativa y fluida el catálogo de series y caricaturas clásicas de `lacartoons.com` con audio Español Latino.

---

## ✨ Características

* **Catálogo Completo:** Acceso indexado a series, temporadas y episodios directamente en la interfaz de Stremio.
* **Streaming Optimizado:** Extracción dinámica de enlaces de video (`.m3u8`, `.mp4`) mediante scraping inteligente híbrido.
* **Respaldo con `yt-dlp`:** Uso integrado de herramientas de extracción secundaria para garantizar la estabilidad de los reproductores externos.

---
### 🚀 Mejoras Recientes y Estado del Proyecto

Este addon se actualiza constantemente para mejorar la estabilidad, seguridad y experiencia de usuario. Las últimas incorporaciones incluyen:

| Área | Mejora Implementada | Impacto para el Usuario |
| :--- | :--- | :--- |
| **🛡️ Seguridad** | Parche **CVE-2024-45296** (`path-to-regexp`) | Protege el servidor de ataques de denegación de servicio (ReDoS). |
| **💻 Multiplataforma** | Soporte nativo para **Linux y macOS** | Binarios `yt-dlp` incluidos para todos los sistemas operativos (PR #22). |
| **🎬 Calidad de Video** | Soporte para **HLS nativo** y corrección de Stremio Web | Reproducción fluida en navegadores y resolución óptima (PR #15, #19). |
| **🔍 Catálogo** | Filtros por género, cadena y sección "Recomendadas" | Búsqueda más precisa y descubrimiento de contenido (PR #11, #13). |
| **⚙️ Estabilidad** | Actualización a **Node.js 20** y Docker | Mayor rendimiento del servidor y compatibilidad con entornos modernos. |
| **🔗 Enlaces** | Uso de enlaces nativos de YouTube (sin proxy) | Carga más rápida y menor latencia en videos de YouTube (PR #7). |

> **Nota de Seguridad:** La actualización de `path-to-regexp` fue aplicada automáticamente por herramientas de seguridad IA y verificada manualmente para garantizar la compatibilidad con todas las rutas del addon.

---
## 🛠️ Requisitos Previos

Antes de realizar la instalación, asegúrate de contar con los siguientes elementos en tu sistema:
* **Node.js:** Versión 18 o superior recomendada.
* **Git:** Configurado en tu entorno local.
* **Binarios locales:** El ejecutable `yt-dlp.exe` debe estar ubicado en la raíz del proyecto para dar soporte al motor de extracción.

---

## 💻 Instalación y Ejecución Local

Sigue estos pasos desde tu terminal preferida (**PowerShell** o **Bash**) para desplegar el entorno de desarrollo:

### 1. Clonar el repositorio
Navega hasta el directorio donde desees almacenar el proyecto y clona el código fuente:
```powershell
git clone https://github.com
cd stremio-lacartoons
```

### 2. Instalar dependencias y binarios de automatización
Este comando instalará los módulos del framework y ejecutará de forma automatizada la descarga del navegador Chromium headless requerido por el motor de Playwright:
```powershell
npm install
```

### 3. Iniciar el servidor local
Pon en marcha el entorno de desarrollo utilizando el script nativo configurado:
```powershell
npm start
```

Una vez iniciado, el addon expondrá una interfaz local en la dirección:  
`http://127.0.0`

---

## 🎮 Cómo Vincular el Addon en Stremio

1. Mantén la terminal con el comando de ejecución **activa**.
2. Abre la aplicación de **Stremio** en tu computadora o en cualquier dispositivo dentro de tu misma red local.
3. Dirígete a la sección de **Addons** (icono de la pieza de rompecabezas).
4. Pega la URL local `http://127.0.0` en la barra de búsqueda superior.
5. Haz clic en el botón verde **Instalar**.

---

## 🤝 ¿Cómo colaborar?

¡Cualquier aporte para optimizar los selectores de scraping o la estabilidad del flujo de video es totalmente bienvenido!

1. Haz un **Fork** de este repositorio.
2. Crea una rama con tu nueva funcionalidad o corrección:
   ```bash
   git checkout -b feature/nueva-mejora
   ```
3. Registra tus cambios con un mensaje descriptivo:
   ```bash
   git commit -m 'feat: optimizar extractor de enlaces de video'
   ```
4. Sube la rama a tu repositorio remoto:
   ```bash
   git push origin feature/nueva-mejora
   ```
5. Abre un **Pull Request** detallando tus modificaciones.

---

## 📄 Licencia

Este proyecto se distribuye bajo la **Licencia MIT**. Consulta el archivo `LICENSE` para obtener más detalles.
