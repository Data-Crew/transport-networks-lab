# SKILL: Generar script de fiscalización con route-optimizer

Genera un script Python que resuelva un problema de fiscalización de
estacionamiento medido usando la API pública de route-optimizer.

Repositorio de referencia (clonar si no está disponible localmente):
https://github.com/Data-Crew/route-optimizer

Referencia obligatoria dentro de ese repo: parking_enforcement.py — replicá
su mismo flujo (Zone → RouteOptimizer → download_street_network →
label_zones → solve_cpp/solve_tsp → exportar → visualizar). Las firmas de
`Zone`, `RouteOptimizer` y sus métodos están definidas en `route_optimizer.py`,
en la raíz de ese mismo repo — no las inventes ni las asumas: leelas del
código real antes de escribir el script.

Restricciones:
- No modifiques route_optimizer.py ni los solvers.
- Usá únicamente la API pública tal como se usa en el ejemplo de referencia.

El script debe, en este orden:
1. Definir la(s) zona(s) según el SPEC (nombre, polígono lon/lat, horario).
2. Descargar la red de calles según el bbox del SPEC.
3. Etiquetar zonas y calcular la ruta con el algoritmo indicado en el SPEC.
4. Exportar resultados a Excel, generar visualización estática (.png) e
   interactiva (.html), con los nombres de archivo indicados en el SPEC.
5. Imprimir: cantidad de nodos, cantidad de ejes, distancia total en km.

## Evaluación de resultados (obligatoria, varía según el SPEC)

- Si `entorno_ejecucion: colab` → generá un archivo `.md` con la secuencia
  exacta de celdas de Colab, en este formato:

  **CELDA 1**
  ```notebook-python
  !git clone <url-del-repo>
  ```

  **CELDA 2**
  ```notebook-python
  %cd <nombre-del-repo>
  ```

  **CELDA 3**
  ```notebook-python
  !pip install -r requirements.txt
  ```

  **CELDA 4**
  ```notebook-python
  !mkdir -p <directorio-de-archivo_destino> output
  ```

  **CELDA 5**
  ```notebook-python
  %%writefile <archivo_destino>
  <CONTENIDO COMPLETO del script generado en el paso anterior>
  ```

  **CELDA 6**
  ```notebook-python
  !python <archivo_destino>
  ```

  Reglas:
  - Fence siempre `notebook-python`, nunca `python`: `!`, `%cd` y
    `%%writefile` son magics de IPython, no sintaxis Python válida.
  - Cada celda lleva su etiqueta en negrita `**CELDA N**` (no un heading
    `#`, que se ve gigante y rompe la legibilidad del documento).
  - CELDA 5 contiene el script completo tal cual quedó en `archivo_destino`
    — nunca un resumen ni una referencia al archivo.
  - No agregar celdas markdown, comentarios de transición ni texto
    explicativo entre celdas.
- Si `entorno_ejecucion: cursor` (o cualquier editor con terminal, sobre el
  repo `route-optimizer` clonado en el `root`) → NO uses `pip install`
  suelto ni comandos de venv: el repo ya tiene un flujo Docker vía
  `Makefile`/`docker-compose.yml` que monta el código y persiste
  `output/` fuera del contenedor. La instrucción debe ser, en este orden:
  1. `make build` (una sola vez, si la imagen no existe todavía).
  2. `make shell` — abre una bash dentro del contenedor, en el `root` del
     repo, con todas las dependencias ya instaladas.
  3. Dentro de esa shell: `python <archivo_destino>` — ejecuta el script
     de fiscalización generado.
  4. Salir del contenedor (`exit`) y revisar los resultados en
     `output/` (excel, .png, .html), que persisten en el host porque
     `docker-compose.yml` monta `./output:/app/output`.
  No generar comandos alternativos (venv, pip global, etc.) salvo que el
  SPEC lo pida explícitamente.
