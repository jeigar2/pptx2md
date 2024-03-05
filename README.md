# Presentacione PPTX 2 Markdown

- Función que toma un directorio y lee todos los ficheros pptx que tiene.
  - Crea un fichero md con el mismo nombre que el fichero pptx
  - Crea un Titulo con el slide 1
  - Crea un subtitulo con cada nuevo slide
  - El resto de textos los pone con bullet

  - Muestra por consola todo el texto compuesto

## Dependencias

- Para que compile hay que instalar la libreria pptx

```sh
pip install python-pptx
```

```log
Collecting python-pptx
  Downloading python_pptx-0.6.23-py3-none-any.whl (471 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 471.6/471.6 kB 5.4 MB/s eta 0:00:00
Requirement already satisfied: lxml>=3.1.0 in /usr/local/lib/python3.10/dist-packages (from python-pptx) (4.9.4)
Requirement already satisfied: Pillow>=3.3.2 in /usr/local/lib/python3.10/dist-packages (from python-pptx) (9.4.0)
Collecting XlsxWriter>=0.5.7 (from python-pptx)
  Downloading XlsxWriter-3.2.0-py3-none-any.whl (159 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 159.9/159.9 kB 7.2 MB/s eta 0:00:00
Installing collected packages: XlsxWriter, python-pptx
Successfully installed XlsxWriter-3.2.0 python-pptx-0.6.23
```

## Google colab

Para que funcione hay que subir unos ficheros pptx en google colab en la siguiente ruta

```sh
/content/sample_data
```

Ejecución del método

```py
# Directorio que contiene los archivos .pptx
pptx_directory = "/content/sample_data"
convert_pptx_to_md(pptx_directory)
```

### Ejemplo de salida por consola

```md
# AZ-104

## AZ-104T00A - Administración de la protección de datos

- AZ-104T00A - Administración de la protección de datos

### Introducción a la administración de la protección de redes

- Introducción a la administración de la protección de redes
- Configuración de copias de seguridad  - de archivos y carpetas
- Configuración de copias de seguridad  - de máquinas virtuales
- Laboratorio 10: Implementación de la protección de datos

### Configuración de copias de seguridad de archivos y carpetas

- Configuración de copias de seguridad de archivos y carpetas

### Introducción a la configuración de copias de seguridad de archivos y carpetas

- Introducción a la configuración de copias de seguridad de archivos y carpetas
- Descripción de las ventajas de Azure Backup
- Implementación del Centro de copias de seguridad de Azure
- Configuración de las opciones de copia de seguridad del almacén de Recovery Services
- Demostración: Copia de seguridad de recursos compartidos de archivos de Azure
- Configuración de copias de seguridad de archivos y carpetas locales
- Administración del agente de Microsoft Azure Recovery Services
- Demostración: Copia de seguridad de archivos y carpetas
- Resumen y recursos

### Descripción de las ventajas de Azure Backup

- Descripción de las ventajas de Azure Backup
- Servicio de Azure que se usa para realizar copias de seguridad y restaurar los datos en la nube de Microsoft
- Administración automática del almacenamiento
- Varias opciones de almacenamiento
- Transferencia de datos ilimitada
- Cifrado de datos
- Copia de seguridad coherente con la aplicación
- Retención a largo plazo

### Implementación del Centro de copias de seguridad de Azure

- Implementación del Centro de copias de seguridad de Azure
- Panel único para administrar copias de seguridad en un entorno de Azure grande  - y distribuido
- Administración centrada en orígenes de datos con la atención en el contenido del que se está realizando una copia de seguridad
- Experiencias conectadas con integraciones nativas que permiten la administración  - a escala

### Configuración de las opciones de copia de seguridad del almacén de Recovery Services - Archivos

- Configuración de las opciones de copia de seguridad del almacén de Recovery Services - Archivos
- Cargas de trabajo de Azure
- Cargas de trabajo locales

### Demostración: Copia de seguridad de recursos compartidos de archivos de Azure

- Demostración: Copia de seguridad de recursos compartidos de archivos de Azure
- Configuración de una cuenta de almacenamiento con un recurso compartido de archivos
- Creación de un almacén de Recovery Services
- Configuración de la copia de seguridad de un recurso compartido de archivos
- Comprobación de la copia de seguridad del recurso compartido de archivos

### Configuración de copias de seguridad de archivos y carpetas locales

- Configuración de copias de seguridad de archivos y carpetas locales
- Creación del almacén de Recovery Services
- Descarga del agente y el archivo de credenciales
- Instalación y registro del agente
- Configuración de la copia de seguridad

### Administración del agente de Microsoft Azure Recovery Services

- Administración del agente de Microsoft Azure Recovery Services
- Copia de seguridad de archivos y carpetas en el sistema operativo Windows físico o virtual (las máquinas virtuales pueden estar en el entorno local o en Azure)
- No se necesita ningún servidor de copia de seguridad independiente
- No es compatible con la aplicación; restauración solo a nivel de archivo, carpeta y volumen
- No es compatible con Linux

### Demostración: Copia de seguridad de archivos y carpetas

- Demostración: Copia de seguridad de archivos y carpetas
- Creación de un almacén de  - Recovery Services
- Configuración del almacén
- Instalación y registro del agente
- Creación de la directiva de copia de seguridad
- Realizar copias de seguridad de archivos y carpetas
- Exploración de la configuración de recuperación
- Exploración de las propiedades de copia de seguridad
- Eliminación de la programación de copias de seguridad

### Resumen y recursos: configuración de copias de seguridad de archivos y carpetas

- Resumen y recursos: configuración de copias de seguridad de archivos y carpetas
- Preguntas de la prueba de conocimientos
- Módulos de Microsoft Learn (docs.microsoft.com/Learn)
- Introducción a Azure Backup

### Configuración de copias de seguridad de máquinas virtuales

- Configuración de copias de seguridad de máquinas virtuales

### Introducción  - a la configuración de las copias de seguridad de máquinas virtuales

- Introducción  - a la configuración de las copias de seguridad de máquinas virtuales
- Protección de los datos de la máquina virtual
- ​Creación de instantáneas de máquina virtual
- Configuración de las opciones de copia de seguridad del almacén de Recovery Services
- Copia de seguridad de máquinas virtuales
- Restauración de máquinas virtuales
- Demostración: Copias de seguridad de máquinas virtuales
- Implementación de Azure Backup Server
- Comparación de las opciones de copia de seguridad
- Administración de la eliminación temporal
- Implementación de Azure Site Recovery
- Resumen y recursos

### Protección de los datos de la máquina virtual

- Protección de los datos de la máquina virtual
- Instantáneas
- Azure Backup
- Azure Site Recovery
- Las instantáneas administradas proporcionan una opción rápida y sencilla para hacer copias de seguridad de máquinas virtuales que usan  - Managed Disks.
- Azure Backup admite las copias de seguridad coherentes con la aplicación para máquinas virtuales Windows y Linux.
- Azure Site Recovery permite proteger las máquinas virtuales en un escenario grave de desastre en el que toda una región experimenta una interrupción.
```
