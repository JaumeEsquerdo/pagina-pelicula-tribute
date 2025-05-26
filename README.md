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

- Capas:

| Capa | Nombre                     | Tipo          | `z-index`     | Comentario                                                      |
| ---- | -------------------------- | ------------- | ------------- | --------------------------------------------------------------- |


| 1️⃣  | **Cielo**                  | Fondo         | `z-index: 0`  | Parte superior de la pantalla. Empieza visible.                 |

| 2️⃣  | **Playa**                  | Fondo         | `z-index: 1`  | Arena estática o con efecto de calor. Muy visible al principio. |

| 3️⃣  | **Mar cercano (superior)** | Fondo         | `z-index: 2`  | Parte del agua vista desde fuera, con olas animadas.            |

| 4️⃣  | **Mar lejano (submarino)** | Fondo         | `z-index: 3`  | Agua más profunda y oscura. A medida que haces scroll.          |

| 5️⃣  | **Silueta bajo el agua**   | Flotante      | `z-index: 4`  | Tiburón visto desde dentro del agua (oscuro, difuso).           |

| 6️⃣  | **Aleta del tiburón**      | Flotante      | `z-index: 5`  | Aparece conforme te acercas. Emergente.                         |

| 7️⃣  | **Gaviotas**               | Flotante      | `z-index: 6`  | Volando sobre la playa y el mar al principio.                   |

| 8️⃣  | **Título de la película**  | Flotante/Text | `z-index: 10` | Solo aparece tras la aleta, ya bajo el agua.                    |
