# Estadística y Ciencia de Datos

Trabajo práctico final de la materia **Introducción a la Estadística y Ciencia de Datos** de la **Universidad de Buenos Aires (UBA)**.

El proyecto estudia, mediante desarrollo teórico y simulaciones computacionales en R, distintos problemas de inferencia estadística asociados a tests diagnósticos imperfectos. Se analiza la estimación de una proporción poblacional, el comportamiento de estimadores, la construcción de intervalos de confianza y el nivel empírico de tests para comparar proporciones.

## Contenidos

El análisis implementado incluye:

- Simulaciones Monte Carlo para evaluar la cobertura de intervalos de confianza.
- Análisis de sensibilidad de la probabilidad observada frente a la sensibilidad, especificidad y prevalencia.
- Comparación del error cuadrático medio (ECM) entre estimadores en escenarios con tests perfectos e imperfectos.
- Evaluación del sesgo y la varianza del estimador de momentos.
- Bootstrap paramétrico y no paramétrico.
- Intervalos de confianza bootstrap por los métodos normal y percentil.
- Estudio de un estimador truncado en el intervalo `[0, 1]`.
- Simulación de tests para comparar proporciones entre mediciones pre y post.
- Evaluación del nivel empírico del test bajo distintos tamaños muestrales, incluidos escenarios desbalanceados.

## Tecnologías utilizadas

- **R**: lenguaje principal para el análisis estadístico y las simulaciones.
- **RStudio**: entorno recomendado para abrir y ejecutar el proyecto.
- **ggplot2**: generación de gráficos estadísticos.
- **latex2exp**: representación de expresiones matemáticas de LaTeX en gráficos.
- **patchwork**: combinación y composición de gráficos.
- **PDF**: el informe final se encuentra disponible en `TP_IECD.pdf`.

## Estructura del repositorio

```text
.
├── TP_IECD.pdf   # Informe final con el desarrollo del trabajo
├── tp.R          # Código de simulaciones, estimaciones y gráficos
├── tp.Rproj      # Proyecto de RStudio
├── .gitignore    # Archivos locales excluidos del control de versiones
└── README.md     # Documentación del proyecto
```

## Requisitos

Se recomienda contar con:

- R 4.x o una versión posterior compatible.
- RStudio (opcional, pero recomendado).
- Conexión a Internet únicamente para instalar las dependencias por primera vez.

## Instalación

1. Clonar el repositorio:

   ```bash
   git clone https://github.com/kissdelfina/estadistica-y-ciencias-de-datos.git
   cd estadistica-y-ciencias-de-datos
   ```

2. Instalar las dependencias de R:

   ```r
   install.packages(c("ggplot2", "latex2exp", "patchwork"))
   ```

3. Abrir `tp.Rproj` en RStudio o establecer el directorio del repositorio como directorio de trabajo.

## Ejecución

### Desde RStudio

1. Abrir el archivo `tp.Rproj`.
2. Abrir `tp.R`.
3. Ejecutar el script completo con **Source** o ejecutarlo por bloques para inspeccionar cada ejercicio.
4. Consultar la consola para ver las tablas y métricas calculadas, y la pestaña **Plots** para visualizar los gráficos.

### Desde la consola

Desde la carpeta raíz del repositorio, ejecutar:

```bash
Rscript tp.R
```

El script imprime en consola los resultados numéricos y genera los gráficos durante la ejecución. Para una visualización interactiva de los gráficos, se recomienda utilizar RStudio.

## Reproducibilidad

El script fija una semilla aleatoria mediante `set.seed(72)`, por lo que las simulaciones principales pueden reproducirse bajo la misma versión de R y de los paquetes instalados.

Los parámetros de referencia utilizados en el análisis incluyen:

- Prevalencia: `theta = 0.25`.
- Sensibilidad: `Se = 0.90`.
- Especificidad: `Sp = 0.95`.

Las simulaciones utilizan distintos tamaños muestrales y cantidades de réplicas según el ejercicio. En particular, los procedimientos bootstrap pueden requerir más tiempo de ejecución que los cálculos analíticos.

## Resultados

El informe completo, con el desarrollo matemático, las tablas y los gráficos obtenidos, está disponible en [`TP_IECD.pdf`](./TP_IECD.pdf).

## Licencia

Este repositorio se publica con fines académicos y educativos.
