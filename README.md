# 📜 Heraldic Player: El Ingenio Musical del Reino

En el amanecer de aqueste siglo de silicios y algoritmos, un heraldo recorre las almenas anunciando una obra nueva: **Heraldic Player**, un reproductor de la gran biblioteca de YouTube **forjado enteramente en los talleres de Python**. Posee su propia interfaz gráfica sobre los cimientos de *pygame* y una estética extraída directamente de la heráldica medieval: un severo blanco y negro, filigranas de oro, espadas cruzadas, coronas, castillos y flores de lis.

No es aqueste un burdo envoltorio para las interfaces comerciales de moda. Es una **pieza artesanal, escrita línea por línea**, diseñada para ejecutarse en vuestro propio feudo local, sin cuentas extranjeras, sin espías ni telemetrías, y sin promesas vacías. Toma al usuario del sistema como único señor del castillo y guarda su perfil en `~/.ytmusic_cmd/profiles.json`, tal como un escribano anotaría cada sesión en su pergamino.

---

## I. Las Puertas del Castillo
Al abrir el artefacto, no os recibe un menú frío y desalmado. Contemplaréis una introducción heráldica: **dos espadas que convergen sobre un sol radiante**, un destello dorado y, finalmente, el nombre de la casa: *Heraldic Player*. El señor recibe además un saludo aleatorio, como si un heraldo distinto le diese la bienvenida cada mañana:

* 📜 *«¡Paz y bien, mi señor! Que los acordes guíen vuestra jornada.»*
* 🪕 *«El trovador afina su laúd.»*
* 🏰 *«Las puertas del castillo se abren de par en par.»*

---

## II. La Búsqueda, Afilada como una Hoja de Toledo
El motor de búsqueda no se conforma con una sola estrategia; interroga a la gran biblioteca a través de **cuatro senderos en cascada**, respetando el orden real del reino y no una burda imitación:

1. Petición directa a la URL de resultados vía `yt-dlp`, con el parámetro `sp` correctamente codificado.
2. Una consulta propia a *InnerTube* mediante `urllib`, independiente del extractor general.
3. Lectura directa de la página de resultados y decodificación de `ytInitialData`.
4. Como último recurso, el conjuro `ytsearchN` del propio `yt-dlp`.

Si `yt-dlp` flaquease, el ingenio lo detecta y se actualiza a sí mismo por la vía de `pip`. Si todo lo demás fallase, deja un registro honesto en `search_error.log`. **No hay magia negra aquí: es ingeniería blindada en acero.**

---

## III. Filtros, Estandarte de Reproducción y Biblioteca
Cada resultado es clasificado con juicio: cantar, vídeo o cantar de larga duración (podcast), según su canal, duración y título. **A la izquierda se despliega la cola de reproducción**, alzándose como el estandarte de vuestra marcha musical; a la derecha, la biblioteca custodia vuestros cantares favoritos, el historial, las listas guardadas y las tonadas recientes. Las listas salvadas se sincronizan automáticamente al abrir el ingenio, portando su marca de tiempo y la portada del primer cantar.

---

## IV. El Ecualizador y el Arte del Tono
Bajo la estampa del cantar que resuena, **un ecualizador de cuarenta bandas pulsa con vida propia**, leyendo el audio en vivo mediante `ffmpeg` y descomponiéndolo en tiempo real con las matemáticas de `numpy`. No es mero adorno: respira y danza al son de la música.

El control de velocidad os permite marchar desde un paso lento de `x0.50` hasta un galope de `x2.00`, aplicado por el místico `VLC` sin alterar el tono. El control del tono os permite elevar o descender la melodía hasta doce semitonos, procesando el flujo con `ffmpeg` (usando `rubberband` si estuviere disponible, o el truco de `asetrate` con `atempo` en caso contrario). Los archivos procesados se guardan en una solana (caché) que se purga sola al superar los 250 MB.

---

## V. Logística de Suministros y Descargas
Aprovisionar vuestras arcas es tan sencillo como pulsar la tecla **O** para el cantar activo, o la **W** para toda la vista del inventario. Los archivos desembarcan seguros en `~/Music/YTMUSIC_CMD`, convertidos al formato MP3 si `ffmpeg` estuviere en los talleres, o a M4A si no lo estuviere. El ingenio resuelve la presencia de `ffmpeg` por sí solo, incluso si debe importarlo desde los almacenes de `imageio-ffmpeg`.

---

## VI. La Pantalla Principal: Una Vidriera Animada
El modo hogareño no es una lista inerte. Es **una vidriera gótica animada con estrellas doradas que titilan y flotan lentamente** por la pantalla. Sobre ella se despliega un inventario de anaqueles horizontales: vuestras listas guardadas, los cantares recientes, las tonadas más escuchadas, vuestros favoritos y las sugerencias del bardo basadas en vuestro historial. Las portadas se cargan en hilos paralelos, por lo que **la interfaz jamás se detiene a esperar por las redes externas**.

---

## VII. Sin Tributos, Sin Cuentas, Sin Ruido
No hay aquí accesos de Google, ni protocolos OAuth, ni contraseñas (*tokens*) extranjeras. El usuario del sistema operativo es el único señor y soberano. Todo se guarda en vuestras propias tierras. El artefacto instala sus propias dependencias si faltasen (`yt-dlp`, `python-vlc`, `pygame`, `pillow`, `numpy`, `imageio-ffmpeg`) y se reinicia solo tras la primera forja. Si el entorno de `VLC` no estuviere en el reino, intentará convocarlo mediante los heraldos del sistema (`winget`, `brew`, `apt`, `dnf` o `pacman`), según los fueros del territorio donde se ejecute.

---

## VIII. Los Atajos del Caballero

| Tecla / Atajo | Acción Consagrada |
| :---: | :--- |
| **Espacio** | Pausar y reanudar el cantar activo. |
| **N / P** | Avanzar al siguiente cantar o regresar al previo. |
| **+ / -** | Elevar o descender el volumen del elixir musical. |
| **← / →** | Retroceder o avanzar diez segundos en el tiempo. |
| **[ / ]** | Minorar o aumentar la velocidad del galope. |
| **, / .** | Descender o elevar el tono por un semitono. |
| **S / R** | Alterar el orden (azar) y repetir el cantar. |
| **F** | Marcar como favorito de vuestras arcas. |
| **G** | Guardar la lista actual en el pergamino. |
| **Y** | Sincronizar todas las listas guardadas del reino. |
| **I** | Regresar al hogar (la vidriera animada). |
| **L** | Desplegar la gran biblioteca. |
| **/** | Invocar el motor de búsqueda. |
| **Q** | Clausurar el ingenio y salir en paz. |

---

## IX. Breve Manifiesto
*Heraldic Player* no aspira a ser el soberano más rápido ni el más colosal del orbe. **Su único fin es ser honesto**: usar la gran biblioteca sin intermediarios, descargar sin pedir venia a ningún señor, ecualizar sin comerciar con vuestros secretos y vestir todo el conjunto con la solemnidad de un escudo de armas. Un ingenio escrito para perdurar, para ser leído y para sonar con fuerza en las tabernas.

---
*¡Que la música llene vuestra taberna, Señor de los Acordes!*
