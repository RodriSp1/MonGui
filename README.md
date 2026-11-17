# MonGui 🐒🎸

Una web hecha en un solo archivo (`index.html`) para practicar guitarra, ukulele y flauta dulce. Incluye acordes con sonido real, rasgueos, afinador usando el micrófono, géneros musicales y un espacio para guardar tus propias grabaciones.

Todo está escrito en HTML, CSS y JavaScript puro, sin librerías externas y comentado en español para que cualquiera le pueda meter mano.

---

### 📂 Estructura del proyecto

Si vas a clonar o subir esto a tu propio repositorio, así es como se organizan los audios para que la página los reconozca:

```text
/
├── index.html          # Toda la app (estilos, estructura y lógica)
├── README.md
├── sonidos/            # Grabaciones de los acordes y rasgueos
│   ├── lista.json      # Se genera desde la misma página
│   ├── guitarra-clasica/
│   │   ├── Am.m4a
│   │   ├── Am-arriba.m4a   (opcional)
│   │   ├── apagado.m4a     (opcional)
│   │   └── rasgueos/
│   │       └── el-mas-usado.m4a
│   ├── guitarra-acustica/
│   ├── guitarra-electrica/
│   ├── ukulele-soprano/
│   ├── ukulele-concierto/
│   └── flauta/
└── canciones/          # Tus covers o canciones del repertorio
    ├── canciones.json  # Se genera desde la página
    └── mi-cancion.m4a
```
*(Acepta `.mp3`, `.wav` o `.m4a`, por ejemplo las notas de voz directo del iPhone).*

---

### 🎙️ Cómo agregar tus propios sonidos

1. Graba cada acorde (con un rasgueo de 1 a 3 segundos basta).
2. Entra a la pestaña **Mis sonidos** en la página, elige el instrumento y ve subiendo los archivos. No hace falta que les cambies el nombre antes, la app lo hace sola.
3. Dale a **Descargar todos con nombre correcto** y después a **Descargar lista.json**.
4. Mete los audios en `sonidos/<instrumento>/` y el `lista.json` en la raíz de `sonidos/`.
5. Sube la carpeta a tu repo en GitHub.

**Para subir canciones al Repertorio:**
Entra a **Repertorio**, sube tu pista con el nombre y artista, dale a **Descargar para publicar** y mete los audios junto con `canciones.json` dentro de la carpeta `canciones/`. *(Ojo: GitHub no deja subir archivos de más de 25 MB directo desde el navegador).*

---

### 🚀 Correrlo en local o subirlo a GitHub Pages

* **En tu compu:** Ábrelo usando la extensión **Live Server** de VS Code. Si abres el `index.html` directo con doble clic, el navegador bloquea el acceso al micrófono y a las carpetas de audio locales por seguridad.
* **En internet (GitHub Pages):** Sube tus archivos a un repo público, ve a **Settings → Pages**, elige la rama `main` (carpeta `/root`) y guarda. En un par de minutos queda en línea.

---

### 🛠️ Personalización rápida

Si quieres moverle al código, busca estas partes dentro del `index.html`:

* **Colores:** Variables en `:root` al inicio del `<style>`.
* **Usar audio sintetizado (sin grabaciones):** Cambia `PERMITIR_SINTETIZADO` a `true` en el script.
* **Nuevos acordes, ritmos o géneros:** Busca los objetos `ACORDES`, `UKE_ACORDES`, `PATRONES` y `GENEROS`.
* **Créditos y enlaces:** En la sección `creador` del HTML.

---

Hecho por **Rodri Santini** ([@ronits.ss](https://www.instagram.com/ronits.ss)).  
*Las letras se jalan de la API de [lyrics.ovh](https://lyricsovh.docs.apiary.io/). Las digitaciones las armé y revisé a mano; si notas algún dedo raro, échame un grito.* 🐒