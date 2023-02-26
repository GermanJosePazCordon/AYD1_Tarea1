UNIVERSIDAD DE SAN CARLOS DE GUATEMALA 

FACULTAD DE INGENIERÍA

ESCUELA DE CIENCIAS Y SISTEMAS

PRIMER SEMESTRE 2023

LABORATORIO SOFTWARE AVANZADO 

![](logo.png)

# *INFING-USAC*

<br>

INTEGRANTES


|**CARNE**|**ESTUDIANTE**|**PARTICIPACIÓN**|
| :- | :- | :- |
|201901510|Pablo Daniel Rivas Marroquin     |100%|
|201902934|German Jose Paz Cordon           |100%|
|201903850|Adrian Samuel Molina Cabrera     |100%|
|201900955|Diego Fernando Cortez Lopez      |100%|

<br>

GUATEMALA 25 DE FEBRERO DE 2023

---
<br>

## **Descripcion de la seguridad de la aplicacion**

**JWT (JSON Web Token)**

Utilizamos JWT para garantizar que la información enviada entre los servicios sea auténtica y no pueda ser alterada además de evitar que los usuarios manden sus credenciales constantemente. En el siguiente esquema se presenta la estructura del JSON que se utilizará para este proyecto.

```json
{
    "id": 1,
}
```

**Encriptacion SHA256**

Utilizamos SHA256 para la encriptación de datos sensibles como credenciales de los usuarios para aumentar la seguridad de la información almacenada garantizando que los datos sean seguros y que los posibles  atacantes no puedan acceder a la información original.

<br>

## **Diagrama de Pipelines**

[]()

El escenario de Build Images es la etapa donde se realiza la construcción de las imágenes de Docker para los servicios de la plataforma.

El escenario de Push Images es la etapa donde se publican las imágenes, creadas en el escenario anterior, a un contenedor de Docker.

El escenario de Test es la etapa donde se ejecutarán las pruebas unitarias para notificar fallos.

El escenario de Build Backend levanta cada una de las imágenes de los servicios, para poder ejecutar al backend de la plataforma, de forma que una no dependa de la otra al levantarse.

El escenario de Build Frontend levanta la imagen del frontend.

<br>

## **Análisis y solución de la problemática propuesta**

<p style="text-align: justify;">
Se desea desarrollar un software, que permita conectarse con fuentes externas, para la gestión de las actividades empresariales; que permita facilitar el registro de usuarios, la administración de recursos humanos, compra y ventas de productos,  inventario, contabilidad y rutas de distribución. La plataforma deberá contar con una amplia variedad el catálogo de los productos para que los usuarios puedan realizar dichas acciones. Además, se debe generar e integrar la lógica necesaria para el reabastecimiento de productos. 
</p>

<p style="text-align: justify;">
Bajo esta problemática, se procedió a realizar el desarrollo de la solución donde se tomó la decisión de crear e implementar una plataforma que funcione a base micro servicios de manera que funcionen de forma independiente entre sí. Esto con la finalidad de que los demás micro servicios sigan en ejecución sin importar el caso donde alguno de estos llegara a detenerse.  
</p>

<p style="text-align: justify;">
Los servicios funcionan de manera aislada, cada bajo su propia lógica, con el propósito de proporcionarle a la plataforma mayor tolerancia a fallo, escalabilidad y flexibilidad, ya que si se quiere agregar una nueva funcionalidad o simplemente realizar un mantenimiento, esto pueda hacerse sin comprometer la integridad de los servicios existentes.
</p>
<br>

## **Metodología de ágil justificada del porqué de su selección con sus respectivas etapas**

<p style="text-align: justify;">
Utilizamos la metodología SCRUM porque consideramos que es la más adecuada en este tipo de desarrollo de software. Scrum fomenta la colaboración, la flexibilidad y la transparencia, lo que ayuda a aumentar la calidad, la productividad y el compromiso del equipo. Las etapas de la metodología SCRUM se dividen en varias por cada ciclo interactivo llamado Sprint, estas son las siguientes
</p>

<p style="text-align: justify;">
Sprint Planning: en esta etapa, el equipo Scrum se reúne para definir el objetivo del Sprint y acordar las tareas que se llevarán a cabo durante el mismo
</p>

