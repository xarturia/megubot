[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![GNU License][license-shield]][license-url]




<!-- LOGO -->
<br />
<p align="center">
  <a href="https://github.com/xarturia/megubot">
    <img src="images/megupfp.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Megubot | Telegram management bot</h3>


<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Tabla de Contenido</summary>
  <ol>
    <li>
      <a href="#acerca-del-proyecto">Acerca del Proyecto</a>
      <ul>
        <li><a href="#megu-fue-hecha-con">Built</a></li>
      </ul>
    </li>
    <li>
      <a href="#Antes-de-continuar-lee-atentamente">Antes de continuar lea antentamente</a>
      <ul>
        <li><a href="#Instalación">Instalación</a></li>
        <li><a href="#Prerrequisitos">Prerrequisitos</a></li>
      </ul>
    </li>
    <li><a href="#Configuración">Configuración</a></li>
    <li><a href="#Contribuciones">Contribuciones</a></li>
    <li><a href="#license">License</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## Acerca del proyecto

[![Product Name Screen Shot][product-screenshot]](https://xarturia.github.io/megubot/)

Megu es un bot de Telegram modular, con temática anime, basado en python y con base de datos sqlalchemy.
El principal objetivo de nuestro proyecto es que puedas administrar tus grupos con la mayor eficacia, eficiencia y facilidad, por ello Megu cuenta con muchas funciones, no sólo administrativas, sinó también divertidas!

Aquí el por qué:
* Respuestas personalizadas y triggers.
* Federaciones, global ban, blacklists.
* Crea tus propias reglas, busca stickers, información sobre animes/manga. ¿Quieres también tirar los dados? Adelante!

Megu goza también de un código robusto y en constante mantenimiento, puesto al día con las últimas novedades de Telegram.

### Megu fue hecha con:

* [Python](https://www.python.org)
* [SQLAlchemy](https://www.sqlalchemy.org)
* [Pyrogram](https://docs.pyrogram.org)
* [Telethon](https://docs.telethon.dev/en/)
* [python-telegram-bot](https://github.com/python-telegram-bot/python-telegram-bot)



### Antes de continuar lee atentamente
* OpenSource:
Tu código debe ser OpenSource y mencionar/contener el link desde donde has hecho el fork.
* License:
Incumplir con la norma anteriormente mencionada es estar violando la licencia de código abierto, usted será Gbaneado de la red de grupos sin previo aviso y se le añadirá a la lista negra de SpamWatch.
Asegúrate de leer el archivo   ```LICENSE``` para más información.
* Scam:
Está absolutamente prohibida la venta y así también la distribución de éste código sin las atribuciones correspondientes.
* Support:
Si ha decidido hacer un fork por su cuenta, nosotros no brindamos ningún tipo soporte/ayuda técnica para el mismo, sólo para MeguBot. Ante cualquier problema, asegúrate de leer el repositorio.
* Spamming (megu): 
Evita usar a Megu para difundir mensajes spam, enlaces a sitios externos poco confiables/pornográficos. Puedes ser reportado y Gbaneado de la red de grupos.

## Instalación

### Heroku
* Complete todos los detalles y variables requeridas (Puedes omitir las opcionales) ?¡Deploy!
* Ahora vaya a https://dashboard.heroku.com/apps/(app-name)/resources (Reemplace (app-name) con el nombre de su aplicación)
* Activa el Dyno de tu worker (no te preocupes, es gratis :D) y Webhook.
* Ahora envía /start dentro del chat con tu bot. Si no responde, vaya a ```https://dashboard.heroku.com/apps/(app-name)/settings``` y elimine el ```webhook``` y el ```puerto```.

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/NachABR/MeguRobot.git)

### Prerrequisitos

¡Asegúrese de usar ```python 3.6```, ya que no puedo garantizar que todo funcione como se esperaba en versiones anteriores de Python! Esto se debe a que el análisis de markdown se realiza iterando a través de un dictado, que está ordenado por defecto en 3.6.
#### Windows
* [Python](https://www.python.org/downloads/)

#### Linux
Para ver que versión de Python 3 tienes instalada, abre una terminal y ejecuta
* python3

  ``` $ python3 --version ```
 
 Si estás usando Ubuntu 16.10 o uno más nuevo, entonces puedes fácilmente instalar Python 3.6 con los siguientes comandos:
 ```
 $ sudo apt-get update
 $ sudo apt-get install python3.6
 ```
 
## Configuración

Hay dos formas posibles de configurar su bot: un archivo config.py o variables ENV.

La versión preferida es usar un archivo `config.py`, ya que facilita ver todas las configuraciones agrupadas.
Este archivo debe colocarse en su carpeta `MeguRobot`, junto con el archivo `__main__.py`.
Aquí es donde se cargará su token de bot, así como el URI de su base de datos (si está usando una base de datos), y la mayoría de
sus otras configuraciones.

Se recomienda importar sample_config y extender la clase Config, ya que esto asegurará que su configuración contenga todos
valores predeterminados establecidos en sample_config, lo que facilita la actualización.

Un ejemplo de archivo `config.py` podría ser:
```
from MeguRobot.sample_config import Config

class Development(Config):
    API_ID = 12489275 # integer value, dont use ""
    API_HASH = 'hg35k7gh683ghkj586hj35'
    OWNER_ID = 254318997 # Su ID de telegram.
    OWNER_USERNAME = "SonOfLars" # Su nombre de usuario de telegram.
    TOKEN = "your bot api key" # Su clave api, tal como la proporciona @botfather.
    SQLALCHEMY_DATABASE_URI = 'postgresql://nombredeusuario:contraseña@localhost:5432/database' # Credenciales de base de datos de muestra.
    JOIN_LOGGER = '-1234567890' # Algún chat grupal donde su bot este ahí.
    USE_JOIN_LOGGER = True
    SUDO_USERS = [18673980, 83489514] # Lista de identificadores de usuarios que tienen acceso superusuario al bot.
    LOAD = []
    NO_LOAD = ['translation']
```

Si no puede tener un archivo config.py (Ej.: en Heroku), también es posible usar variables de entorno. En ése caso, lea el archivo `sample_config`, en él están detalladas las variables.

### Dependencias de Python
Instale las dependencias necesarias de Python moviéndose al directorio del proyecto y ejecutando:

```pip3 install -r requirements.txt.```

Esto instalará todos los paquetes python necesarios.


### Base de datos
Si desea utilizar un módulo dependiente de la base de datos (por ejemplo: bloqueps, notas, userinfo, usuarios, filtros, bienvenidas), necesitará tener una base de datos instalada en su sistema. Yo uso Postgres, así que recomiendo usarlo para una compatibilidad óptima.

En el caso de Postgres, así es como se configuraría una base de datos en un sistema Debian/ubuntu. Otras distribuciones pueden variar.

* instalar postgresql:

```sudo apt-get update && sudo apt-get install postgresql```

* cambie al usuario de Postgres:

```sudo su - postgres```


* cree un nuevo usuario de base de datos (cambie TU_USUARIO adecuadamente):

```createuser -P -s -e TU_USUARIO```

A continuación, deberá introducir su contraseña.


* crear una nueva tabla de base de datos:

```createdb -O TU_USUARIO TU_NOMBRE_DE_BD```

Cambia TU_USUARIO y TU_NOMBRE_DE_BD adecuadamente.


* finalmente:

```psql TU_NOMBRE_DE_BD -h TU_HOST TU_USUARIO```

Esto le permitirá conectarse a su base de datos a través de su terminal. Por defecto, TU_HOST debería ser 0.0.0.0:5432.

Ahora deberías poder crear el URL de tu base de datos. Esta será:

```sqldbtype://nombre_de_usuario:pw@nombre_de_host:puerto/nombre_de_la_base_de_datos```

Sustituya ```sqldbtype``` por la base de datos que esté utilizando (por ejemplo, Postgres, MySQL, SQLite, etc.) y repita la operación con su nombre de usuario, contraseña, nombre de host (¿localhost?), puerto (¿5432?) y nombre de la base de datos.

## Módulos
### Establecer el orden de carga.
El orden de carga de los módulos se puede cambiar a través de los ajustes de configuración LOAD y NO_LOAD. Ambos deben representar listas.

Si ```LOAD``` es una lista vacía, todos los módulos en ```modules/``` serán seleccionados para cargar por defecto.

Si ```NO_LOAD``` no está presente o es una lista vacía, se cargarán todos los módulos seleccionados para la carga.

Si un módulo está tanto en ```LOAD``` como en ```NO_LOAD```, el módulo no se cargará - ```NO_LOAD``` tiene prioridad.

### Creación de módulos propios.
La creación de un módulo se ha simplificado al máximo, pero no dude en sugerir una mayor simplificación.

Todo lo que se necesita es que su archivo ```.py``` esté en la carpeta de módulos.

Para añadir comandos, asegúrate de importar el ```dispatcher``` mediante

```from MeguBot import dispatcher.```

A continuación, puedes añadir comandos utilizando el método habitual

```dispatcher.add_handler().```

Asignar la variable ```__help__``` a una cadena que describa los comandos disponibles de este módulo permitirá al bot cargarlo y añadir la documentación de su módulo al comando ```/help```. Establecer la variable ```__mod_name__``` también le permitirá utilizar un nombre más agradable y amigable para un módulo.

La función ```__migrate__()``` se utiliza para migrar chats - cuando un chat se actualiza a un supergrupo, el ID cambia, por lo que es necesario migrarlo en la DB.

La función ```__stats__()``` es para recuperar las estadísticas del módulo, por ejemplo, el número de usuarios, el número de chats. Se accede a ella a través del comando ```/stats```, que sólo está disponible para el propietario del bot.

## Iniciando el bot.
Una vez que hayas establecido tu base de datos y tu configuración esté completa, simplemente ejecuta el archivo bat (si estás en Windows) o ejecuta (Linux)

```python3 -m MeguBot```

Puedes usar [nssm](https://nssm.cc/usage) para instalar el bot como servicio en windows y configurarlo para que se reinicie en ```/gitpull```. Asegúrate de editar los bats de inicio y reinicio según tus necesidades. 
* Nota: ```el bat de reinicio requiere que el control de cuentas de usuario esté desactivado.```

Para consultas o cualquier problema relacionado con el bot, abra un hilo de problema (aka Issue Ticket) o visítenos en [Megu Support](https://t.me/MeguSupport)


<!-- CONTRIBUTING -->
## Contribuciones

Las contribuciones son lo que hace que la comunidad de código abierto sea un lugar increíble para aprender, inspirar y crear. *** Cualquier contribución que hagas será muy apreciada.***

1. Fork del Proyecto
2. Crea tu Branch de características (`git checkout -b feature/CaracteristicaGenial`)
3. Haz commit de tus cambios (`git commit -m 'Alguna característica genial'`)
4. Haz Push al Branch (`git push origin feature/CaracteristicaGenial`)
5. Abre una Pull Request

<!-- LICENSE -->
## License

Distribuído bajo la licencia GLP v3. Para más información revisa ```LICENSES```



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/xarturia/Megubot.svg?style=for-the-badge
[contributors-url]: https://github.com/xarturia/megubot/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/xarturia/megubot?style=for-the-badge
[forks-url]: https://github.com/xarturia/megubot/network/members
[stars-shield]: https://img.shields.io/github/stars/xarturia/megubot?style=for-the-badge
[stars-url]: https://github.com/xarturia/megubot/stargazers
[issues-shield]: https://img.shields.io/github/issues/xarturia/megubot?style=for-the-badge
[issues-url]: https://github.com/xarturia/megubot/issues
[license-shield]: https://img.shields.io/badge/License-GPLv3-brightgreen?style=for-the-badge&logo=appveyor
[license-url]: https://github.com/xarturia/megubot/blob/master/LICENCES.md
[product-screenshot]: https://i.imgur.com/KcCPvoi.png
