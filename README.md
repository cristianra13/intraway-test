# Intraway-test

_Prueba técnica para Intraway donde a partir de dos números dados, se validan los múltiplos de 3, 5 o ambos.
1) Si el número es múltiplo de 3 -> imprimir “Fizz” 
2) Si el número es múltiplo de 5 -> imprimir “Buzz” 
3) Si es múltiplo de ambos -> imprimir “FizzBuzz”

## Backend

### Pre-requisitos 📋

_1. Se debe tener una base de datos instalada localmente en Mongo
_2. Se debe contar  con la versión de 11 o superior para ejecutar el proyecto
_3. Se debe contar con la instalación de Maven

### Instalación 🔧

_ Se deben descargar las dependencias del proyecto inicialmente con:

```
mvn clean install
```

## Ejecución de pruebas unitarias ⚙️
_El proyecto cuenta con sus respectivas pruebas unitarias las cuales se puede ejecutar con:

```
mvn test
```

_Una vez ejecutadas, el proyecto cuenta con un plugin llamado **Jacoco** con el cual se puede ver el pocentaje de cubrimiento de pruebas. Estás quedan almacenadas en la ruta:
```
target/site/index.html
```

## Endpoints
Se cuentan con dos respectivos endpoints los cuales van por método GET:
_El primero se encarga de recibir dos parámetros por url para el valor mínimo y el valor máximo los cuales se procesarán y darán su respectivo resultado:

```
localhost:8080/intraway/api/fizzbuzz/{min}/{max}
```

Por ejemplo, al ejecutar **http://localhost:8080/intraway/api/fizzbuzz/1/15** obtendremos como resultado:
```
{
    "id": "608ab88703e95d0c94f6f6a4",
    "min": "1",
    "max": "15",
    "timestamp": 1619703943010,
    "statusCode": 200,
    "description": "multiples of 3 and 5 were found.",
    "uuid": "4bc6a1f2-8c4e-4c93-bb7a-3644994cda60",
    "list": "1,2,Fizz,4,Buzz,Fizz,7,8,Fizz,Buzz,11,Fizz,13,14,FizzBuzz"
}
```

_El Segundo endpoint se encarga de mostrar un listado de todos los procesos que se han enviado y están almacenado en base de datos:

```
localhost:8080/intraway/api/fizzbuzz/list
```

Para este obtendremos como resultado de ejemplo:
```
 [
    {
        "id": "608ab626e3af874d07ecad01",
        "min": "1",
        "max": "15",
        "timestamp": 1619703334419,
        "statusCode": 200,
        "description": "multiples of 3 and 5 were found.",
        "uuid": "fb0e3865-aec7-4549-91e7-db12dece03da",
        "list": "1,2,Fizz,4,Buzz,Fizz,7,8,Fizz,Buzz,11,Fizz,13,14,FizzBuzz"
    },
    {
        "id": "608ab88003e95d0c94f6f6a3",
        "min": "10",
        "max": "10",
        "timestamp": 1619703936074,
        "statusCode": 200,
        "description": "multiples of 5 were found.",
        "uuid": "f28d8b0d-da4c-4f66-abe5-a1e4e4cb259d",
        "list": "Buzz"
    },
    {
        "id": "608ab88703e95d0c94f6f6a4",
        "min": "1",
        "max": "15",
        "timestamp": 1619703943010,
        "statusCode": 200,
        "description": "multiples of 3 and 5 were found.",
        "uuid": "4bc6a1f2-8c4e-4c93-bb7a-3644994cda60",
        "list": "1,2,Fizz,4,Buzz,Fizz,7,8,Fizz,Buzz,11,Fizz,13,14,FizzBuzz"
    }
]
```


## Frontend
El proyecto cuenta con su parte visual desarrollada en Angular 11.

### Pre-requisitos 📋
_1. Es importante que al clonar elproyecto, se instalen las dependencias de npm
```
npm install
```
_2. Una vez instaladas, se debe ejecutar el proyecto con:

```
ng serve -o
```

## Endpoints
El Proyecto se desplegará en la url http://localhost:4200