<p style="text-align: justify;">
Sprint: en esta etapa, el equipo Scrum trabaja en las tareas identificadas en la Planificación del Sprint para alcanzar el objetivo definido.
</p>

<p style="text-align: justify;">
Daily Scrum: en esta etapa, el equipo Scrum se reúne diariamente para discutir el progreso del trabajo y cualquier obstáculo que se haya encontrado.
</p>

<p style="text-align: justify;">
Sprint Review: en esta etapa, el equipo identifica oportunidades de mejora y define los próximos pasos para el siguiente Sprint.
</p>

<p style="text-align: justify;">
Sprint Retrospective: en esta etapa, el equipo Scrum se reúne para revisar el proceso y discutir formas de mejorar la eficiencia y la calidad del trabajo en el futuro.
</p>


---

<br>

## **MICROSERVICIOS**

A continuación se muestran todos los aspectos de cada módulo que se asignaron a los desarrolladores para realizar sus microservicios.


|**DESARROLLADOR**|**MÓDULO**|
| :- | :- |
|Pablo Daniel Rivas Marroquin   |<p>- </p><p>- </p>|
|German Jose Paz Cordon         |<p>- </p><p>- </p>|
|Adrian Samuel Molina Cabrera   |<p>- </p><p>- </p>|
|Diego Fernando Cortez Lopez    |<p>- </p><p>- </p>|
<br>


**Código de respuestas exitosas**

Se utilizaron la siguiente lista de errores

|Código|Descripción|
| :- | :- |
|200|Solicitud aceptada; la respuesta contiene el resultado|
<br>

**Código de respuestas fallidas**

Se utilizaron la siguiente lista de errores

|Código|Descripción|
| :- | :- |
|400|La solicitud no fue válida. Este código se devuelve cuando el servidor ha intentado procesar la solicitud|
|500|Se ha producido un error interno en el servidor|
<br>

**Cuerpo de Token**
```
{
    "id" : "001"
    "exp" : 1677041618
}
```
---
<br>

## **Endpoint 1**

Este microservicio fue elegido debido a que necesitamos obtener un token para validar la existencia del usuario y realizar las operaciones dentro de la plataforma.

<Table>
    <tr>
        <th>ID: 001</th>
        <th>Nombre: Microservicio acceso de usuarios</th>
    </tr>
    <tr>
        <td ><b>Prioridad:</b></td>
        <td>
            <p><b>Historia de usuario:</b></p>
            <p>Descripcion de la historia</p>
        </td>
    </tr>
    <tr>
        <td colspan="4"><b>Estimado:</b> </td>
    </tr>
    <tr>
        <td colspan="4"><b>Modulo:</b> </td>
    </tr>
    <tr>
        <td colspan="4">
             <p><b>Criterio de aceptación:</b></p>
             <p>Descripcion del criterio de aceptacion</p>
             <p>El servicio debe de tener la siguiente configuración</p>
             <p><b>Ruta:</b>    <br>
             <b>Método:</b>     <br>
             <b>Descripción:</b>    </p>
        </td>
    </tr>
</Table>


**Formato de entrada:** JSON

**Header:**
|**Atributo**|**Tipo**|**Descripción**|
| :- | :- | :- |
| Content type | header | application/json |

**Body:**

|**Atributo**|**Tipo**|**Descripción**|
| :-         | :-     | :-            |
|            |        |               |

**Ejemplo de body de entrada:**
```
{
    "": ""
}
```
**Formato de salida:** JSON

**Código de respuesta exitosa:** HTTP 200

|**Atributo**|**Tipo**|**Descripción**|
| :-         | :-     | :-            |
| status | Integer | Código de respuesta |
| token | String | Token de autenticación |
<br>

**Ejemplo de parámetros de salida exitosa:**

```
{
    "status" : 200,
    "token" : d45a98d4a6d58nfuf9837489vfsmoiksa4d54a…
}
```

**Formato de salida:** JSON

**Código de respuesta fallida:** HTTP 400, HTTP 500

|**Atributo**|**Tipo**|**Descripción**|
| :- | :- | :- |
| status | Integer | Código de respuesta |
| description | String | Descripción del error |

**Ejemplo de parámetros de salida fallida:**

```
{
    "status" : 400,
    "description" :  "Descripcion del error"
}
```

---
<br>
