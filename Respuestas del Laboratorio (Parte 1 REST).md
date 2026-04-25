### **Respuestas del Laboratorio (Parte 1: REST)**

* **¿Qué API elegiste y por qué?**
    Elegí una combinación de dos APIs para cubrir todo el alcance solicitado. Utilicé **Random User** para las pruebas de consumo masivo y filtrado de datos básicos por su facilidad de uso, y **The Lord of the Rings API (The One API)** para implementar la autenticación. Elegí esta última porque, a diferencia de las otras, exige un registro previo y el uso de un token real, cumpliendo con la aclaración del docente sobre el uso obligatorio de autorización.

* **¿Qué datos devuelve?**
    **Random User** devuelve objetos JSON con datos de identidad ficticios (nombres, correos, géneros y nacionalidades). **The Lord of the Rings API** devuelve metadatos detallados de la obra de Tolkien, incluyendo una lista de películas con sus presupuestos y duraciones, así como un arreglo de "quotes" (frases) vinculadas a personajes y diálogos específicos.

* **¿Usa token o no? ¿Qué tipo?**
    Sí. Mientras que Random User es de acceso abierto, la API del Señor de los Anillos requiere un **Access Token**. El tipo de autenticación utilizado en Postman fue **Bearer Token**, el cual se envía en el encabezado (header) de la petición para validar los permisos de acceso.

* **¿Qué código de estado recibiste en cada request?**
    En todas las peticiones exitosas recibí un código **200 OK**, lo que indica que el servidor procesó la solicitud correctamente. En el caso de la API con token, si intentaba enviar la petición sin el Bearer Token, recibía un **401 Unauthorized**, confirmando que la seguridad estaba activa.

* **¿Qué aprendiste diferente a JSONPlaceholder?**
    Aprendí que las APIs reales tienen estructuras más complejas; por ejemplo, los datos no siempre están en la raíz, sino dentro de propiedades como `results` o `docs`. También aprendí a gestionar la seguridad mediante **Bearer Tokens**, algo que JSONPlaceholder no exige, y a utilizar **Query Params** avanzados para limitar resultados (`?limit=10`) o filtrar por campos específicos (`?inc=name`), lo que optimiza el consumo de datos en aplicaciones reales.