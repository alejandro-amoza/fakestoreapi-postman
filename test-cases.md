# Test Cases – Fake Store API

## 1. Login de usuario  
**Método:** POST  
**Endpoint:** `/auth/login`  
**Datos de entrada:** email y password  
**Verificaciones:**  
- Status code 201  
- Se recibe un token en la respuesta (`access_token`)  
- Se almacena en variable de entorno (`accessToken`)  

---

## 2. Obtener información del usuario logueado  
**Método:** GET  
**Endpoint:** `/auth/profile`
**Headers:** Authorization: Bearer {{accessToken}}  
**Verificaciones:**  
- Status code 200  
- El email de la respuesta coincide con la variable de entorno `email`  

---

## 3. Listar productos  
**Método:** GET  
**Endpoint:** `/products`  
**Headers:** Authorization: Bearer {{accessToken}} 
**Verificaciones:**  
- Status code 200  
- La respuesta es un array  
- El array contiene al menos un producto  
- El primer producto tiene las propiedades con tipos correctos:  
  - `id` (number)  
  - `title` (string)  
  - `price` (number)  
  - `description` (string)  
  - `category` (object)  
  - `images` (array)  
- Todos los productos tienen las propiedades mencionadas arriba  
- Se guarda el id del primer producto en variable de entorno `productId`  

---

## 4. Crear producto  
**Método:** POST  
**Endpoint:** `/products`  
**Headers:** Authorization: Bearer {{accessToken}}  
**Body:** JSON con datos del producto  
**Verificaciones:**  
- Status code 201  
- El producto creado tiene el título esperado (ejemplo: "Test QA New product")  
- Se guarda el id del producto creado en variable de entorno `productId`  

---

## 5. Actualizar producto  
**Método:** PUT  
**Endpoint:** `/products/{{productId}}`  
**Headers:** Authorization: Bearer {{accessToken}}  
**Body:** JSON con datos actualizados  
**Verificaciones:**  
- Status code 200  
- El producto actualizado tiene los datos esperados (ejemplo: título "Producto actualizado QA" y precio 50000)  

---

## 6. Eliminar producto  
**Método:** DELETE  
**Endpoint:** `/products/{{productId}}`  
**Headers:** Authorization: Bearer {{accessToken}}  
**Verificaciones:**  
- Status code 200  
- El cuerpo de la respuesta está vacío (0)  
