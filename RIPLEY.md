1. [Saga Ripley] Diseña un caso de prueba de REGRESIÓN para verificar que, tras una actualización del módulo de pagos, el flujo de compra con cupón de descuento sigue funcionando correctamente. Incluye: flujo feliz, flujo alterno (cupón expirado) y flujo de error (fallo en pasarela).
Respuesta:
-------------------------------------------------
	Flujo feliz:
Identificador del caso de prueba	Cp_001
Nombre	Verificar actualización de compra con cupón
Precondiciones	Debe estar implementado en el módulo de pagos
Entrada	Ingresar compra con cupón valido
Pasos	1.	Iniciar sesión.
2.	Agregar Producto al carrito
3.	Aplicar cupón valido “RIPLEY10”.
4.	Proceder al pago y completar la transacción. 
Resultado Esperado	El descuento se aplica correctamente y la compra se finaliza sin errores.
Postcondiciones	Se verifica la existencia del cupón.
Estado	Iniciado
Prioridad	Media
--------------------------------------------------
	Flujo alterno:
Identificador del caso de prueba	Cp_002
Nombre	Verificar compra con cupón expirado
Precondiciones	Debe estar implementado en el módulo de pagos
Entrada	Ingresar compra con cupón expirado
Pasos	1.	Iniciar sesión.
2.	Agregar Producto al carrito
3.	Aplicar cupón expirado “RIPLEY2024”.
Resultado Esperado	El sistema muestra el mensaje “Cupón expridado o no valido”.
No se aplica el descuento.
Postcondiciones	Se verifica que el descuento no aplicado a la compra.
Estado	Iniciado
Prioridad	Alta
----------------------------------------------------------------
	Flujo error:
Identificador del caso de prueba	Cp_003
Nombre	Verificar fallos en pasarela
Precondiciones	Debe estar localizado en el módulo de pagos
Entrada	Ingresar compras
Pasos	1.	Iniciar sesión.
2.	Agregar Producto al carrito
3.	Aplicar cupón valido “RIPLEY10”.
4.	Proceder al pago y simular error de pasarela. 
Resultado Esperado	El sistema muestra mensaje de error “Error en la transacción”. 
No se descuenta el cupon ni se genera el pedido.
Postcondiciones	-
Estado	Iniciado
Prioridad	Alta
