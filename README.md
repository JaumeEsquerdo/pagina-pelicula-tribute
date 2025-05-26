# pagina-pelicula-tribute
Para poner en práctica lo aprendido sobre animaciones. Hago esta landing page, con total referencia a la página tribute de 'The Goonies' , que encontré mientras buscaba inspiración para dar un salto a las páginas webs que estaba realizando. Digamos que esta es mi primera página con animaciones avanzadas.

# Partes para hacer de la página (pelicula JAWS)

- 1: zoom
 💡 Recomendación: El efecto de zoom mientras se hace scroll puede funcionar muy bien si haces que el fondo se acerque con varios layers de parallax (olas, cielo, gaviotas, etc.), mientras la aleta del tiburón aparece lentamente.

    - zoom mientras hace scroll hacia la playa donde se ve la aleta del tiburón
    - al llegar al máximo zoom, aparece el título de la película

- 2: transición
💡 Recomendación: Este momento puede simular muy bien el paso de estar fuera del agua a "sumergirse" (como si fueras el tiburón). Puedes hacer el difuminado con un gradiente oscuro y filtros CSS.

    - transición con un enfoque tipo difuminado de la primera parte a la siguiente, con esta parte donde se imitaría con el scroll el efecto tipo cuando vas sumergiendo en la playa
    - mini texto

- 3: parte datos de interés de la película con un masonry layout (con cards??)

💡 Recomendación: Usar cards con interacciones hover puede ayudar a mantenerlo dinámico. Un masonry layout también se ve moderno y bien ordenado.

🤔 Mejoraría: Asegúrate de no sobrecargar con texto. Intenta incluir imágenes o gifs pequeños (como detrás de cámaras o posters).

- 4: parte de Personajes principales + ciudad donde ocurre todo

💡 Recomendación: Puedes hacer animaciones pequeñas al entrar en viewport (fade-in, slide, etc.). La ciudad puede mostrarse con un pequeño mapa animado o ilustración interactiva.

🤔 Extra idea: Puedes añadir un efecto de “cámara antigua” o “dossier policial” para los personajes, para dar un toque más narrativo.

- 5: fin. algún link de interés + cierre final comentando que es un tributo
💡 Recomendación: Muy bien que incluyas un mensaje de que es un tributo. Puedes usar tipografía retro o tipo póster de cine clásico.
    - botón de volver al inicio


🚀 Sugerencias extra:
Añade un loader con efecto tipo "proyector de cine antiguo". SOLO SI REQUIERE MUCHA CARGA ALGUNA ANIMACION... tipo contador 3...2...1...

Considera una versión responsive bien cuidada, ya que parallax puede ser problemático en móvil.

Si usas sonido, dale opción de apagar/encender (por accesibilidad).

## Elementos visuales necesarios! Assets a tener para el parallax

- Objetivo: scroll descendente desde la playa hacia el tiburón
Es como si tú, el espectador, estuvieras caminando hacia el mar… y luego, lentamente, bajaras bajo el agua.

| Capa | Nombre                         | Tipo       | `z-index`     | Visibilidad inicial                |
| ---- | ------------------------------ | ---------- | ------------- | ---------------------------------- |

| 1️⃣  | **Cielo**                      | Fondo      | `z-index: 0`  | Visible desde el inicio            |

| 2️⃣  | **Gaviotas (PNG)**             | Flotante   | `z-index: 1`  | Encima del cielo                   |

| 3️⃣  | **Playa (con arena)**          | Fondo      | `z-index: 2`  | Visible desde el inicio            |

| 4️⃣  | **Mar lejano (agua lejana)**   | Fondo      | `z-index: 3`  | Aparece mientras haces scroll      |

| 5️⃣  | **Mar cercano (olas grandes)** | Fondo      | `z-index: 4`  | Cubre parte de la playa al avanzar |

| 6️⃣  | **Aleta del tiburón (PNG)**    | Flotante   | `z-index: 5`  | Se muestra en el momento cumbre    |

| 7️⃣  | **Texto “JAWS” (h1)**          | Texto      | `z-index: 6`  | Aparece tras la aleta              |

| 8️⃣  | **Fade oscuro / sumersión**    | Transición | `z-index: 10` | Se activa al terminar la intro     |

### Animación esperada: 

Parallax: al hacer scroll, que cada capa se mueva a distinta velocidad (transform: translateY()).

Gaviotas: flotan o se mueven muy lentamente en loop.

Aleta: aparece lentamente con opacity + scale.

Texto “JAWS”: con fade-in + letter-spacing amplio.

Fade oscuro: opacity desde 0 a 1 mientras haces scroll.

- Características de las imágenes

| Imagen                   | Tipo de recorte         | Formato recomendado                              |
| ------------------------ | ----------------------- | ------------------------------------------------ |
| Cielo                    | Completa, rectangular   | JPG o PNG sin transparencia                      |
| Playa                    | Completa, rectangular   | JPG o PNG sin transparencia                      |
| Mar lejano y mar cercano | Completa, rectangular   | PNG sin transparencia                            |
| Gaviotas                 | Elemento flotante       | PNG con fondo transparente                       |
| Aleta del tiburón        | Elemento flotante       | PNG con fondo transparente                       |
| Fade oscuro              | Gradiente o capa CSS    | CSS (`linear-gradient`) o PNG negro transparente |
| Texto título             | Texto HTML o imagen SVG | h1 o SVG estilizado                              |
