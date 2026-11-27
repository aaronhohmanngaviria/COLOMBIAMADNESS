# Runas de Cobre

ARPG 2D por turnos ambientado en mitos y leyendas colombianas.

## Abrir en Unity

1. Instala **Unity 6.3 LTS** con Unity Hub.
2. En Unity Hub, selecciona **Add > Add project from disk** y abre la carpeta `RunasDeCobreUnity`.
3. Espera a que termine la importación. Unity crea `Assets/Scenes/Main.unity` automáticamente.
4. Abre esa escena y pulsa **Play**.

El proyecto no requiere paquetes externos. La versión original del navegador sigue disponible en `index.html` como referencia durante la migración.

> Unity no está instalado en el entorno de desarrollo, por lo que la escena y el juego deben validarse al abrir el proyecto con el Editor.

## 🎮 Controles en Unity

| Acción | Teclado / ratón |
|---|---|
| Mover | `WASD` / Flechas / clic en el mapa |
| Atacar | Clic en enemigo / `Espacio` |
| Cambiar arma activa | `X` (consume un turno) |
| Salto (2 casillas) | `Shift` + mover |
| Ficha de estadísticas | `C` |
| Pausa | `Esc` |

Los indicadores carmesí señalan ataques enemigos telegrafiados. Cada acción consume un turno.

## Estado de la migración

La primera versión Unity es un prototipo jugable: incluye las 12 capas, movimiento por turnos, enemigos y guardianes, ataques telegrafiados, cambio entre dos armas, botín y una tienda básica. Sus 180 PNG incluyen los sprites originales del héroe, criaturas, guardianes y sus impactos, suelos, rocas, árboles y muros de los 12 biomas, además de iconos de armas, monedas y pociones.

Los PNG se importan como recursos de `Assets/Resources/Sprites` con filtro **Point**, sin compresión ni mipmaps para preservar el pixel-art. Las fuentes editables de LibreSprite (`.aseprite`) están en `RunasDeCobreUnity/Art/LibreSprite`, una por sprite; las instrucciones para editarlas y exportarlas están en esa carpeta.

El HTML conserva la versión original completa como referencia. El equipo defensivo, las mejoras rúnicas y los comportamientos únicos de los jefes aún no están migrados a Unity.

## ⚔️ Estadísticas del juego original

- **DAÑO** — puntos por golpe
- **VIDA** — corazones (2 puntos = 1 ♥)
- **GANANCIA DE EXP** — % de experiencia obtenida
- **GANANCIA DE ORO** — % de oro obtenido
- **ARMADURA** — reduce daño y añade probabilidad de bloqueo

## ⚔️ Armas (portadas a Unity)

Puedes llevar un arma principal y una secundaria. Pulsa `X` para alternar entre ellas; cambiar de arma consume un turno.

| Arma | Alcance | Daño adicional | Recarga |
|---|---:|---:|---:|
| Espada Guerrero | 1 casilla | +3 | 2 turnos |
| Lanza | 2 casillas | +2 | 2 turnos |
| Arco | 5 casillas | +1 | 3 turnos |
| Dagas | 1 casilla | +1 por golpe, 2 golpes | 1 turno |

## 🗺️ Contenido pendiente de portar desde el original

- **12 capas/tierras** con temática propia (Laguna de Bachué, Cascada de Bochica, El Dorado, La Patasola, El Sombrerón, La Madremonte, El Mohán, La Llorona, El Hombre Caimán, El Silbón, El Duende, La Buina).
- **Jefes únicos** con fases, invocación de esbirros y ataques telegrafiados.
- **Sistema de equipo** por ranuras: Malla, Pantalón, Arma principal, Arma secundaria y Escudo.
- **Mejoras rúnicas** al subir de nivel (11 tipos).
- **Tienda del Guardián** entre capas.
- **Objetos legendarios** exclusivos por jefe.

## Ejecutar la versión original del navegador

No requiere instalación. Abre `index.html` en cualquier navegador moderno.

Para servirlo localmente:

```bash
# Opción 1: Python
python3 -m http.server 8000

# Opción 2: Node
npx serve .

# Opción 3: PHP
php -S localhost:8000