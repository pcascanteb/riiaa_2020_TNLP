# ¡Atención! El auge de los Transformadores - RIIAA '20

Este repositorio de github contiene material el workshop sobre **Transformadores** y **Self-Attention** presentado en [RIIAA '20](https://riiaa.org/).

**TL;DR**: vamos a trabajar con [Google Colab](https://colab.research.google.com/). Da click en los links de abajo para abrir un notebook, y haz una copia para empezar a trabajar en ellos.
* [1) Mecanismos de Atencion](https://colab.research.google.com/drive/1rL75HO8-jyK-ZfeE5_xJjh2WT9d_xzEt?usp=sharing)
* [2) Transformadores y clasificacion de texto](https://colab.research.google.com/drive/1lH8XCs7GIkNW7i_qvFPILxaImwkq2WeW?usp=sharing)

<br>
<hr>

## Organización del repositorio

La estructura está inspirado en una versión lite de [cookie cutter data science project](https://drivendata.github.io/cookiecutter-data-science/):

* **data/**: folder de datos para tu taller. Es recomendable enfocarse en un dataset o dos durante el workshop (vs varios), asi los talleristas podrán profundizar en aspectos específico de los datos y después enfocar su atención a la parte algorítmica/teoria del taller.
* **code/**: funciones de utilidad para usar en los notebooks.
* **notebook/**: jupyter notebooks que se pueden lanzar en colab. Enumera los notebook en orden de uso.
* **media/**: imagenes para usar en tus notebooks y repo.
* **environment.yml**: archivos anaconda para replicar el software stack localmente.
* **README.md**: archivo markdown de entrada para la pagina y tu taller.

## Mejoras? sugerencias?
Manda un [pull request](https://help.github.com/en/articles/about-pull-requests)!

## Instrucciones para estudiantes

Este taller esta desarrollado en Python 3.7+ usando la biblioteca [Pytorch](https://pytorch.org/) como interfaz de alto nivel para construir y entrenar redes neuronales.

Cosas para preparar
* Una laptop.
* Tener acceso a [Google Colab](https://colab.research.google.com/)
* Opcional:
    * Este repositorio de GitHub clonado y actualizado antes del taller.
    * Un ambiente Python 3.7+ con Anaconda (ver opciones 1 y 2 abajo).

Los talleres serán impartidos usando *notebooks* de Jupyter, documentos con código ejecutable, texto, ecuaciones, visualizaciones, imágenes y demás material. Los *notebooks* se pueden crear y ejecutar en la nube vía Google Colab (opción 1) o de manera local en tu computadora a través de [Jupyter Notebooks](https://jupyter.org/) (opción 2).

### Opcion 1: Google Colab
[Colab](https://colab.research.google.com) es un servicio de Google para ejecutar *notebooks* en la nube. Provee ambientes de Python 2 y 3 con CPUs, GPUs y TPUs. ¡Y es gratis! Solo necesitas tener una cuenta de Google o crear una.

Recomendamos que elijas un ambiente con Python 3 y GPU. Para activarlo:
* Abre el menú `Entorno de ejecución`
* Elige la opción `Restablecer todos los entornos de ejecución...` .
* Vuelve a abrir `Entorno de ejecución`
* Elige `Cambiar tipo de entorno de ejecución`
* Selecciona Python 3 como `Tipo de ejecución` y GPU de la lista de `Acelerador por hardware`

La siguiente captura de pantalla ilustra este proceso.

![](media/escoge_acelerador.png)

En [Colab](https://colab.research.google.com) puedes crear un nuevo *notebook*, subir uno existente desde tu computadora o importarlo de Google Drive o GitHub.

### Opcion 2: Ambiente local
Para tener la versión de Python 3.7+ y todas las bibliotecas instaladas en cualquier plataforma, recomendamos que uses [**Anaconda**](https://www.anaconda.com/) y generes un ambiente con el archivo `environment.yml` de este repositorio usando una terminal y el comando:

```
conda env create -n riiaa20 -f environment_cpu.yml
```

Cambia el nombre `riia20` por tu nombre favorito para el ambiente. Si cuentas con un GPU Nvidia y deseas aprovecharlo cambia el archivo `environment_cpu.yml` a `environment_gpu.yml`.

Para activar el ambiente que creaste, en una terminal ingresa el comando

```
conda activate riiaa20
```

Una vez activado, puedes ejecutar la aplicación de Jupyter Notebook

```
jupyter notebook
```

Este comando abrirá una pestaña o ventana en tu navegador web, como se muestra en la siguiente captura de pantalla:

![](media/jupyter_notebook.png)

Al igual que en Google Colab, puedes crear un nuevo *notebook* seleccionando el botón `New` y posteriormente `Python 3`. De forma alternativa, puedes abrir uno existente seleccionando el archivo del *notebook* (con extensión `.ipynb`) dentro del directorio donde ejecutaste Jupyter Notebook. Con el botón `Upload` agregas archivos que se encuentran en otra parte de tu computadora a este directorio. Para cerrar Jupyter Notebook, presiona el botón `Quit` y posteriormente cierra la pestaña o ventana de tu navegador web.

Para desactivar el ambiente `riiaa20` de Anaconda simplemente haz

```
conda deactivate
```
