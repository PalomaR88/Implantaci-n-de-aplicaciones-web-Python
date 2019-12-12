# Entornos virtuales

### Entornos pypi
Se utiliza pip para instalar.

Para instalar un paquete de python hay 3 opciones:
- apt-get: este no se va a utilizar porque vamos a trabajar en entornos y de esta forma no se garantiza que funcione en el entorno de producción y en el estable.
- Como root pip. Los paquetes que se instalan se realizan en el sistema, pero esto tiene un problema y es que puede que se instalen versiones diferentes a los paquetes python que ya están en el sistema.
- En el entorno virtual, de esta forma los paquetes que se instalen solo se instalan en el directorio del usuario del entorno virtual. 

## Creación de los entornos virtuales:
1. Se crea una carpeta dentro de /virtualenv. 
 
2. Se crea el direcotrio, en este caso llamado django:
~~~
python3 -m venv django
~~~

3. Se activa el entorno. Dentro del entorno no existen los paquetes python del sistema. 
~~~
source django/bin/activate
~~~

4. Se instalan los paquetes que se quieran:
~~~
pip install django
~~~

5. Para ver los paquetes instalados:
~~~
$ pip freeze
Django==2.2.7
pkg-resources==0.0.0
pytz==2019.3
sqlparse==0.3.0
~~~
El paquete pkg-resource se recomienda eliminar de la lista o desinstalarlo del entorno porque es problemático.

6. Para llevarse los paquetes a otro entorno:
~~~
pip freeze > requirements.txt
~~~
Se guardan en requirements.txt y hay que copiarlo al nuevo entorno.

7. Para instalar los paquetes en el nuevo entorno virtual:
~~~
pip install -r requirements.txt
~~~




