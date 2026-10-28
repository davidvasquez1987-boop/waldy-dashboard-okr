# Tablero OKR · Uniformes Waldy

Tablero interactivo de una sola página para seguir los **3 objetivos y 9 resultados clave (KR)** de la propuesta de innovación de Uniformes Waldy (planta Paipa – sede Bogotá).

No necesita instalación, servidor ni librerías: es un único archivo `index.html`.

## Qué permite hacer

- Cambiar el **valor actual** de cada KR con los botones **+** / **−** o escribiendo el número.
- Ver el **porcentaje de avance**, el **estado** (Cumplido, En camino, En riesgo, Crítico) y cuánto falta para la meta.
- Filtrar por objetivo (O1, O2, O3).
- Identificar desviaciones en el panel **Áreas de mejora** (los 3 KR más atrasados).
- Modo claro y oscuro.

## Cómo se calcula

- **Avance** = (valor actual − línea base) ÷ (meta − línea base), limitado entre 0% y 100%. Funciona igual para KR que deben bajar (merma, ciclo) y para los que deben subir (entregas a tiempo).
- **Estado**: Cumplido ≥ 100% · En camino ≥ 70% · En riesgo ≥ 40% · Crítico < 40%.

## Los 9 KR

| KR | Objetivo | Resultado clave | Base → Meta |
|---|---|---|---|
| KR1 | O1 Corte y sostenibilidad | Merma de tela en mesa de corte | 7,5% → 2,2% |
| KR2 | O1 | Tiempo de ciclo por lote | 18 → 14,4 días |
| KR3 | O1 | Cumplimiento de lista de chequeo* | 60% → 90% |
| KR4 | O2 Cuellos de botella | Capacidad ociosa de la planta | 25% → 10% |
| KR5 | O2 | Piezas defectuosas por 100 prendas | 9,0 → 6,4 |
| KR6 | O2 | Traslados por urgencia por turno* | 40% → 20% |
| KR7 | O3 Logística y trazabilidad | Entregas a tiempo Bogotá–Paipa | 72% → 92% |
| KR8 | O3 | Órdenes visibles en el dashboard* | 0% → 100% |
| KR9 | O3 | Costo de fletes de emergencia (índice base 100)* | 100 → 80 |

\* Línea base **supuesta** (el documento no la indica). Confirmar con datos reales.

## Datos de ejemplo y almacenamiento

- Los valores actuales que trae el tablero son **de ejemplo**. Usa el botón **Poner en línea base** para empezar desde cero.
- Los valores se guardan en el **navegador del dispositivo** (`localStorage`). Cada persona ve sus propios números; no se comparten entre dispositivos.

## Publicar en GitHub Pages (sin instalar nada)

1. Entra a [github.com](https://github.com) e inicia sesión (o crea una cuenta gratis).
2. Toca **New repository**. Nombre sugerido: `tablero-okr-waldy`. Déjalo **Public** y crea el repositorio.
3. En el repositorio, toca **Add file → Upload files** y arrastra estos archivos: `index.html`, `README.md` y `.nojekyll`. Toca **Commit changes**.
4. Ve a **Settings → Pages**. En *Build and deployment*, elige **Source: Deploy from a branch**, **Branch: main** y carpeta **/ (root)**. Guarda.
5. Espera 1 o 2 minutos. El enlace para compartir será:

   `https://TU-USUARIO.github.io/tablero-okr-waldy/`

   (reemplaza `TU-USUARIO` por tu nombre de usuario de GitHub).

## Cambiar metas o KR

Abre `index.html` y busca la lista `const KR=[ ... ]`. Cada fila tiene este orden:

`[ID, objetivo (1-3), nombre, unidad, línea base, meta, valor inicial, paso del botón]`

Edita los números, guarda el archivo y vuelve a subirlo (en GitHub: abre el archivo, toca el lápiz, pega el cambio y *Commit changes*).

## Fuente

Metas y líneas base tomadas del documento de la Fase 5 (Pasos 3 y 5) de la propuesta de innovación. Para KR4 se usó la meta de 10% de la matriz de alineación (Paso 5).
