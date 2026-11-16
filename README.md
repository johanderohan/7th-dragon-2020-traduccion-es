# 7th Dragon 2020 — Traducción al castellano

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Traducción al **castellano de España** de la versión japonesa de PSP de *7th Dragon 2020*
(NPJH-50459). Se ha traducido desde el japonés, sin usar el texto de ningún otro parche.

Se distribuye únicamente un **parche xdelta**. Necesitas tu propia copia del juego.

## Estado

**v1.0 — en revisión.** Todo el texto extraído está traducido y revisado, pero no se ha
completado una partida de principio a fin ni existe revisión humana independiente.
La traducción y su revisión están asistidas por IA.

- Historia, conversaciones con los residentes, encargos secundarios, terminales, menús,
  objetos, habilidades, enemigos, mensajes de combate, avisos del sistema y tutoriales.
- 12.613 cadenas con texto (9.273 distintas) en 1.101 tablas; ninguna queda en japonés.
- Fuente nueva con tildes, ñ, ü, signos de apertura y comillas españolas, a tamaño real y
  con los mismos colores que el original.
- 246 texturas redibujadas en 74 archivos: los 66 subtítulos del prólogo, los títulos de
  capítulo, las placas de zona y de mazmorra, las órdenes «Usar» y «Tirar», la leyenda del
  mapa y los rótulos de los minimapas del Ayuntamiento.
- Voces originales japonesas. Los rótulos gráficos que el juego original ya muestra en inglés
  (menú principal, órdenes de combate, estado) se conservan.

## Cómo aplicar el parche

1. Usa la ISO japonesa **NPJH-50459** que coincida con las huellas de abajo.
2. Aplica `7th.Dragon.2020.ES.v1.0.xdelta` con Delta Patcher, xdeltaUI o xdelta3.
3. Comprueba el tamaño y MD5 del resultado. El parche se aplica sobre el original japonés,
   no sobre otro parche.
4. Abre la ISO resultante en PPSSPP o en tu equipo compatible. Solo se ha probado en PPSSPP;
   no se ha comprobado en PSP física ni en PS Vita con Adrenaline.
5. Si tienes instalados los datos del juego japonés (DATA INSTALL), bórralos y vuelve a
   instalarlos con la ISO traducida. No mezcles los datos instalados con otra versión.

```sh
xdelta3 -d -s "7th Dragon 2020 (Japan).iso" \
  7th.Dragon.2020.ES.v1.0.xdelta "7th Dragon 2020 (Castellano).iso"
```

| Archivo | Tamaño en bytes | MD5 |
|---|---:|---|
| ISO japonesa original | 1.125.482.496 | `507131c25d65a6c0a028deb94b1cff44` |
| ISO resultante v1.0 | 1.125.482.496 | `4f48f34724c21b579b2f162d5948edfc` |

SHA-256 de la ISO resultante: `39a9d1b854957de33b57bee692e1323f57b45c1f6cc0d3a83ea25436fecb4bf2`.

## Comprobaciones

La construcción parte siempre del original y una auditoría lee de nuevo la ISO ya montada:
comprueba cada cadena traducida y cada textura contra lo esperado, que ningún archivo del
juego se solapa con otro, que todo lo que no se ha traducido queda idéntico y en su sitio, y
que no queda texto japonés. La única excepción son nueve archivos vecinos (121 KB en total)
que se desplazan o se recomprimen para hacer sitio al texto castellano; su contenido, una vez
descomprimido, es idéntico al original. El ejecutable original no se ha modificado.

Se ha jugado en el emulador, desde arranque en frío y partida nueva: aviso inicial, título,
dificultad, escena de apertura, creación de personaje (aspecto, clase, nombre, voz), exploración
de la plaza y del Ayuntamiento, conversaciones, tutoriales, menú (objetos con sus órdenes «Usar» y
«Tirar», equipo, estado, opciones con todos sus valores), varios combates completos con ataque,
habilidad, objeto, huida y combate automático, pantalla de resultado, subida de nivel, fin de
partida, y guardar y cargar una partida. Otro revisor miró todas las capturas de las dos rondas
principales (unas 2.000) comparándolas con el original: sin texto cortado, sin restos de japonés
en el texto y con los mismos colores. Las rondas se hicieron sobre candidatas anteriores a la
publicada; la publicada añade ajustes de la fuente (signos de apertura y cifras) y tiene su propio
arranque en frío y sus propios combates.

Del resto de texturas redibujadas (subtítulos del prólogo, títulos de capítulo, placas de zona,
leyenda del mapa y minimapas) solo se ha comprobado que se leen correctamente de la imagen; no
se han visto todavía dentro del juego.

El parche se ha reaplicado al original y reproduce exactamente la candidata publicada.
Las comprobaciones en emulador utilizan PPSSPP 1.20.4, compilación sin ventana, en Linux.

## Limitaciones conocidas

- No hay partida completa ni pruebas en hardware real. Solo se ha jugado el principio del
  juego; el resto de la historia, los encargos y las zonas tardías no se han recorrido en
  pantalla.
- **El nombre de los personajes solo se puede escribir en kana.** El juego original limita el
  teclado del sistema a hiragana y katakana; no se ha cambiado.
- La fuente es de paso fijo, con letras de 6 píxeles de ancho: es la única forma de que el
  castellano quepa sin modificar el ejecutable. Tras un nombre de longitud impar insertado
  por el juego (un enemigo, un objeto) puede verse un espacio algo más ancho de lo normal.
- Los nombres de objetos, habilidades y enemigos están limitados por el ancho de sus casillas
  y algunos se abrevian. Sus topes se han tomado del original y no todos se han visto en pantalla.
- Se conservan como en el original los logotipos, las voces, el vídeo de apertura, las cartelas
  caligráficas de entrada a cada zona, el aviso legal de arranque, las capturas de los
  tutoriales a pantalla completa y los carteles del escenario.
- En el PPSSPP sin ventana usado para las pruebas no se dibuja el texto de los diálogos de
  guardado del sistema; guardar y cargar funcionan.

Si encuentras un fallo, indica el lugar, qué estabas haciendo y la versión, y adjunta una
captura o partida guardada propia en una incidencia de GitHub o en la ficha del proyecto.

## Cambios

### v1.0 — 16 de noviembre de 2026

- Primera versión al castellano desde el japonés de PSP.
- Traducción con biblia de términos, revisión editorial cruzada de todos los lotes y
  unificación de nombres y términos.
- Fuente castellana, texturas redibujadas y parche que conserva en su sitio todo lo que no
  se traduce.

## Créditos y aviso legal

Proyecto de **johanderohan**. Traducción, revisión y herramientas asistidas por IA.
La fuente del texto se basa en la tipografía de mapa de bits «misc-fixed 6x13» de X11 (dominio
público). Los rótulos redibujados usan Noto Serif y DejaVu Sans Condensed (licencias libres);
no se distribuyen sus archivos de fuente.

Proyecto de aficionados, sin afiliación con los titulares de 7th Dragon ni del juego.
El juego, sus personajes, gráficos, música y marcas pertenecen a sus respectivos titulares.
Este repositorio no contiene la ISO ni herramientas que incluyan el texto del juego.

SHA-256 del parche v1.0: `57e20eb9ca4c02c6820caef6f4f9106fb979f60c4a63c4de7df0b6f5406ec3e0`.
