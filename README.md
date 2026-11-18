# Carreteras Zona 1 Coria (Norte-Oeste) — GitHub Pages

Visor listo para publicar:

- `index.html` — mapa completo (carreteras, PK, poblaciones del IGN, fondos IGN, GPS, Referencial/LRS, Wake Lock y coordenadas WGS84 / ETRS89 UTM 29N H29).
- `.nojekyll` — evita que GitHub procese los archivos con Jekyll.

## Sistema de coordenadas

Los SHP de partida están reproyectados a **ETRS89 / UTM 29N (H29, EPSG:25829)**, elipsoide GRS80, meridiano central -3°. El visor dibuja en lat/lon (WGS84) para Leaflet, pero muestra en el panel, los PK y las fichas tanto WGS84 como E/N UTM 29N en metros.

El campo `LONGITUD` del DBF viene en **metros**; el visor lo muestra en **km** en negrita, seguidos de `/` y los metros en la misma línea, igual que Zona 4.

El **Referencial/LRS** solo se actualiza al tocar la traza de la carretera (30 m): si haces clic fuera se conserva el último PK mientras buscas coordenadas. Con el GPS activo sigue tu posición.

El botón rojo **Búsqueda por Referencial** permite escribir una vía y su PK (p. ej. `CC-102` y `2+522` o `2522`): el mapa se centra en ese punto y resalta la carretera y el PK en rojo.

## Datos (18/11/2026)

- 69 carreteras, 16.448 vértices tras simplificar los SHP H29 con tolerancia 0,5 m.
- 474 puntos kilométricos (campo `Number`).
- 80 núcleos de población del IGN con habitantes, capital y altitud.

## Publicar en 5 pasos

1. Crea un repositorio **público** llamado `zona1-mapa`.
2. Sube los 3 archivos de esta carpeta: `index.html`, `README.md` y `.nojekyll`.
3. Escribe un mensaje de commit y pulsa **Commit changes**.
4. Ve a **Settings → Pages**, Source: **Deploy from a branch**, rama `main`, carpeta `/(root)`, **Save**.
5. Abre `https://inventario2020.github.io/zona1-mapa/`. En iPhone usa Safari y acepta el permiso de ubicación (Pages da HTTPS).
