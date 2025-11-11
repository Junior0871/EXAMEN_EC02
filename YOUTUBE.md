2. [YouTube] Crea un conjunto de tres casos de prueba para el proceso de subida de video: (a) Flujo feliz: video válido subido correctamente. (b) Flujo alterno: error al subir por conexión inestable. (c) Flujo de error: archivo no compatible. Incluye resultados esperados y evidencias.
Respuesta:
----------------------------------------------------------------------
Flujo feliz
Identificador del caso de prueba	Cp_001
Nombre	Subir video valido.
Precondiciones	El archivo debe estar en un formato valido.
Entrada	Subir video
Pasos	1.	 Iniciar sesión.
2.	Subir video.
3.	Cargar video en formato “.mp4”
4.	Completar titulo y descripción.
Resultado Esperado	El video se sube correctamente.
Postcondiciones	El usuario debe estar con conexión a la red.
Estado	Iniciado
Prioridad	Bajo
--------------------------------------------------------------------
Flujo alterno:
Identificador del caso de prueba	Cp_002
Nombre	Error por conexión inestable
Precondiciones	Al subir video se debe demostrar instabilidad en la red.
Entrada	Subir video con conexión inestable.
Pasos	1.	Iniciar sesión.
2.	Seleccionar “Subir video”.
3.	Desconectar la red durante la subida 
Resultado Esperado	El descuento se aplica correctamente y la compra se finaliza sin errores.
Postcondiciones	Se verifica la existencia del cupón.
Estado	Iniciado
Prioridad	Alta
