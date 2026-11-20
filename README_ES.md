# Titanfall Ultimate Expansion — base de desarrollo 0.1.0

**Estado: proyecto fuente inicial; todavía NO es un `.jar` instalable ni la expansión completa.**

## Qué implementa esta primera etapa

- Registra huevos de aparición para los 12 Titanes humanoides y 8 chasis/frames que ya están registrados por `Titan Combat 2.10.0`.
- Añade los huevos a la pestaña creativa de huevos de aparición.
- Añade una receta individual para cada huevo.
- Usa los IDs reales observados en `ModEntities` del archivo `titancombat-2.10.0.jar`.

## Dependencias

- Minecraft Java 1.20.1
- Forge 47.x
- Titan Combat: Frontline Mechs 2.10.0
- Simple Voice Chat 1.20.1-2.6.27 es opcional para la futura integración de voz; esta etapa todavía no procesa audio ni reconoce órdenes.

## Cómo compilar

1. Instala Java 17.
2. Instala Gradle 8.1 o superior.
3. Copia `titancombat-2.10.0.jar` a `run/mods/` para probar en cliente.
4. Desde la carpeta del proyecto ejecuta `gradle build`.
5. El archivo compilado aparecerá en `build/libs/`.

El proyecto declara la dependencia obligatoria `titancombat` en `mods.toml`. No incluye ni redistribuye el archivo original de Titan Combat.

## Importante sobre las recetas

Cada receta usa:
- 1 batería de Titán de Titan Combat (`titancombat:titan_battery`)
- 1 bloque de hierro
- 1 ingrediente especial que diferencia la receta

## Próximas etapas pendientes

Esta base NO implementa todavía:
- BT-7274 ni los Titanes adicionales Atlas, Ogre, Stryder y Brute.
- IA autónoma, órdenes, protección o combate de compañero.
- Pilotaje mejorado, animaciones de entrada/salida ni eyección.
- Reconocimiento de voz en español.

El archivo recibido de voz es **Simple Voice Chat**, no Voice Survival. Simple Voice Chat expone paquetes de audio mediante su API, pero hace falta integrar un motor de reconocimiento de voz y diseñar el procesamiento de comandos. No se debe afirmar que ya escucha o entiende al jugador hasta implementarlo y probarlo.
