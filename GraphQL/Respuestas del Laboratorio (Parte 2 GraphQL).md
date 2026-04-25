### **Respuestas del Laboratorio (Parte 2: GraphQL)**

* **¿Qué diferencia encontraste vs REST?**
    La diferencia principal es el control sobre los datos. En **REST**, el servidor decide qué enviarme (yo pido un país y me llega todo el objeto con 50 campos aunque solo quiera el nombre). En **GraphQL**, yo (el cliente) tengo el control: escribo una consulta pidiendo exactamente los campos que necesito y el servidor responde solo con eso. Además, en REST usé múltiples rutas (endpoints) como `/movie` o `/character`, mientras que en GraphQL toda la comunicación se hace a través de un **único endpoint** mediante peticiones **POST**.

* **¿Cuántos requests REST necesitarías para reemplazar tu query más compleja?**
    Para mi query más compleja (donde pedí un **Continente**, todos sus **Países** y los **Idiomas** de cada país), en REST habría necesitado **mínimo 3 peticiones**:
    1.  Una para obtener los datos del continente.
    2.  Otra para obtener la lista de países de ese continente.
    3.  Y una serie de peticiones adicionales (o una muy grande) para obtener los idiomas de cada país. 
    En GraphQL, logré traer toda esa estructura anidada y relacionada en **una sola petición**.

* **¿En qué proyecto real usarías GraphQL?**
    Lo usaría en proyectos donde la eficiencia de la red sea crítica, como una **aplicación móvil** (donde el usuario puede tener datos limitados) o en un **Dashboard de administración** muy complejo. También es ideal para aplicaciones tipo redes sociales o e-commerce, donde los datos están muy relacionados entre sí (ejemplo: un post que tiene comentarios, y cada comentario tiene un autor con su foto), permitiendo cargar todo el muro de una sola vez sin sobrecargar el servidor con múltiples llamadas.