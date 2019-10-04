# mesa-de-calibracion
Interfaz para controlar el estatus de la calibración de los fixtures. Con conexión al indusoft de la línea.

Pasos en pantalla local:
1. Realizar escaneo de QR o código de barras en el fixture. Se envía la señal del modelo a calibrar al PLC. 
2. En el PLC se detectan los sensores y se cambia el estatus de la calibración de ese modelo. Se despliegan alertas en caso de que falte algún sensor por colocar.
3. Se cambia el estatus a verde si todos los sensores se colocaron de forma correcta. 
4. Se envía el resultado al paso de Indusoft para que continue el proceso.

Pasos en la pantalla de Indusoft:
1. Se llega al paso de validación de calibración de fixture se compara el modelo corriendo contra el estatus del fixture correspondiente.
2. Si es bueno sigue al siguiente paso, si es malo, se queda ahí hasta que se realice la calibración.
