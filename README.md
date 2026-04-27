# Agenda · Cesar

Calendarios .ics suscribibles para Apple Calendar vía GitHub Pages.

## Calendarios incluidos

- `agenda-trabajo.ics` — Aeroméxico
- `agenda-freelance.ics` — Freelance
- `agenda-uam.ics` — UAM
- `agenda-escuela.ics` — UAM · Escuela
- `agenda-alimentacion.ics` — Alimentación
- `agenda-hogar.ics` — Hogar
- `agenda-familia.ics` — Familia
- `agenda-lectura.ics` — Lectura
- `agenda-educacion.ics` — Educación
- `agenda-crecimiento.ics` — Crecimiento personal

## Setup inicial (5 minutos)

### 1. Crea el repo en GitHub
```bash
# Crea un repo PÚBLICO llamado "agenda" (o el nombre que prefieras)
# Sube todos los archivos de esta carpeta al repo
git init
git add .
git commit -m "agenda inicial"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/agenda.git
git push -u origin main
```

### 2. Activa GitHub Pages
1. Ve al repo en GitHub
2. **Settings** → **Pages**
3. Source: **Deploy from a branch**
4. Branch: **main** / Folder: **/ (root)**
5. Guarda

Espera ~1 minuto. GitHub te dará una URL del tipo:
```
https://TU-USUARIO.github.io/agenda/
```

### 3. Suscribe cada calendario en Apple Calendar
Para cada archivo .ics:

**En Mac:**
1. Apple Calendar → **Archivo** → **Nueva suscripción de calendario**
2. Pega la URL: `https://TU-USUARIO.github.io/agenda/agenda-trabajo.ics` (cambia el nombre por cada calendario)
3. **Auto-actualizar:** cada hora
4. **Eliminar:** alertas, archivos adjuntos (opcional)

**En iPhone/iPad:**
1. Ajustes → Calendario → Cuentas → Añadir cuenta → Otra → **Añadir calendario suscrito**
2. Pega la URL completa

Repite con los 10 archivos. Listo: cada vez que actualices el repo, todos tus dispositivos verán los cambios en máximo 1 hora.

## Actualizar la agenda

1. Modifica la agenda en el HTML interactivo
2. Descarga los nuevos .ics (botón "Descargar 10 .ics" o individualmente por categoría)
3. Reemplaza los archivos en este repo
4. `git add . && git commit -m "actualizar agenda" && git push`
5. Espera ~1-60 minutos. Apple Calendar trae los cambios automáticamente.

## Notas

- Los UIDs de los eventos cambian cada vez que regeneras los .ics. Apple Calendar tratará cambios mayores como "evento nuevo + viejo eliminado" en lugar de "evento editado". Para ediciones puntuales (cambiar 1 evento), es mejor editarlo directamente en Apple Calendar.
- El repo debe ser **público** para que GitHub Pages sirva los archivos. Si tu agenda contiene info sensible, considera ofuscar títulos antes de subir.
- GitHub Pages tiene cache CDN — los cambios pueden tardar hasta 10 minutos en propagarse.
