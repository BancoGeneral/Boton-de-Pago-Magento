#  Botón de Pago Yappy – Magento

##  Descripción
Botón de Pago Yappy es el checkout oficial de Banco General para Magento. Ofrezca Yappy como método de pago a más de 500 mil clientes y reciba pagos con Yappy directamente en su tienda.

Rápido, seguro y fácil de implementar en su sitio web.

## Documentación

Encuéntrala en [www.bgeneral.com](Https://www.bgeneral.com/desarrolladores)

## Requerimientos mínimos

PHP 7.2+

Magento 2.3+

Una cuenta jurídica con Yappy

Un certificado de SSL

## Instalación

Para esta instalación necesitará acceso a su servidor por medio de **SFTP** y **SSH**. Antes de iniciar, favor asegúrese que cuente con los accesos correctos. También recomendamos que previamente realice un respaldo de su tienda.

1. Descargue el archivo .zip desde este repositorio.
2. Por medio de SFTP, conéctese a la carpeta madre (root) de la instalación de Magento.
3. Suba el archivo **yappy-bg-para-magento.zip** a la carpeta **“root/app/code”**.

> ⚠️ Nota: En el caso de no tener la carpeta “code”, debe crearla manualmente.

4. Abra una terminal y conéctese por SSH. Navegue a la carpeta **“app/code”** en su instalación de Magento y descomprima el archivo **yappy-bg-para-magento.zip** utilizando el comando:

```PHP
unzip yappy-bg-para-magento.zip
```
![Visual del Botón de Pago Yappy](https://www.bgeneral.com/wp-content/uploads/2020/11/Magento%201-1200x553.png)

5. **Desde la carpeta root**, ejecute en la terminal los comandos descritos a continuación. Para asegurar una correcta instalación, ejecute los comandos **línea por línea** (espere la ejecución del comando anterior antes de continuar con el siguiente).

```PHP
php bin/magento setup:upgrade
```
```PHP
php bin/magento setup:static-content:deploy -f
```
```PHP
php bin/magento indexer:reindex
```
```PHP
php bin/magento cache:flush
```
6. Opcionalmente, puede borrar el archivo **yappy-bg-para-magento.zip**.

## Actualización
Para esta instalación necesitará acceso a su servidor por medio de **SFTP** y **SSH**. Antes de iniciar, favor asegúrese que cuente con los accesos correctos. También recomendamos que previamente realice un respaldo de su tienda.

1. Descomprima el archivo yappy-bg-para-magento.zip
2. Por medio de **SFTP**, conéctese a la carpeta madre (root) de la instalación de Magento.
3. Suba los archivos de Yappy a la carpeta **“root/app/code”** y sobra escriba los archivos.
4. **Desde la carpeta root**, ejecute en la terminal los comandos descritos a continuación. Para asegurar una correcta instalación, ejecute los comandos **línea por línea** (espere la ejecución del comando anterior antes de continuar con el siguiente).

```PHP
php bin/magento setup:upgrade
```
```PHP
php bin/magento setup:static-content:deploy -f
```
```PHP
php bin/magento indexer:reindex
```
```PHP
php bin/magento cache:flush
```

## Configuración
Luego de completar la instalación de la extensión, siga estos pasos para comenzar a utilizar el Botón de Pago Yappy:

1. Entre al panel de configuración de su tienda.
2. Seleccione **Stores** desde la barra de menú lateral y elija la opción **Configuration**.
3. En el nuevo menú de la izquierda, seleccione la categoría Sales. Luego, elija la opción de **Payment methods**. Se mostrarán todos los métodos de pago disponibles para su tienda.
4. En la sección de **Recommended solutions** se encontrará el Botón de Pago Yappy. Para comenzar con la configuración, haga clic en **Configure**.

![Visual del Botón de Pago Yappy](https://www.bgeneral.com/wp-content/uploads/2020/11/Magento%202.png)

5. Complete los campos de **ID del comercio** y **Clave secreta** con la información proporcionada en su Banca en Línea Comercial (Administración > Botón de Pago Yappy > Generar clave secreta). Su ID del comercio es un valor alfanúmerico de 32 caracteres.
6. En la opción de **Activar Botón de Pago**, seleccione **“Sí”**.

![Visual del Botón de Pago Yappy](https://www.bgeneral.com/wp-content/uploads/2020/11/Magento%203.png)

## Modo de pruebas
El modo de pruebas permite simular transacciones utilizando números de teléfono de prueba para visualizar el flujo de compra sin realizar un pedido real. Debe tener en cuenta que:
- El modo de pruebas **sólo funciona con los números de teléfono de pruebas** (se detallan a continuación).
- El modo de pruebas no descuenta inventario.
- Recuerde deshabilitar el modo de pruebas para aceptar transacciones reales.

| 6000-0000                | 6000-0002                |
|:------------------------:|:------------------------:|
| Transacciones realizadas | Transacciones canceladas |

![Visual del Botón de Pago Yappy](https://www.bgeneral.com/wp-content/uploads/2020/11/Magento%204.png)

## Funcionalidades extra
### Personalización del Botón de Pago Yappy
Opcionalmente, puede seleccionar el color del botón que se ajuste mejor al estilo de su tienda. Recomendamos la opción predeterminada.

![Brand (predeterminada)](https://www.bgeneral.com/wp-content/uploads/2020/10/Boton%20de%20pago%20woocommerce/brand.png)"Brand (predeterminada)"

![Dark](https://www.bgeneral.com/wp-content/uploads/2020/10/Boton%20de%20pago%20woocommerce/dark.png)"Dark"

![Light](https://www.bgeneral.com/wp-content/uploads/2020/10/Boton%20de%20pago%20woocommerce/light.png)"Light"

![White](https://www.bgeneral.com/wp-content/uploads/2020/10/Boton%20de%20pago%20woocommerce/white.png)"White"

### Método de pago por defecto
También puede habilitar Yappy como la opción de pago por defecto en su tienda (sin importar el orden de los métodos de pago instalados).
![Visual del Botón de Pago Yappy](https://www.bgeneral.com/wp-content/uploads/2020/11/magento%205.png)

## Preguntas frecuentes

**1. ¿El Botón de Pago Yappy funciona con el plugin X que modifica Magento?**

En general, el Botón de Pago Yappy funciona con cualquier extensión que funcione con Magento 2.3+. Sin embargo, no podemos certificar que funcione con todas las extensiones del mercado.

**2. Como comercio, ¿recibiré alguna notificación de las compras realizadas por Yappy?**

Sí. Cada vez que se realice una compra por Yappy, recibirá un correo de confirmación con el número de pedido de Magento, el monto y la hora de la transacción.

**3. ¿Dónde puedo conseguir mis credenciales para el Botón de Pago Yappy?**

Sus credenciales las puede conseguir en Banca en Línea Comercial. Siga este enlace para verificar los pasos de generación de credenciales.

**4.¿Para qué países está disponible Yappy?**

El Botón de Pago solo está disponible para Panamá.

**5.¿Cómo se manejan los pedidos con el Botón de Pago Yappy?**

La extensión maneja 3 estados de pedidos:

1. **Pendiente de pago:** El cliente hizo clic en el botón de “Paga con Yappy” y se está a la espera de que confirme la compra en el *app* de Banco General.
2. **Cancelado:** El cliente inició el proceso, pero canceló el pedido en el *app* de Banco General.
3. **Procesado:** El cliente confirmó la compra en el *app* de Banco General y el pago se ejecutó. Si se maneja inventario, el mismo se descontará.

**6. Veo un mensaje que dice “Algo salió mal, contacta al administrador.” ¿Qué debo hacer?**
- Asegúrese de que su sitio web cumple con los requerimientos mínimos.
- Revise que cuenta con la versión más reciente del módulo.
- Confirme que sus credenciales son correctas y que fueron colocadas en los campos correspondientes.
- Confirmar que el URL de su tienda está registrado correctamente en el perfil de su Botón de Pago Yappy en Banca en Línea Comercial.

**7. ¿Dónde puedo ver reportes de ventas de mi Botón de Pago Yappy?**

Las ventas del Botón de Pago se verán reflejadas en su Banca en Línea Comercial. Acceda a las mismas desde Reportes > Reportes Yappy.

## Resolución de problemas

¿Tiene algún problema? Siga estos pasos para asegurar la correcta configuración de la extensión:
- Asegúrese que su sitio cumple con los requerimientos mínimos.
- Revise que cuenta con la versión más reciente del módulo.
- Revise las preguntas frecuentes por si su pregunta se ve reflejada en las mismas.
- Confirme que sus credenciales son correctas y que fueron colocadas en los campos correspondientes.
- Confirme que no está habilitado el modo de pruebas (sandbox).
- Revise que el dominio de su tienda (URL) sea igual al que definió en su perfil de Botón de Pago en Banca en Línea Comercial, ya que se utilizará para validar la solicitud.

## ¿Tiene alguna pregunta?
Consulte nuestra sección de Preguntas Frecuentes o de Resolución de problemas para resolver los inconvenientes más comunes. Si requiere mayor soporte, comuníquese con nosotros por correo electrónico a botondepagoyappy@bgeneral.com.
