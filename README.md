<div align="center">

# 💖 Reconoce el Objeto ✨

### El juego de visión artificial en tiempo real donde dos equipos compiten por encontrar objetos antes que el rival

![Python](https://img.shields.io/badge/Python-3.9%2B-ff69b4?style=for-the-badge&logo=python&logoColor=white)
![YOLOv8](https://img.shields.io/badge/YOLOv8-Ultralytics-d400ff?style=for-the-badge)
![OpenCV](https://img.shields.io/badge/OpenCV-Visi%C3%B3n%20Artificial-ffb6c1?style=for-the-badge&logo=opencv&logoColor=white)
![Tkinter](https://img.shields.io/badge/Tkinter-Pantalla-ffd700?style=for-the-badge)
![Estado](https://img.shields.io/badge/Estado-Funcional-success?style=for-the-badge)

💗 ✨ 💖 ✨ 💗 ✨ 💖 ✨ 💗

</div>

---

## 📖 Tabla de contenidos

- [🌸 ¿Qué es?](#-qué-es)
- [🎮 Cómo se juega](#-cómo-se-juega)
- [⭐ Características](#-características)
- [🧰 Objetos reconocidos](#-objetos-reconocidos)
- [🛠️ Tecnologías](#️-tecnologías)
- [📦 Instalación](#-instalación)
- [🚀 Ejecución](#-ejecución)
- [⌨️ Controles](#️-controles)
- [🧠 Cómo funciona por dentro](#-cómo-funciona-por-dentro)
- [⚙️ Personalización](#️-personalización)
- [📂 Estructura del proyecto](#-estructura-del-proyecto)
- [🩹 Solución de problemas](#-solución-de-problemas)
- [🔮 Ideas a futuro](#-ideas-a-futuro)

---

## 🌸 ¿Qué es?

**Reconoce el Objeto** es un juego interactivo para dos equipos que usa **visión artificial en tiempo real**. La cámara web captura la escena, se divide la pantalla en dos mitades (**Equipo A** a la izquierda y **Equipo B** a la derecha) y la IA pide un objeto cualquiera: *"Encuentra: Tijeras"*.

El primer equipo que **muestre el objeto frente a la cámara** en su lado de la pantalla se lleva el punto. ¡Gana quien tenga más puntos cuando se acabe el tiempo! 🏆

Fue creado como demostración para la experiencia **UCB - IA Experience**, pensado para mostrar de forma divertida cómo una red neuronal de detección de objetos (**YOLOv8**) puede usarse en una dinámica de juego, con una estética **girly** llena de corazones 💗, destellos ✨ y colores rosa, magenta y dorado.

---

## 🎮 Cómo se juega

1. 🚀 Ejecuta el juego, se abrirá en **pantalla completa** con la imagen de tu cámara.
2. ⌨️ Presiona **`S`** en la pantalla de bienvenida para empezar.
3. 🎯 Aparece en la parte inferior un objetivo, por ejemplo **"Encuentra: Botella"**.
4. 🏃‍♀️ Cada equipo corre a buscar ese objeto y lo muestra a la cámara **dentro de su mitad** de la pantalla.
5. 💥 La IA detecta el objeto, dibuja un recuadro con su nombre en español y **suma un punto** al equipo que lo mostró.
6. 🔄 Se elige un nuevo objetivo y la ronda continúa durante **60 segundos**.
7. 👑 Al terminar el tiempo se anuncia al **ganador** (o el empate) y puedes reiniciar con **`R`**.

> 💡 **Regla de oro:** solo puntúa **un equipo por ronda**. Si ambos muestran el objeto a la vez, se prioriza al Equipo A; y hay un enfriamiento de 2 segundos para evitar puntos dobles con el mismo objeto.

---

## ⭐ Características

| | Característica |
|---|---|
| 🎥 | **Detección en tiempo real** con YOLOv8 nano sobre la cámara web |
| 👯‍♀️ | **Modo 2 equipos**: pantalla dividida en izquierda (A) y derecha (B) |
| 🇪🇸 | **Interfaz 100 % en español**: los objetos se traducen automáticamente |
| 🔀 | **Cola de objetos barajada**: todos los objetos aparecen antes de repetirse |
| ⚡ | **Inferencia optimizada**: solo se detectan las clases del juego, no las 80 de COCO |
| ⏱️ | **Temporizador** configurable (60 s por defecto) |
| 🏁 | **Pantalla de resultados** con ganador, marcador y lluvia de corazones |
| 🖱️ | **Botones táctiles/clicables** para *Saltar* objeto y *Salir* |
| 🖥️ | **Pantalla completa automática** adaptada a la resolución de tu monitor |
| 💅 | **Estética girly**: corazones animados, destellos, paneles translúcidos y paleta rosa/magenta/dorado |

---

## 🧰 Objetos reconocidos

El juego usa **12 objetos cotidianos** del conjunto COCO que YOLOv8 ya conoce:

| Inglés (COCO) | Español (en el juego) | | Inglés (COCO) | Español (en el juego) |
|---|---|---|---|---|
| `bottle` | 🍼 Botella | | `book` | 📓 Cuaderno |
| `cup` | 🥤 Vaso | | `scissors` | ✂️ Tijeras |
| `fork` | 🍴 Tenedor | | `clock` | ⏰ Reloj |
| `spoon` | 🥄 Cuchara | | `teddy bear` | 🧸 Oso de peluche |
| `cell phone` | 📱 Celular | | `toothbrush` | 🪥 Cepillo de dientes |
| `remote` | 📺 Control remoto | | `sports ball` | ⚽ Pelota |

---

## 🛠️ Tecnologías

- 🐍 **Python 3.9+**
- 🤖 **[Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)** — modelo `yolov8n.pt` (nano: rápido y ligero)
- 👁️ **OpenCV** — captura de cámara, dibujo de la interfaz y ventana a pantalla completa
- 🔢 **NumPy** — geometría de corazones/destellos y animaciones
- 🪟 **Tkinter** — solo para detectar la resolución de la pantalla

---

## 📦 Instalación

### Requisitos previos

- Python **3.9 o superior**
- Una **cámara web** conectada
- Un monitor (el juego se muestra en pantalla completa)
- *(Opcional pero recomendado)* una GPU compatible con CUDA para mayor fluidez

### Pasos

```bash
# 1. Clona el repositorio
git clone https://github.com/Luugallego17/Reconoce-el-Objeto.git
cd Reconoce-el-Objeto

# 2. (Recomendado) crea un entorno virtual
python -m venv venv
source venv/bin/activate        # En Windows: venv\Scripts\activate

# 3. Instala las dependencias
pip install -r requirements.txt
```

> ℹ️ El archivo `yolov8n.pt` (pesos del modelo) ya viene incluido en el repositorio. Tkinter viene con Python en Windows y macOS; en Linux instálalo con `sudo apt install python3-tk`.

---

## 🚀 Ejecución

```bash
python Juego_VA.py
```

Se abrirá la ventana **"UCB - IA Experience"** en pantalla completa. ¡Presiona **`S`** y a jugar! 💖

---

## ⌨️ Controles

| Acción | Tecla / Clic |
|---|---|
| ▶️ Empezar partida | `S` (en la pantalla de bienvenida) |
| ⏭️ Saltar al siguiente objeto | `N` o botón **SALTAR** (arriba a la derecha) |
| 🔁 Reiniciar tras terminar | `R` (en la pantalla final) |
| ❌ Salir del juego | `Q` o botón **SALIR** |

---

## 🧠 Cómo funciona por dentro

```
 Cámara ──► Espejo + redimensión a pantalla ──► YOLOv8 (solo 12 clases, conf ≥ 0.5)
                                                       │
                          ¿Detecta el objeto objetivo? ◄┘
                                   │
              centro de la caja < mitad de pantalla ?
                    ├─ Sí → Equipo A (izquierda)
                    └─ No → Equipo B (derecha)
                                   │
                  +1 punto  ·  nuevo objetivo  ·  cooldown 2 s
```

**Puntos clave del código (`Juego_VA.py`):**

- **Filtrado de clases** — se calcula `CLASES_VALIDAS` a partir de los nombres del modelo y se pasa a `model(..., classes=CLASES_VALIDAS)`, de modo que YOLO solo busca los objetos del juego (más rápido y con menos falsos positivos).
- **Asignación a equipos** — el centro horizontal del recuadro detectado (`cx_box`) se compara con `w // 2` para saber si el objeto está en el lado A o B.
- **Un punto por ronda** — una estructura `if / elif` da prioridad al Equipo A si ambos lados muestran el objeto a la vez; un cooldown de 2 s evita puntos duplicados.
- **Cola barajada** — `siguiente_objeto()` mezcla los 12 objetos y los va sacando uno a uno; cuando se agotan, vuelve a barajar. Así ningún objeto se repite hasta haberlos usado todos.
- **Interfaz con OpenCV** — corazones (`draw_heart`), destellos (`draw_sparkle`), paneles translúcidos (`overlay_rect`), marcadores y botones se dibujan directamente sobre cada frame. Los corazones de las esquinas "laten" usando una función seno.
- **Máquina de estados** — tres estados: pantalla de inicio → juego activo → pantalla final.

---

## ⚙️ Personalización

Todo se configura editando `Juego_VA.py`:

| Quieres... | Qué cambiar |
|---|---|
| ⏱️ Cambiar la duración de la partida | La variable `tiempo_limite` (en segundos) |
| 🧸 Añadir o quitar objetos | El diccionario `TRADUCCION` (usa los nombres de clases COCO de YOLO) |
| 🎯 Hacer la detección más/menos estricta | El parámetro `conf=0.5` en la llamada a `model(...)` |
| 🎨 Cambiar la paleta de colores | Las constantes `ROSA`, `MAGENTA`, `LILA`, `DORADO`, etc. (formato BGR) |
| 📷 Usar otra cámara | El índice en `cv2.VideoCapture(0)` (prueba 1, 2…) |
| 🧠 Mayor precisión | Cambia `yolov8n.pt` por `yolov8s.pt` / `yolov8m.pt` (se descargan automáticamente) |

---

## 📂 Estructura del proyecto

```
Reconoce-el-Objeto/
├── Juego_VA.py        # Código completo del juego
├── yolov8n.pt         # Pesos del modelo YOLOv8 nano
├── requirements.txt   # Dependencias de Python
└── README.md          # Este archivo 💖
```

---

## 🩹 Solución de problemas

| Problema | Solución |
|---|---|
| La ventana se cierra al abrir | La cámara no se pudo abrir. Revisa que esté conectada y no la use otra app; prueba otro índice en `VideoCapture`. |
| `ModuleNotFoundError` | Ejecuta `pip install -r requirements.txt` dentro de tu entorno virtual. |
| `No module named tkinter` (Linux) | `sudo apt install python3-tk` |
| El juego va lento | Cierra otras aplicaciones, usa GPU con CUDA o baja la resolución de la cámara. |
| No detecta mi objeto | Mejora la iluminación, acércalo a la cámara o baja el valor de `conf`. |
| No puedo salir | Pulsa `Q` o haz clic en el botón **SALIR**. |

---

## 🔮 Ideas a futuro

- 🏅 Ranking de puntuaciones históricas
- 🔊 Efectos de sonido y voz que anuncie el objeto
- 👥 Más de dos equipos o modo individual
- 🧠 Dificultades (objetos más raros, menos tiempo)
- 🌍 Selector de idioma

---

<div align="center">

### Hecho con 💖, ✨ y mucha visión artificial

**¡Gracias por jugar! Que gane la mejor** 👑

</div>
