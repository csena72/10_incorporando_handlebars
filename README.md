# Desafío #10 Incorporando Handlebars

### Consigna:  
Sobre el proyecto entregable de la clase anterior, incorporar y configurar el motor de plantillas handlebars para que permita ver mediante la ruta get '/productos/vista' los productos cargados.

## Aspectos a incluir en el entregable:
- Realizar las plantillas correspondientes que permitan recorrer el array de productos y representarlo en forma de tabla dinámica, siendo sus cabeceras el nombre de producto, el precio y su foto (la foto se mostrará como un imágen en la tabla)
- En el caso de no encontrarse datos, devolver el mensaje: 'No hay productos'
- Utilizar bootstrap para maquetar la vista creada por dicho motor de plantillas.
- Maquetar con bootstrap el formulario de ingreso de productos. Al guardar el producto, se debe redirigir la vista al formulario vacío.

### Sugerencias:
- Utilizar iconfinder (https://www.iconfinder.com/free_icons) para obtener la url de las imágenes de los productos (click derecho sobre la imagen -> copiar dirección de la imagen)
- Probar desde postman las demás funciones (actualizar y borrar producto) y ver el resultado reflejado en la tabla de productos.

## Ejemplo para consumir el EP que actualiza un producto:

```
curl --location --request PUT 'localhost:8080/api/productos/2' \
--header 'Content-Type: application/json' \
--data-raw '[
    {
        "title": "manzana",
        "price": "222",
        "thumbnail": "dsafwea"        
    }
]'
```

## Ejemplo para consumir el EP que borra un producto:

```
curl --location --request DELETE 'localhost:8080/api/productos/2'
```