```markdown
# prueba_psychopy_web

Contenido mínimo para publicar el experimento en GitHub Pages.

Archivos:
- index.html : página web que carga conditions.csv, reproduce audios y envía respuestas al Apps Script.
- conditions.csv : ejemplo con rutas relativas a la carpeta `stimuli/`.
- stimuli/ : carpeta con tus archivos WAV (NO incluida aquí; cópiala desde tu proyecto local).

Instrucciones para publicar en GitHub Pages (pasos rápidos)

1) Crear repositorio en GitHub
- Ve a https://github.com/new y crea un repo (ej: prueba_psychopy_web). Puedes hacerlo público (Pages funcionará para sitios públicos gratis).

2) Subir archivos (opciones)
Opción A — desde la línea de comandos (recomendado si usás git):
  mkdir prueba_psychopy_web
  cd prueba_psychopy_web
  # Copia aquí index.html, conditions.csv y la carpeta stimuli/
  git init
  git add .
  git commit -m "Initial commit - PsychoPy web export"
  # crea el repo en GitHub (sigue las instrucciones en la web para añadir remote), por ejemplo:
  git remote add origin https://github.com/tu-usuario/prueba_psychopy_web.git
  git branch -M main
  git push -u origin main

Opción B — subir por la web:
- En tu repo en GitHub haz click en "Add file" → "Upload files" y arrastra index.html, conditions.csv y la carpeta stimuli/.

3) Activar GitHub Pages
- En el repo en GitHub: Settings → Pages.
- Source: selecciona Branch: main, Folder: / (root).
- Click Save. Espera 1–5 minutos y tu sitio estará en:
  https://<tu-usuario>.github.io/<repo-name>/

4) Pruebas y comprobaciones
- Abre la URL de Pages en un navegador y prueba el experimento.
- Abre DevTools → Network/Console para confirmar que las peticiones POST van a tu ENDPOINT_URL y reciben {"status":"ok"}.
- Verifica la Google Sheet para confirmar que llegan las respuestas.

Advertencias y buenas prácticas
- Tu SECRET_TOKEN está incluido en index.html: si tu repo es público, cualquiera que vea la página podrá inspeccionar ese token. Para producción, considera mover la validación a un backend o usar otro método de autenticación.
- Mantén backups periódicos del sheet exportando CSV.
- Si quieres que no se exponga el token en la página, decime y te propongo una alternativa (GitHub Actions + proxy o servidor simple con Secrets).
```