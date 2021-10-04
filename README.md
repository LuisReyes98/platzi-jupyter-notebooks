# Clases del Curso de Entorno de Trabajo para Ciencia de Datos con Jupyter Notebooks y Anaconda

## ¿En qué lugares programar para ciencia de datos?

**Existen muchas plataformas para trabajar en Data Science**, se recomiendo usar algún Sistema Operativo basado en UNIX usando Linux, MacOS o WSL en Windows, en editores estan VSCode, PyCharm, Deepnote, Google Colab, y el que usaremos Jupyter, todo basado en Notebooks que te permiten ir ejecutando trozos de código, en el cual puedes escribir pocas lineas de código probarlas, asegurarse de que estén bien y seguir adelante con otro trozo, allí también se pueden añadir código, ecuaciones, gráficas, texto enriquecido, etc.

**IPython**
Creado por Fernando Perez (Fisico Colombiano)
IPython es una herramienta que mejora el REPL (Read, Evaluate, Print, Loop) por defecto de python.

**Notebooks Vs Scripts**
Ambos son útiles, aunque los Scripts son mas directos, los Notebooks te permiten ver lo que haces, a medida de que lo haces, en estos puedes encargarte de experimentar y hacer el prototipado de tu script y finalmente pasarlo a un Script cuando ya este listo y estés seguro de que todo funciona como es esperado

**En un Scripts** podras ver lo que hizo el programador sin interrupciones

**Notebooks**
Los notebooks son mas interactivos y como un reporte en vivo en el cual puedes ver cual fue el proceso creativo y analitico que se hizo para llegar a los resultados.

## Google Colab: primeros pasos

Es un sistema basado en notebooks y estos se almacenan en tu google drive

### Notebooks en la nube vs en local

- ambos son utiles
- Configuracion de entorno (en la nube ya esta todo listo en local se debe configurar)
- Tiempos de ejecución
- Escalabilidad (en proyectos grandes con un dataset mas grande que la capacidad de mi computadora)

### Google Colab

- Servicio en la nube
- Basado en Jupyter Notebooks
- No requiere configuración
- Trabajo a nivel de archivo

- Uso gratiuto de GPUs y TPUs

## Utilizar Deepnote

- Servicio en la nube
- Basado en Jupyter Notebooks
- No requiere configuración
- Trabaja a nivel de **proyecto**

Poseé

- Colaboracion en tiempo real
- Integracion con multiples apps
- Acceso a una terminal o linea de comandos

- Almacenamiento de variables de entorno
- Publicar proyectos (construir portafolio)

Interfaz muy bonita y limpia de visualizacion de archivos subidos

Deep note extendio los tipos de bloques disponibles originalmente solo markdown o codigo, en deepnote deja agregar celdas de graficas y de visualizacion del resultado de sentencias SQL a un dataframe

**Ver comandos disponibles:** CTRL + P

Además Deepnote permite compartir proyectos mediante un link o publicar el notebook en un formato de Dashboard o Articulo.

## Instalar VSCode

## Agregar extensiones para VSCode

## Uso de VSCode notebooks

## ¿Qué son los ambientes virtuales?

Los ambientes virtuales son entornos de trabajos aislados del resto en la computadora para poder trabajar en multiples proyectos sin que exista conflictos en las dependencias del proyecto.

Dependiendo del lenguaje de programación existen diferentes herramientas para lograr esto.

En python existen herramientas como:

- .venv
- Pipenv
- conda

## Instalar Conda a través de la terminal

[Anaconda individual edition](https://www.anaconda.com/products/individual)

## Conda: crear y actualizar ambientes

```sh
$ conda create --name [nombre] [paquete]=[versión]
```

Si no hay se especifíca una versión, se instalará la última disponible.

Para ver los paquetes(si no se especifican los paquetes, dará una lista de los ambientes virtuales):

```sh
$ conda list [paquete]
```

Para activar y desactivar los ambientes:

```sh
$ conda activate [nombre del ambiente] y $ conda deactivate
```

Para actualizar paquetes:

```sh
$ conda update [paquete]
```

Para instalar un paquete específico:

```sh
$ conda install [paquete]=[versión]
```

Para clonar un ambiente:

```sh
$ conda --name [nuevo ambiente] --copy --clone [ambiente]
```

## Conda: abrir VSCode Notebooks con tu ambiente creado

## Conda: eliminar ambientes y librerías

Notas:
Para desinstalar un paquete:

```sh
$ conda remove [paquete]
```

Para eliminar un ambiente (el ambiente debe estar desactivado):

```sh
$ conda env remove --name [nombre de un ambiente]
```

## Conda: comandos avanzados

```sh

#Crear ambiente
conda create --name py39 python=3.9 pandas=1.2

#Ir al ambiente
conda activate py39

# Instalar boltons
conda install -c conda-forge boltons
# conda-forge es un canal de conda de las librerias

#Devolver a un punto anterio y asi no tener que remover
conda list -r

#Devolverme a larevision 0
conda install --revision 0
# Conda almacena cada uno de sus estados anterios al instalar una dependencias, estos estados se llaman revision, perminiendo asi volver a una revision anterior, con un registro de las "migraciones" del ambiente.

#Revisar si esta instalado
conda list boltons

#Exportar tu ambiente
conda env export

#Exportar tu ambiente pero sin las versiones
conda env export --no-builds

#Exportar tu ambiente LA MEJOR
conda env export --from-history

#Exportar tu ambiente a un archivo
conda env export --from-history --file environment.yam

#Remover ambiente
conda env remove --name py39

#Importar el ambiente desde un archivo
conda env create --file environment.yaml

#Ir al ambiente
conda activate py39
```
