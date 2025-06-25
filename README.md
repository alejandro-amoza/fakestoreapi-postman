# 🧪 DummyJSON API Testing (Postman)

Este proyecto contiene una colección de pruebas API usando Postman para la API pública [Fake Store API](https://fakestoreapi.com/), Cubre operaciones CRUD sobre productos, con autenticación de usuario y tests automatizados.

---

## 📦 Contenido

- Login de usuario (`/auth/login`)
- Listado de productos (`/products`)
- Detalle por ID (`/products/:id`)
- Crear producto (`POST /products`)
- Actualizar producto (`PUT /products/:id`)
- Eliminar producto (`DELETE /products/:id`)

---

## 🔐 Autenticación
Se realiza un login con credenciales válidas y se obtiene un token, usado luego en endpoints protegidos mediante el header:


---

## 📦 Endpoints testeados

- `POST /api/v1/auth/logi`
- `GET /api/v1/auth/profile`
- `GET /api/v1/products`
- `POST /api/v1/products`
- `PUT /api/v1/products/:id`
- `DELETE /api/v1/products/:id`

📄 Diseños de los CP disponibles en:
https://drive.google.com/drive/folders/1C00yOygsRSXHbVRoUy82-2ilcbkadbgH?usp=drive_link

---

## 📁 Estructura del proyecto

- `collections/`: colección principal exportada desde Postman
- `environments/`: archivo de entorno con variables usadas
- `docs/`: capturas de pantalla de las pruebas
- `test-cases.md`: documento con casos de prueba

---

## 🧪 Tests automáticos

Cada request contiene scripts en Postman para validar:
- Códigos de estado HTTP
- Datos esperados en las respuestas
- Almacenamiento de variables para uso encadenado

---

## 🚀 Cómo usar

1. Cloná este repo.
2. Importá la colección y el entorno en Postman.
3. Iniciá con el request de login.
4. Ejecutá las pruebas manualmente o con Collection Runner.

---

## 📎 Fuente de la API

> https://fakestoreapi.com/docs


---

## 🙌 Autor
Alejandro Amoza – QA Tester
 [LinkedIn](https://www.linkedin.com/in/alejandro-amoza)
 [Portfolio](https://alejandro-amoza.github.io/portfolio)
