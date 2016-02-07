# API-RESTful-Python #

## Introducción ##

Este es un ejemplo basico para la creción de un API Restful usando Python con 
el framework [Flask][1] y [Flask-RESTful][2], se utiliza dos EndPoint HTTP (GET y POST), 
ademas se incorpora un metodo de authentication Basic para poder hacer las peticiones al API.

Este docuemento contiene instrucciones breves sobre la instalación de requerimientos,
instalación de los framework [Flask][1] y [Flask-RESTful][2]

Para más información, consulte:

  * [Flask][1],
  * [Flask-RESTful][2],

[1]: http://flask.pocoo.org
[2]: http://flask-restful-cn.readthedocs.org/en/0.3.4/

La API fue desarrollada en un sistema operativo Mac OS Yosemite 10.10.5

## Instalación ##

    sudo easy_install pip
    sudo pip install virtualenv

## Ejecutar el APPI RESTful ##

Primer paso, se debe acceder a nuestro proyecto 

    cd API-Restful-Python

A continuacion ejecutamos virtualenv:
    
    virtualenv flask

procedemos a instalar Flask y Flask-RESTful en nuestro proyecto

    flask/bin/pip install flask
    flask/bin/pip install flask-restful

asignamos permiso de ejecucion a nuestro archivo apprestful.py:
    
    chmod a+x apprestful.py

ejecutamos nuestro archivo:

    ./apprestful.py

Debe indicarnos que esta en ejecución nuestra API RESTful

    * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
    * Restarting with stat
    * Debugger is active!
    * Debugger pin code: 378-764-549

## Otras Configuraciones ##

si requieres de cambiar el puerto (default = 5000) por el puerto 9001:

abrimos el archivo apprestful.py y cambiamos esta linea:
      
      app.run(debug=True)

por esta otra:
      
      app.run(port = 9001, debug=True)


### Usando la API

Ejemplo de uso de llamadas al API usando `curl` para las peticiones:

#### Regresa un JSON con todos los usuarios registrados (dispositivos iOS y/o Android en nuestro caso )

  $ curl -X GET -u "<user>:<pwd>" http://<server_ip>:5000/users

#### Agrega un nuevo usuario (dispositivo iOS y/o Android en nuestro caso )

  $ curl -u "<user>:<pwd>" http://<server_ip>:5000/users -H "Content-Type: application/json" --data '{"idUser":"4","UDID":"hjsgjkdhgah","NmbrDisp":"aMEJIA","Device":"iOS"}' -X POST -v



## Contact ##

Abel Mejía Hernández <abel.mejia.hdz@gmail.com>