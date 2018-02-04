# Ejecución de consultas en OrionX desde Java

En este tutorial se desarrolla una solución en Java para que cualquiera pueda hacer consultas sobre la API de OrionX desde cualquier máquina conectada a internet. 

No están todas las consultas disponibles en la plataforma API, y esto es a propósito. La idea es que leas y entiendas el código para así perfeccionarlo y aplicar tu intelecto en nuevas soluciones. Aquí sólo se expone la base del desarrollo del `cliente` que consume la API de OrionX.

# Prerequisitos

Para poder ejecutar el programa, debes primero tener un compilador de Java. Recomiendo descargar la última versión disponible de [Eclipse](http://www.eclipse.org/downloads/) o bien de [NetBeans](https://netbeans.org/downloads/).

Ya que Java es un lenguaje [Multiplataforma](https://es.wikipedia.org/wiki/Multiplataforma), no hay escusas par no poder ejecutar el software. Esta característica, te permitirá correrlo en Windows, en MAC, obviamente en GNU/Linux y practicamente en cualquier dispositivo. 

# Obtención de código

Para obtener el código fuente, puedes descargarlo directamente [Aquí](https://github.com/panterozo/API2-OrionX/archive/master.zip) o hacer `clone` al repositorio.

```sh
$ git clone https://github.com/panterozo/API2-OrionX.git
```

# Trabajando con Eclipse

Una vez descargado, debes importar el proyecto dentro del [IDE](https://es.wikipedia.org/wiki/Entorno_de_desarrollo_integrado) descargado anteriormente. En mi caso, utilizaré Eclipse.

Al abrir Eclipse, debes ir al menú principal y dar click en `Archivo => Importar...`. Esto desplegará un conjunto de opciones. En ellas, tienes que indicarle que importarás desde un proyecto existente, tal como se muestra en la imagen:

<div align="center">
	<a href="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/ExistingProject.png">
		<img style="width: 50%" src="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/ExistingProject.png">
	</a>
</div>

Luego, seleccionas la carpeta donde descargaste el proyecto:

<div align="center">
	<a href="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/SelectFolder.png">
		<img style="width: 50%" src="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/SelectFolder.png">
	</a>
</div>

* Importante: Si descargaste el archivo `.zip`, debes descomprimirlo para poder realizar la importación dentro de Eclipse.

Si todo salió bien hasta este punto, debería haberse importado correctamente el proyecto y deberías ver las `clases` como en la siguiente imagen:

<div align="center">
	<a href="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/ClassesError.png">
		<img style="width: 50%" src="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/ClassesError.png">
	</a>
</div>

El proyecto utiliza la librería [JSON](http://www.java2s.com/Code/JarDownload/java/java-json.jar.zip) que viene incluida dentro de la carpeta lib. Debes incluir el `.jar` al path para poder compilar el proyecto. 


<div align="center">
	<a href="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/BuildPath.png">
		<img style="width: 50%" src="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/BuildPath.png">
	</a>
</div>

Con ello, el proyecto podrá compilar sin problemas. Las clases deben aparecer como en la siguiente imagen:

<div align="center">
	<a href="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/ClassesImage.png">
		<img style="width: 50%" src="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/ClassesImage.png">
	</a>
</div>

Una vez incluida la librería JSON, debes incluir tus KEYS creadas en OrionX. Si aún no lo has hecho, puedes seguir [este tutorial](https://www.orionx.io/developers/tutorials/creacion-api-key). Debes incluir las llaves en los siguientes elementos:

```sh
user.setApiKeyPublic("AQUI TIENES QUE PONER TU API KEY");
user.setSecretKey("AQUI TIENES QUE PONER TU SECRET KEY");
```

<div align="center">
	<a href="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/settingUpKeys.png">
		<img style="width: 50%" src="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/settingUpKeys.png">
	</a>
</div>

De tal manera que quede algo como esto:

```sh
user.setApiKeyPublic("ERssdrbrajh8o6a744fdVFvdfvSPYPqz");
user.setSecretKey("WsdKztw9CcnnYrOM8SExKSN5sqiEr5hw9P");
```

Ahora podrás ejecutar el programa sin problemas. Para ello, debes clickear con el botón derecho del mouse sobre la clase OrionXBase.java, y seleccionar `Run As... Java Application`, como se muestra en la imagen abajo.

<div align="center">
	<a href="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/RunProgram.png">
		<img style="width: 50%" src="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/RunProgram.png">
	</a>
</div>


Con la ejecución, deberías obtener los resultados en la consola de Eclipse.

<div align="center">
	<a href="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/Reponses.png">
		<img style="width: 50%" src="https://raw.githubusercontent.com/panterozo/API2-OrionX/master/img/Reponses.png">
	</a>
</div>

<!--# Obtener Código Fuente

Para obtener el código fuente, puedes descargarlo en un zip desde [Aquí](https://raw.githubusercontent.com/orionsoft/orionx-developers-tutorials/master/tutorials/java/Zipped-API2-OrionX_v1.0.zip), o bien desde el repositorio de origen [aquí](https://github.com/panterozo/API2-OrionX/archive/master.zip).
-->

