## Instrucciones

Se pide diseñar un formulario para los clientes de la empresa de manera similar al creado en clase.

Los datos de los clientes se encuentran en el fichero [Clientes](./clientes.dat).

En dicho fichero están almacenados los datos de los clientes en el siguiente orden:

`id, nombre, apellidos, empresa, direccion, ciudad, estado, pais, codigoPostal, telefono, fax, email, idRepresentante, urlFoto`

Donde los campos `id` e `idRepresentante` son enteros y el resto cadenas de texto.

El formulario deberá emplear un diseño basado en un `GridBagLayout` y deberá redimensionarse de manera adecuada.

Será necesario definir una clase `Cliente`, un interfaz `ClienteDAO` con métodos para obtener todos los clientes, buscar un cliente en base al id  y para modificar un cliente y una clase `ClienteFich` que implemente dicho interfaz. Además se añadirán una propiedad de dicha clase y los mismos métodos a la clase de servicio ya creada. Podéis, si queréis, crear una **clase de servicio**.

El campo `idRepresentante` se mostrará en el formulario como un `JComboBox` (que configuraremos en una actividad posterior).

El formulario mostrará todos los controles (excepto el `id`) como editables y dispondrá, aparte de los botones de desplazamiento, de botones para `guardar`, `cancelar` y `salir`. Esto se hará en un método `mostrar` en el que se actualizará la información del formulario en base al cliente actual (`pos`) (excepto el `JComboBox` que todavía no sabemos cómo hacerlo). 

El método `guardar` creará un nuevo cliente con la información del formulario (excepto el campo `idRepresentante` que se cogerá del cliente en la posición actual). Tras ello se llamará al método `modificar` del servicio y luego a `mostrar`.

El método `cancelar` simplemente llamará a `mostrar` y el método `salir` finalizará la aplicación.
