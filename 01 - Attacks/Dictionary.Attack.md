**IMPORTANT:** FOR LEGAL PURPOSES ONLY.<br>
**Objective:** Attack on login credentials with dictionary attack.

<br>

## Ataque de diccionario
<br>

Para empezar, en el panel de login, sacar el mensaje de **error** por credenciales incorrectas.

![Image](https://github.com/user-attachments/assets/78342547-5d5d-4ed0-8f50-d1ef2cad33aa)
<br>

Después, ir al BurpSuite a **Proxy > HTTP history**. Si no has navegado mas por la web, dar a la ultima consulta. 
        En **Request** estará nuestra petición, con información importante, como el método usado o la cookie. 
        En **Response**, dar a render y así confirmar que esta la consulta con el error. 

![Image](https://github.com/user-attachments/assets/66a4b272-c5b5-455c-b796-5ba21626cc94)
<br>

En la ventada de **Request** hacer click derecho y elegir la opción **Send to intruder**. Cambiar a la pestaña **Intruder**.

![Image](https://github.com/user-attachments/assets/e8e03a04-420f-4ff4-b337-ed5b824873d7)
<br>

Primero hay que elegir el modo de ataque. Los más comunes serán:<br>
        -**Sniper attack**, cuando se conoce uno de los parámetros.<br>
        -**Clustar bomb attack**, cuando no se conoce ninguno.

![Image](https://github.com/user-attachments/assets/00e0ffff-b60f-40ab-a169-da974a87059d)
<br>

**Seleccionar** el resultado de **username y password** o el campo que se quiera averiguar y presionar en **Positions** el botón **Add**. 
Quedarán marcados los objetivos para cargar los **Payloads**.

![Image](https://github.com/user-attachments/assets/fb9359c3-69c7-4d44-aeeb-4a1467a2d154)
<br>

Ahora, configurar los **Payloads**. Seleccionar el primero. Que, en ese caso, corresponde al de usuario.

![Image](https://github.com/user-attachments/assets/9ce44d72-1f19-49cf-95c5-c90c3bafe694)
<br>

Bajar a Payload configuration. Aquí, puedes escribir una pequeña lista o como en este caso cargar una lista de usuarios comunes.

![Image](https://github.com/user-attachments/assets/5deda0ed-1835-4d1f-9513-c432d42fed87)
<br>

Buscar tu diccionario preferido y lo abres con **Open**. Ver, que se han cargado los resultados del diccionario.

![Image](https://github.com/user-attachments/assets/a963287b-9eda-4f66-90dd-acdfead860cc)
<br>

Ir al Setting de la derecha y bajar hasta **Grep – Extract > Add**.

![Image](https://github.com/user-attachments/assets/9052318b-aad8-432c-acb5-3fc3967e40a7)
<br>

En la nueva ventana, hay que buscar en el codigo el mensaje de error que nos apareció: “Username and/or password incorrect.” 
O más fácil, en el buscador de abajo se pega y ya aparecerá. Una vez seleccionado terminamos con OK.

![Image](https://github.com/user-attachments/assets/ff80cead-efb8-4057-b02d-9f0fe3930b73)
<br>

No olvidar cargar el diccionario que falta en el segundo **Payloads**.

Terminada la configuracion, ejecutar con **Start attack**.

![Image](https://github.com/user-attachments/assets/26569459-2f2d-483a-9076-6a959233d053)
<br>

La combinación correcta es justo en la que no aparece el mensaje de error.

![Image](https://github.com/user-attachments/assets/b455dc85-eb33-4532-a9eb-c69f1d2aac5b)
<br>
