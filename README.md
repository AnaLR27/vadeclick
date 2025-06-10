# 💊 VadeClick – Aplicación de Farmacología Clínica

**VadeClick** es una aplicación web desarrollada como Trabajo de Fin de Grado (TFG) orientada a facilitar la búsqueda y gestión de información sobre fármacos, principios activos, bacterias, fórmulas magistrales y usuarios. Permite a los usuarios buscar tratamientos, guardar favoritos, crear fórmulas personalizadas y gestionar su cuenta, todo a través de una interfaz intuitiva y moderna.

---

## 🧠 Funcionalidades principales

- 🔍 **Búsqueda por fármaco** y visualización de su ficha técnica.
- 🦠 **Búsqueda por bacterias** para encontrar principios activos eficaces y sus fármacos asociados, pudiendo descartar por resistencias.
- ⭐ **Favoritos personalizados** para cada usuario.
- 🧾 **Gestión de fórmulas magistrales** (ver, crear, editar, eliminar).
- 👤 **Autenticación y control de roles**: usuarios estándar y administradores.
- 🛡️ **Panel de administración** para gestionar usuarios (solo admin).

---

## 🖥️ Frontend – Angular

| Tecnología           | Descripción |
|----------------------|-------------|
| **Angular 17**       | SPA basada en componentes, estructura modular. |
| **RxJS**             | Observables para manejar estado reactivo (auth, roles, etc). |
| **Angular Material** | Componentes de interfaz modernos (formularios, toolbars, modales). |
| **SCSS**             | Estilos organizados con Sass. |
| **LocalStorage**     | Persistencia local del token y rol de usuario. |

> El frontend consume los endpoints REST del backend, usa guards para restringir rutas por rol y presenta una UX fluida y adaptada a distintos usuarios.

---

## 🔧 Backend – Node.js + Express

| Tecnología          | Descripción |
|---------------------|-------------|
| **Node.js & Express** | API REST modular, clara y mantenible. |
| **MySQL**            | Base de datos relacional con relaciones entre usuarios, fármacos, fórmulas, etc. |
| **bcrypt**           | Cifrado de contraseñas para máxima seguridad. |
| **JWT**              | Tokens seguros con información del usuario (ID y rol). |
| **Middlewares**      | Control de CORS, parsing de JSON, autenticación. |

> El backend expone rutas como `/api/auth`, `/api/farmacos`, `/api/bacterias`, `/api/users` con control de acceso y validación.

---


