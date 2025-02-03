# **Instalación de Precheckout en TKA**

Sigue estos pasos para integrar la funcionalidad de precheckout en tu tienda.

---

## **Pasos de Instalación**

### 1. Acceder a Partners de TKA
1. Inicia sesión en tu cuenta de **TKA Partners**.
2. Navega hasta el panel de control de la **tienda del cliente**.

### 2. Duplicar el Tema Actual
1. Dirígete a **Canales de venta > Tienda Online**.
2. En la sección **Temas**, localiza el tema activo.
3. Haz clic en los **tres puntos (···)** junto al tema y selecciona **Duplicar**.

### 3. Editar el Código del Tema
1. En la copia del tema, haz clic en **··· > Editar código**.

### 4. Crear el Snippet "cart-precheckout"
1. En la carpeta `Snippets`, haz clic en **Agregar un snippet nuevo**.
2. Nómbralo `cart-precheckout.liquid`.
3. Copia el código de `cart-precheckout.liquid` y pégalo en el snippet.
4. Guarda los cambios.

### 5. Modificar la Plantilla del Carrito
1. Ubica el archivo del carrito (`static-cart.liquid`, `main-cart.liquid` o `cart-template.liquid`).
2. **Al final del archivo**, inserta:
   ```liquid
   {% render 'cart-precheckout' ... %}
   ```
3. Guarda los cambios.

### 6. Habilitar el Tipo de Contenido "Precheckout"
1. En `main-cart.liquid`, añade `"precheckout"` en los tipos de contenido:
   ```liquid
   "blocks": [
     ...
     {
       "type": "precheckout",
       "name": "Precheckout"
       "limit": 1,
       "settings": [
            ...
       ]
       ....
     }
   ]
   ```

### 7. Publicar Cambios
1. Publica el tema modificado desde **Temas > Acciones > Publicar**.
2. Verifica el funcionamiento en la página del carrito.

---

## **Notas Importantes**
✅ Realiza pruebas en un entorno de staging antes de publicar.
📁 Si no encuentras los archivos, consulta la documentación de tu tema.
🔧 Soporte técnico: contact@tka.com.
