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

- Se agrega un fichero de ejemplo
  - `content/sample_data/AZ-104T00A-ES-PowerPoint_01.pptx`
- Genera un fichero de salida llamado
  - `content/sample_data/AZ-104T00A-ES-PowerPoint_01.md`

### Ejemplo de salida por consola

```md
# AZ-104T00A Administración de identidades

## AZ-104T00A Administración de identidades

- AZ-104T00A Administración de identidades
## Introducción a la administración de identidades

- Introducción a la administración de identidades
## Configurar Azure Active Directory

- Configurar Azure Active Directory
## Introducción a la configuración de Azure Active Directory

- Introducción a la configuración de Azure Active Directory
- Descripción de las ventajas y características deAzure Active Directory
- Descripción de los conceptos de Azure AD
- Comparación de AD DS con Azure Active Directory
- Ediciones de Azure AD
- Implementación de identidades de dispositivo de Azure AD
- Implementación de autoservicio de restablecimientode contraseña
- Resumen y recursos
## Descripción de las ventajas y características de Azure Active Directory

- Descripción de las ventajas y características de Azure Active Directory
- Un conjunto de funcionalidades de administración de identidades basado en la nube que le permite administrar de forma segura el acceso a los servicios y recursos de Azure para los usuarios
- Proporciona administración deaplicaciones, autenticación, administración de dispositivos e identidad híbrida
## Descripción de los conceptos de Azure AD

- Descripción de los conceptos de Azure AD
## Comparación de AD DS con Azure Active Directory

- Comparación de AD DS con Azure Active Directory
- Azure AD es principalmente una solución de identidad y está diseñado para comunicaciones HTTP y HTTPS
- Se consulta mediante la API REST sobre HTTP y HTTPS. En lugar de LDAP
- usa los protocolos HTTP y HTTPS, como SAML, WS-Federation y OpenID Connect para la autenticación, así como OAuth para la autorización. En lugar de Kerberos,
- incluye servicios de federación y muchos servicios de terceros (como Facebook)
- Los usuarios y grupos de Azure AD se crean en una estructura plana y no hay unidades organizativas (UO) ni objetos de directiva de grupo (GPO)
## Selección de ediciones de Azure Active Directory

- Selección de ediciones de Azure Active Directory
## Configuración de identidades de dispositivo de Azure AD

- Configuración de identidades de dispositivo de Azure AD
## Implementación de autoservicio de restablecimiento de contraseña

- Implementación de autoservicio de restablecimiento de contraseña
- Determine quién puede usar el autoservicio de restablecimiento de contraseña
- Elija el número de métodos de autenticación necesarios y los métodos disponibles (correo electrónico, teléfono, preguntas)
- Puede exigir que los usuarios se registren en SSPR (el mismo proceso que MFA)
## Resumen y recursos: Configuración de Azure Active Directory

- Resumen y recursos: Configuración de Azure Active Directory
- Prueba de conocimientos
- Módulos de Microsoft Learn (docs.microsoft.com/Learn)
- Uso del autoservicio de restablecimiento de contraseña de Azure Active Directory para permitir a los usuarios restablecer sus contraseñas (espacio aislado)
- Administración de la identidad del dispositivo con Unión a Azure AD y Enterprise State Roaming
- Implementación y administración de una identidad híbrida
- Un espacio aislado indica un ejercicio práctico.
## Configuración de cuentas de usuario y de grupo

- Configuración de cuentas de usuario y de grupo
## Introducción a la configuración de cuentas de usuario y de grupo

- Introducción a la configuración de cuentas de usuario y de grupo
- Creación de cuentas de usuario
- Administrar cuentas de usuario
- Creación de cuentas masivas
- Creación de cuentas de grupo
- Asignación de licencias a usuarios y grupos (tema adicional)
- Creación de unidades administrativas
- Demostración: Usuarios y grupos
- Resumen y recursos
## Creación de cuentas de usuario

- Creación de cuentas de usuario
- Todos los usuarios debentener una cuenta
- La cuenta se usa para la autenticación y la autorización.
- Cada cuenta de usuario tiene propiedades adicionales
## Administrar cuentas de usuario

- Administrar cuentas de usuario
- Debe ser administrador global o administrador de usuarios para administrar usuarios
- El perfil de usuario(imagen, trabajo e información de contacto) es opcional
- Los usuarioseliminados se pueden restaurardurante 30 días
- La informacióndel registro de inicio de sesión y auditoríaestá disponible
## Realización de actualizaciones masivas de cuentas

- Realización de actualizaciones masivas de cuentas
- Azure AD admite actualizaciones masivas de usuarios y miembros de grupos
- Cree la plantilla de valores separados por comas (CSV) que puede descargar desde el portal
- Debe haber iniciado sesión como administrador global o administrador de usuarios
## Creación de cuentas de grupo

- Creación de cuentas de grupo
- Tipos de grupo
- Grupos de seguridad
- Grupos de Microsoft 365
- Tipos de asignación
- Asignada
- Usuario dinámico
- Dispositivo dinámico (solo grupos de seguridad)
## Asignación de licencias a usuarios y grupos

- Asignación de licencias a usuarios y grupos
- Servicios adicionales (como O365 son servicios en la nube de pago)
- Los servicios en la nube de pago de Microsoft requieren licencias.
- Las licencias se asignan a los usuarios que necesitan acceso a los servicios.
- Cada usuario o grupo requiere una licencia de pago independiente.
- Los administradores usan portales de administración y cmdlets de PowerShell para administrar licencias.
- Microsoft Azure es un servicio en la nube que proporciona muchos servicios integrados de forma gratuita.
- Azure AD se incluye como un servicio gratuito.
- Obtención de funcionalidad adicional de Azure AD con una licencia P1 o P2
- Consulta de los planes de licencia y sus detalles
- Establecimiento del parámetro Ubicación de uso
- Asignación de licencias a usuarios y grupos
- Cambio de planes de licencia para usuarios y grupos
- Eliminación de una licencia
## Creación de unidades administrativas

- Creación de unidades administrativas
- Creación de una unidad administrativa
- Rellene la unidad administrativa con usuarios o grupos de Azure AD
- Cree un rol con los permisos adecuados en el ámbito de la unidad administrativa
- Agregue miembros de TI al grupo
- Azure AD Premium P1 o P2 para cada administrador de roles con privilegios o administrador global
## Demostración: Usuarios y grupos

- Demostración: Usuarios y grupos
- Determinación de la información de dominio
- Exploración de cuentas de usuario
- Exploración de cuentas de grupo
- Exploración de PowerShell para la administración de grupos
## Resumen y recursos: Configuración de cuentas de usuario y de grupo

- Resumen y recursos: Configuración de cuentas de usuario y de grupo
- Prueba de conocimientos
- Módulos de Microsoft Learn (docs.microsoft.com/Learn)
- Creación de usuarios y grupos de Azure en Azure Active Directory (espacio aislado)
- Administración de usuarios y grupos en Azure Active Directory
- Un espacio aislado indica un ejercicio práctico.
## Laboratorio 01: Administración de identidades de Azure Active Directory

- Laboratorio 01: Administración de identidades de Azure Active Directory
## Laboratorio 01: Administración de identidades de Azure Active Directory

- Laboratorio 01: Administración de identidades de Azure Active Directory
- Escenario del laboratorio
- Para permitir que los usuarios de Contoso se autentiquen mediante Azure AD, se le ha encargado el aprovisionamiento de usuarios y cuentas de grupo.La pertenencia a los grupos debe actualizarse automáticamente en función de los puestos de trabajo del usuario.También debe crear un inquilino de prueba de Azure AD con una cuenta de usuario de prueba y conceder permisos limitados a esa cuenta para los recursos de la suscripción de Azure de Contoso.
- Objetivos
- Tarea 1: Creación y configuración de usuarios de Azure AD
- Tarea 2: Creación de grupos de Azure AD con pertenencia asignada y dinámica
- Tarea 3: Creación de un inquilino de Azure Active Directory (AD)
- Tarea 4: Administración de usuarios invitados de Azure AD
- Diagrama de la arquitectura en la siguiente diapositiva
## Laboratorio 01: Diagrama de la arquitectura

- Laboratorio 01: Diagrama de la arquitectura
## Fin de la presentación

- Fin de la presentación
```
