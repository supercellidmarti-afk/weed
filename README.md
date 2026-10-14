# GreenLeaf — Spigot 26.3

Plugin de roleplay ficticio: semillas plantables, cosecha de hojas, elaboración de porros, efectos de náusea/velocidad y partículas de humo.

## Requisitos
- Spigot 26.3
- JDK 25
- Maven 3.9+

## Compilar
Desde esta carpeta:
```bash
mvn clean package
```
Copia `target/GreenLeaf-1.0.0.jar` a `plugins/` y reinicia el servidor.

## Uso
- `/weed semillas [cantidad]`
- `/weed hoja [cantidad]`
- `/weed papel [cantidad]`
- `/weed porro [cantidad]`
Solo operadores tienen permiso para dar objetos.
1. Usa las semillas sobre tierra de cultivo.
2. Espera a que la planta de trigo visual madure.
3. Rómpela para recoger hoja y, a veces, semillas.
4. Combina una hoja y un papel en la mesa de crafteo para crear un porro.
5. Haz clic derecho con el porro para fumarlo: náusea, velocidad y partículas de humo.

## Resource pack
La carpeta `resourcepack/` incluye texturas pixel-art y modelos de ejemplo. El `pack.mcmeta` puede requerir ajustar `pack_format`/`min_format`/`max_format` según el formato exacto que solicite tu cliente 26.3. Los overrides de `custom_model_data` incluidos son de compatibilidad de ejemplo y conviene validarlos con el cliente 26.3 antes de publicar. Para que el servidor lo entregue automáticamente, aloja el ZIP en una URL HTTPS pública y configura `resource-pack` en `server.properties` (la configuración exacta depende del método de hosting).

## Notas técnicas
- La planta usa visualmente el cultivo de trigo vanilla para evitar NMS; el plugin registra qué bloques son suyos.
- Los modelos/texturas usan CustomModelData 1001 (semillas), 1002 (hoja), 1003 (porro).
- Haz copia de seguridad antes de probarlo en un servidor real.
