# 6 API REST Trello

En esta práctica jugamos un poco con la API Rest de Trellohttps://trello.com/ 
Para la cual solicitamos una API KEY y un Token

La solicitud se hace de la siguiente manera
1. Con una cuenta creada de Trello entramos al siguiente link: https://trello.com/app-key
  - Ve al portal
  - El primer valor que nos muestra es la API KEY
  
  ![image](https://github.com/OlafRuv/Trello-API/blob/main/imgs/1.png)
    
  - Damos click en el enlace a TOKEN 
  - Autorizamos la peticion:
  
  ![image](https://github.com/OlafRuv/Trello-API/blob/main/imgs/2.png)
  
  - Enseguida nos muestra el TOKEN:
  
   ![image](https://github.com/OlafRuv/Trello-API/blob/main/imgs/3.png)

3. Es importante guardar bien la API KEY y el TOKEN porque son informacion sensible

4. Si queremos aprender mas podemos visitar la documentación de la API Rest de Trello https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-group-boards, donde podremos econtrar:
   - Cómo crear un nuevo board.
   - Cómo obtener la información de un board a partir de su ID
   - Cómo obtener la lista de cards de un board
   - Cómo crear una nueva card en un board

5. Abrimos nuestro entorno de pruebas de Postman e importamos el siguiente archivo: 

[Trello API LaunchX.postman_collection.json.zip](https://github.com/LaunchX-InnovaccionVirtual/MissionNodeJS/files/8585319/Trello.API.LaunchX.postman_collection.json.zip)

# Ya podemos jugar con el Api de Trello con las peticiones armadas de postman: 
## Creamos un tablero.

6. Vamos a la petición de `POST Create board`:

![image](https://user-images.githubusercontent.com/62526919/168375764-6ba2dc58-decd-464a-a282-29b1fe2f1cd3.png)

7. En la sección de `params`, llenamos los valores (aquí incluimos nuestra api key en el campo `key` y el token en `Token`):

![image](https://user-images.githubusercontent.com/62526919/168376774-f85bb333-3981-4eaa-a140-ad8ecf5759ed.png)

8. Da click en SEND, mira el response y verifica que tu tablero nuevo se halla creado.

![6](https://user-images.githubusercontent.com/62526919/168377076-7cb7b400-16f2-44a6-a80b-a3256cf84894.png)
![7](https://user-images.githubusercontent.com/62526919/168377115-741342a4-fa90-4d14-ad3d-bcc18ea5a2d8.png)

9. Del response, hay un campo `id` que corresponde al ID del tablero que acabas de crear, guárdalo.

![8](https://user-images.githubusercontent.com/62526919/168377641-f8f4b9a2-4479-4ade-88f0-ec652cf356d3.jpg)


## Obtenemos la lista de columnas de tu board creado

10. Vamos a la petición de `GET Board by ID` 

![4,2](https://user-images.githubusercontent.com/62526919/168375929-ca0065c4-0acb-4adb-9b40-05b725815d7f.png)

11. Agregamos nuestra API KEY y TOKEN. 
12. En el Url agregamos el ID del board previamente creado

```
https://api.trello.com/1/boards/BOARDID/lists?key=APIKEY&token=TOKEN
```

13. Enviamos nuestro request, y verificamos la información que recibimos. Deberemos ver la lista de columnas que tienes en tu tablero:

![8](https://user-images.githubusercontent.com/62526919/168378300-0a6e152a-e4fd-4f9c-91ef-1ab512d1c151.png)

14. Tomamos el ID del primer registro que corresponde a la primer columna.

![9](https://user-images.githubusercontent.com/62526919/168378597-32eb3843-3d3a-4bd3-b6b7-25b7f19eaf1d.png)

## Agregamos nuevas cards a la primer columna de tu tablero

15. Vamos a la petición de `Create Card By List ID` 

![image](https://user-images.githubusercontent.com/62526919/168376325-fc3d01e0-b114-4a16-ace5-f3ad5bb3d525.png)

16. Agregamos los parámetros necesarios: `idList`, `key`, `token`, y `name` (el cual es el título de la nueva card).

17. Envía tu request y verifica que la respuesta sea éxitosa. Verifica que efectivamente se haya creado directo en la app de trello.

![10](https://user-images.githubusercontent.com/62526919/168379462-dcf4e82b-a93d-46e8-967a-fc81dafcec7d.png)
![11](https://user-images.githubusercontent.com/62526919/168379283-3c7a1760-197f-457d-a3d1-190f1eaf594b.png)

# ¡Felicidades así es como puedes usar Trello mediante su API Rest!
