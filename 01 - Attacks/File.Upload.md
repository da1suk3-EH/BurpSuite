**IMPORTANT:** FOR LEGAL PURPOSES ONLY<br>
**Objective:** 

<br>

## Subir archivo


Comprobar que esta limitado solo a formatos de imagenes, probando el **reverse.php** previamente configurado.

![Image](https://github.com/user-attachments/assets/21b46800-6cf0-4dd8-b8b4-372740dfb5e6)
<br>

**Activar** en BurpSuite el **Intercept**.

![Image](https://github.com/user-attachments/assets/edad7ea0-0d39-4c23-91c7-f37ed03f68c6)
<br>

Primero, subir una foto real. Se abrira el BurpSuite interceptando la petición. 
Abajo en Request copiar la cabezera de **Content-Type: image/jpeg** y rechazar esta petición con **Drop**.

![Image](https://github.com/user-attachments/assets/5a2620c9-2f7e-4c15-934e-6d055bd7c137)
<br>

Ahora si, subir el archivo **reverse.php**

![Image](https://github.com/user-attachments/assets/ba61ccab-508d-4609-ba09-b0198b3f2788)
<br>

Cuando se vuelva a abrir el BurpSuite. Cambiar el **Content-Type: application/x-php** a **image/jpeg**.

![Image](https://github.com/user-attachments/assets/0ce77bef-6bf1-4870-8d34-88eeef213879)
<br>

Una vez cambiado presionar **Forward**.

![Image](https://github.com/user-attachments/assets/a19d0350-ff9a-403d-a403-f214983681c5)
<br>

Ver que la pagina efectivamente a aceptado este archivo como una imagen.

![Image](https://github.com/user-attachments/assets/e6136312-3337-46f6-9bca-88f513f30f47)
<br>

Ir a la ruta que te indica donde subio el **reverse.php**.

![Image](https://github.com/user-attachments/assets/56d6d511-bb7c-4b83-b37f-65baa24d28aa)
<br>

Para **abrir la shell**, hay que dirigirse al Kali y abrir el puerto con el comando **nc -lvnp 4444**.

![Image](https://github.com/user-attachments/assets/1fb22dd0-f782-4edc-88c0-d270b2322819)
<br>

Para terminar, simplemente dar click en el **reverse.php** y ya estarias dentro.

![Image](https://github.com/user-attachments/assets/20b1b90e-0452-4de7-861b-6670053c9434)
<br>
