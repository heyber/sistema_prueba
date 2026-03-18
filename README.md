# 🚀 Gserucó App

Proyecto base para desarrollo de aplicaciones web usando **Next.js + Prisma + PostgreSQL + Docker**.

Este repositorio funciona como **plantilla inicial** para futuros proyectos.

---

## 🧱 Stack Tecnológico

* **Next.js (App Router)**
* **React**
* **Tailwind CSS**
* **Prisma ORM**
* **PostgreSQL**
* **Docker & Docker Compose**

---

## ⚙️ Arquitectura

El proyecto está dividido en:

* `/app` → Frontend (páginas y UI)
* `/app/api` → Backend (API routes)
* `prisma/` → Esquema y configuración de base de datos
* `docker-compose.yml` → Orquestación de servicios

---

## 🐳 Entorno con Docker

El proyecto corre con 2 servicios:

* `app` → aplicación Next.js
* `db` → base de datos PostgreSQL

### 🔌 Conexión a la base de datos

```env
DATABASE_URL="postgresql://postgres:postgres@db:5432/mydb"
```

---

## 🚀 Cómo iniciar el proyecto

### 1. Construir y levantar contenedores

```bash
docker-compose up --build
```

---

### 2. Generar cliente Prisma (IMPORTANTE)

```bash
docker exec -it trabajosss-app-1 sh
npx prisma generate
npx prisma db push
```

---

### 3. Abrir en el navegador

```
http://localhost:3000
```

---

## 🔐 Funcionalidades actuales

* ✅ Registro de usuarios
* ✅ Login con validación en base de datos
* ✅ Redirección a dashboard
* ✅ Persistencia básica con localStorage
* ✅ Dashboard con mensaje de bienvenida

---

## 🖥️ Estructura de rutas

| Ruta            | Descripción         |
| --------------- | ------------------- |
| `/`             | Landing page        |
| `/login`        | Inicio de sesión    |
| `/register`     | Registro de usuario |
| `/dashboard`    | Panel principal     |
| `/api/login`    | API login           |
| `/api/register` | API registro        |

---

## 🧩 Prisma

Ejemplo de modelo actual:

```prisma
model User {
  id       Int    @id @default(autoincrement())
  email    String @unique
  password String
}
```

---

## 🎯 Objetivo del proyecto

Este proyecto sirve como base para:

* Crear aplicaciones rápidamente
* Probar integraciones con base de datos
* Implementar autenticación
* Escalar hacia arquitecturas más completas

---

## ⚠️ Estado actual

* Proyecto en desarrollo
* Seguridad básica (sin hashing ni JWT aún)
* Uso enfocado a aprendizaje y prototipos

---

## 🔮 Próximos pasos

* 🔐 Autenticación segura (JWT / cookies)
* 🔑 Encriptación de contraseñas
* 🧠 Manejo de sesiones real
* 🎨 Mejora de UI/UX
* 🛡️ Protección de rutas

---

## 🧠 Nota para desarrolladores / IA

Este proyecto:

* Corre completamente en Docker
* Usa Prisma como ORM
* No utiliza librerías de autenticación externas
* Prioriza simplicidad sobre complejidad

Se espera:

* Código claro
* Soluciones prácticas
* Evitar sobreingeniería

---

## 📦 Deploy

Para producción se recomienda:

* Configurar variables de entorno reales
* Usar base de datos externa
* Implementar seguridad adecuada

---

## 🤝 Contribución

Este proyecto está diseñado como plantilla personal, pero puede adaptarse a otros casos de uso fácilmente.

---

## 📌 Autor

Proyecto desarrollado como base reutilizable para futuros desarrollos.
