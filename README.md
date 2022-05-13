# 6 API REST Trello

1. Abre una cuenta de Trello https://trello.com/
2. Para jugar con el API Rest de Trello necesitamos un api key y un token que puedes solicitar aquí: https://trello.com/app-key
  - Ve al portal
  - El primer valor que te mostrará es tu API KEY, guárdalo muy bien.
  
  
  
  - Da click en el enlace a TOKEN 
  
  
  Imagen de ejemplo

  - Te pedirá autorizar tu petición:
  
  
  - Enseguida te mostrará el TOKEN:
  

3. Guarda muy bien tu API KEY y TOKEN (estos valores son como tu usuario y password, ES INFORMACIÓN SENSIBLE).


4. Visita la documentación del Api Rest de Trello https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-group-boards
   - Busca cómo crear un nuevo board.
   - Busca cómo obtener la información de un board a partir de su ID
   - Busca cómo obtener la lista de cards de un board
   - Busca cómo crear una nueva card en un board

5. Descarga el siguiente archivo de postman e importalo en tu postman: [ ACTUALIZADO Trello API LaunchX.postman_collection.json.zip](https://github.com/LaunchX-InnovaccionVirtual/MissionNodeJS/files/8585319/Trello.API.LaunchX.postman_collection.json.zip)


# Juega con el Api de Trello con las peticiones armadas de postman: Crea un tablero.

6. Ahora sí ve a la siguiente petición para crear un board `POST Create board`:

7. En la sección de `params`, llena los valores (aquí incluye tu api key en el campo `key` y el token en `Token`):

8. Da click en SEND, mira el response y verifica que tu tablero nuevo se halla creado.


9. Del response, hay un campo `id` que corresponde al ID del tablero que acabas de crear, guárdalo.


# Obtén la lista de columnas de tu board creado

10. Abre el siguiente request: 

11. Agrega tu API KEY y TOKEN. 

```
https://api.trello.com/1/boards/BOARDID/lists?key=APIKEY&token=TOKEN
```

13. Envía tu request, y verifica la información que rexcibes. Deberás ver la lista de columnas que tienes en tu tablero:


14. Toma el ID del primer registro que corresponde a la primer columna.

# Agrega nuevas cards a la primer columna de tu tablero

15. Abre el request POST `Create Card By List Id`:

16. Agrega los parámetros necesarios: `idList`(el id de la primer columna del paso anterior), `key`, `token`, y `name` (este es el título de tu card nueva).

17. Envía tu request y verifica que la respuesta sea éxitosa. Verifica que efectivamente se haya creado directo en la app de trello.


# ¡Felicidades!

Explora la documentación del Api Rest de Trello e investiga:
- Cómo actualizar el título de una card.
- Cómo eliminar una card.

Recuerda que tu API KEY y TOKEN es información sensible. No debes de compartirla con nadie NI MUCHO MENOS VERSIONARLA Y SUBIRLA A GITHUB.
