# Registro de Entrenamiento

Versión digital de la planilla de seguimiento de alumnos (ejercicio · serie ·
peso · reps), pensada para usar solo desde el celular.

## Qué hace

- **Alumnos**: lista con buscador. Ficha con objetivo, frecuencia semanal,
  fecha de inicio, altura, peso, IMC y notas (lesiones, horarios…).
- **Medidas corporales**: peso, % grasa, cintura, cadera, pecho, brazo, muslo y
  pantorrilla, con historial, cambio desde la primera medición y gráficos.
- **Rutina por días** ("Día 1", "Día 2"…): ejercicios con cantidad de series y
  una nota (prono, drop…) y descanso. Los ejercicios se eligen de una
  **biblioteca** (tren inferior y superior) a la que se pueden sumar propios.
  Se puede armar de cero, desde una **plantilla** o **copiando** la rutina de
  otro alumno.
- **Entrenar**: cada serie arranca con el peso y las reps de la última vez.
  Si repite, toca el número de serie (✓). Si cambia, ajusta con **+ / −**
  (el paso del peso se configura, por defecto ±2,5 kg) o escribe el valor.
  Se pueden sumar o quitar series y ejercicios en el día; al terminar, la app
  ofrece guardar esos cambios en la rutina.
- **Por ejercicio**: RIR, descanso, técnica/observación y dolor o molestia
  (leve, moderado, fuerte). Si la vez anterior hubo dolor, aparece un aviso.
- **Repetir último entrenamiento**: desde la ficha (o al sumar un alumno) se
  arranca una sesión igual a la última, para ir modificándola en el momento.
- **Varios alumnos a la vez**: arriba de la sesión hay una barra con todos los
  que están entrenando; se pasa de uno a otro con un toque (cada uno queda
  donde se lo dejó) y con **+ Sumar** se agrega otro sin cerrar nada. Al
  terminar una sesión, la app pasa al siguiente alumno que sigue entrenando.
- **Progreso por ejercicio**: peso máximo, volumen (kg × reps) y una tabla con
  el mismo formato que la planilla en papel.
- **Respaldo**: descarga o comparte (WhatsApp, Drive, mail) un archivo `.json`
  con todo, y lo restaura en otro celular. También se puede exportar a Excel
  (`.csv`). La app avisa si pasó más de una semana sin hacer un respaldo.

## Cómo se usa

Es una página web que se instala como app y funciona **sin internet**. Los
datos se guardan **solo en ese celular** (no hay servidor ni cuenta), por eso
conviene hacer respaldos seguido.

1. Publicar este repositorio en un hosting estático con HTTPS (por
   ejemplo GitHub Pages: Settings → Pages → rama `main`, carpeta raíz; queda en
   `https://giovanacippitelli-png.github.io/Registro-de-entrenamiento-/`).
2. Abrir esa dirección en el celular:
   - **iPhone (Safari):** Compartir → "Agregar a inicio".
   - **Android (Chrome):** menú ⋮ → "Instalar app".
3. Desde **Ajustes** se puede cargar un *alumno de ejemplo* con datos de la
   planilla para probar.

## Archivos

- `index.html`: toda la app (HTML, CSS y JS sin dependencias).
- `sw.js`: service worker para que funcione sin conexión. Al publicar cambios,
  subir `VERSION` para que los celulares descarguen la versión nueva.
- `manifest.webmanifest` e íconos: lo necesario para instalarla como app.
