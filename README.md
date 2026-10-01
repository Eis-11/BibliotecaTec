Control de Configuración y Control de Versiones

1. OBJETIVO DEL CONTROL DE LA CONFIGURACIÓN

El objetivo del control de la configuración del repositorio BibliotecaTec es establecer un conjunto de reglas y procedimientos para organizar, identificar, controlar, versionar y mantener los elementos de configuración del proyecto.

El control de configuración permitirá mantener un registro ordenado de los cambios realizados en los archivos, identificar las diferentes versiones de los elementos de configuración y facilitar el trabajo colaborativo entre los integrantes del equipo.

También permitirá conocer qué cambios se realizaron, quién los realizó y en qué momento fueron incorporados al repositorio, evitando la pérdida de información y manteniendo una estructura organizada.


2. ESTRUCTURA DEL REPOSITORIO

El repositorio se denomina BibliotecaTec y contiene una estructura organizada para almacenar los diferentes elementos de configuración del proyecto.
Estructura propuesta

text
BibliotecaTec/
│
├── README.md
│
├── Código/
│   └── en esta carpeta va todo lo que tiene código como por ejemplo que tiene .HTML, .py, .cs y etc. 
│
├── Documentación/
│   └── en esta carpeta va todos los archivos que sean .pdf, .xlsx, .docx. 
│
└── Imágenes/
    └── en esta carpeta van todas las imágenes que terminen en .png, .jpg, .jpeg. 


3. ESTÁNDAR DE USO DEL REPOSITORIO

3.1 Reglas de nombres

Formato: `BT_Tipo_Descripcion_vX.Y.Z.extension`

**BT**: proyecto (BibliotecaTec)
**Tipo**: `COD` (código), `DOC` (documentos), `IMG` (imágenes)
**Descripcion**: palabras juntas, cada una con mayúscula inicial
**vX.Y.Z**: versión del archivo

| Nemónico | Tipo de elemento | Carpeta |
|---|---|---|
| `COD` | Código fuente (`.html`, `.py`, `.cs`) | Código/ |
| `DOC` | Documentos (`.pdf`, `.docx`, `.xlsx`) | Documentación/ |
| `IMG` | Imágenes (`.png`, `.jpg`, `.jpeg`) | Imágenes/ |

Reglas:

Sin espacios, acentos ni caracteres especiales.
Separar las partes del nombre con guion bajo (`_`).

Ejemplos:

`BT_COD_AbrePaginaWeb_v1.0.0.py`
`BT_DOC_PlanDePruebas_v1.0.0.pdf`
`BT_IMG_DiagramaClasesUML_v1.0.0.jpg`

3.2 Reglas de versiones

Se usa [Versionado Semántico 2.0.0](https://semver.org/lang/es/) con el formato **MAYOR.MENOR.PARCHE**:

| Número | Cuándo se incrementa | Ejemplo |
|---|---|---|
| **MAYOR** | Cambio grande en el elemento | 1.0.0 → 2.0.0 |
| **MENOR** | Se agrega algo nuevo | 1.0.0 → 1.1.0 |
| **PARCHE** | Corrección pequeña | 1.1.0 → 1.1.1 |

Reglas:

La primera versión de cada archivo es `v1.0.0`.
Al subir MAYOR, MENOR y PARCHE vuelven a 0; al subir MENOR, PARCHE vuelve a 0.
Los números de versión no se reutilizan ni se reducen.

Ejemplo con `HolaMundo`:

`BT_COD_HolaMundo_v1.0.0.html` (primera versión)
`BT_COD_HolaMundo_v1.1.0.html` (segunda versión)
`BT_COD_HolaMundo_v1.1.1.html` (segunda versión corregida)

3.3 Reglas para comentar COMMITS

Formato: `tipo: descripción breve`

| Tipo | Uso |
|---|---|
| `feat` | Se agrega un archivo nuevo |
| `fix` | Se corrige un error |
| `docs` | Cambios en documentación |

Reglas:

Escribir en español, en verbo imperativo (agrega, corrige).
Máximo 50 caracteres, sin punto final.
Incluir el nombre y versión del archivo.

Ejemplos:

```text
feat: agrega BT_COD_HolaMundo_v1.0.0.html
feat: agrega BT_COD_HolaMundo_v1.1.0.html
fix: corrige BT_COD_HolaMundo_v1.1.1.html
docs: agrega BT_DOC_PlanDePruebas_v1.0.0.pdf
feat: agrega BT_IMG_DiagramaClasesUML_v1.0.0.jpg
```



