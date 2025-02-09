# 🏋️‍♂️ Aplicación para Entrenadores Personales

## 📌 Introducción

En este proyecto, hemos desarrollado una aplicación móvil diseñada para ayudar a los entrenadores personales a gestionar sus clientes de manera eficiente. La aplicación permite crear planes de entrenamiento personalizados, realizar un seguimiento detallado de las sesiones y enviar recordatorios automáticos, todo con el objetivo de facilitar la gestión de entrenamientos y mejorar el rendimiento de los clientes.

---

## 🎯 Objetivos

- 📊 **Gestionar el progreso de los clientes** de manera eficiente.
- 🏋️ **Crear y asignar planes de entrenamiento personalizados** según objetivos individuales.
- 🔔 **Implementar notificaciones y recordatorios automáticos** para sesiones de entrenamiento.
- 📅 **Ofrecer herramientas de seguimiento** para mejorar el rendimiento de los clientes.

---

## 📌 Características Principales

- ✅ Interfaz intuitiva y fácil de usar.
- ✅ Base de datos para almacenar información de clientes y entrenamientos.
- ✅ Sistema de notificaciones automáticas.
- ✅ Informes y estadísticas de progreso.
- ✅ Soporte para múltiples dispositivos.

---

## 📊 Tecnologías Utilizadas

| Tecnología | Uso |
|------------|-----|
| ![Android Studio](https://img.shields.io/badge/Android-3DDC84?style=flat&logo=android&logoColor=white) | Entorno de desarrollo |
| ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white) | Lenguaje de programación |
| ![SQL Developer](https://img.shields.io/badge/SQL_Developer-0066CC?style=flat&logo=oracle&logoColor=white) | Gestión de bases de datos |
| ![Figma](https://img.shields.io/badge/Figma-F24E1E?style=flat&logo=figma&logoColor=white) | Diseño de interfaz |

---

## 🔄 Flujo de la Aplicación

```mermaid
flowchart TD
    A[Inicio] --> B[Iniciar Sesión]
    B --> C{Seleccionar Tipo de Usuario}
    C -->|Entrenador| D[Panel de Gestión]
    C -->|Cliente| E[Panel de Entrenamiento]
    D --> F[Crear Planes de Entrenamiento]
    D --> G[Gestionar Clientes]
    D --> H[Configurar Recordatorios]
    E --> I[Ver Progreso]
    E --> J[Recibir Notificaciones]
    E --> K[Mis Entrenamientos]
```



## 📆 Planificación (Diagrama Gantt)

```mermaid
gantt
title Desarrollo de la App
    dateFormat YYYY-MM-DD
    section Investigación
    Estudio de necesidades :done, 02-01, 02-15
    Consulta con entrenadores  :active, 02-16, 02-28
    section Diseño y Desarrollo
    Creación de interfaz   :active, 03-01, 03-15
    Implementación base de datos :active, 03-16, 04-01
    Desarrollo de funcionalidades :active, 04-02, 05-01
    Pruebas de usuario     : 05-02, 05-15
    Documentación         : 05-16, 05-30
```

## 🐙 Planificación (Diagrama Git)
```mermaid
gitGraph
    commit id: "Configuración inicial"
    branch dev
    commit id: "Desarrollo de Interfaz"
    checkout main
    commit id: "Commit en main"
    merge dev
    commit id: "Merge de dev a main"
    branch bugfix
    commit id: "Error en RecyclerView"
    checkout dev
    commit id: "Implementación BBDD" tag: "v1.0.0"
    merge bugfix
    checkout dev
    commit id: "Desarrollar Funcionalidades" tag: "v1.2.0"
    checkout main
    merge dev
    commit id: "Merge de dev a main"
    commit id: "Versión 2.0.0" tag: "v2.0.0"
```



## 📜 Diagrama de Entidad-Relación

```mermaid
erDiagram
    ENTRENADOR {
        string id
        string nombre
        string email
    }
    CLIENTE {
        string id
        string nombre
        string edad
        string peso
        string altura
    }
    PLAN_ENTRENAMIENTO {
        string id
        string nombre
        string descripcion
    }
    SESION {
        string id
        date fecha
    }
    ENTRENADOR ||--o{ CLIENTE : "entrena"
    CLIENTE ||--o{ PLAN_ENTRENAMIENTO : "sigue"
    PLAN_ENTRENAMIENTO ||--o{ SESION : "incluye"
```

---

## 📜 Diagrama de Secuencia

```mermaid
sequenceDiagram
    participant Entrenador
    participant Sistema
    participant Cliente
    Entrenador->>Sistema: Crear Plan de Entrenamiento
    Sistema-->>Entrenador: Confirmación de Creación
    Cliente->>Sistema: Ver Plan Asignado
    Sistema-->>Cliente: Mostrar Rutina
    Cliente->>Sistema: Registrar Entrenamiento Realizado
    Sistema-->>Entrenador: Notificación de Progreso
```

## 📜 Diagrama de Requerimientos
```mermaid

requirementDiagram
    requirement R1 {
        id: 1
        text: "La aplicación debe permitir a los entrenadores crear planes de entrenamiento."
    }
    requirement R2 {
        id: 2
        text: "Los entrenadores deben poder asignar planes a los clientes."
    }
    requirement R3 {
        id: 3
        text: "Los clientes deben poder registrar sus entrenamientos."
    }
    requirement R4 {
        id: 4
        text: "El sistema debe enviar notificaciones automáticas."
    }
    requirement R5 {
        id: 5
        text: "Los entrenadores deben poder seguir el progreso de sus clientes."
    }

```

## 📜 Diagrama de Journey
```mermaid
journey
    title Uso de la Aplicación
    section Inicio
        Abrir la aplicación: 5: Ambos
        Iniciar sesión: 4: Ambos
    section Interacción
        Crear Plan de Entrenamiento: 5: Entrenador
        Asignar Plan: 4: Entrenador
        Ver Plan Asignado: 4: Usuario
        Registrar Entrenamiento: 3: Usuario
    section Administración (Entrenador)
        Ver progreso de clientes: 5: Entrenador
        Ajustar Plan: 4: Entrenador
```

#### 🧠 Importancia del seguimiento en el rendimiento deportivo
Los entrenadores deben contar con herramientas eficaces para monitorear el progreso de sus clientes. La capacidad de medir estadísticas físicas y mentales de estos a lo largo del tiempo permite optimizar las estrategias de entrenamiento, prevenir lesiones y ajustar la intensidad del entrenamiento según sea necesario.

---

## 📹 Video Demostrativo


#### Deporte 🏋️‍♂️ y salud mental 🧠
[![Video Presentación](https://img.youtube.com/vi/GImwhD8l4Ho/0.jpg)](https://www.youtube.com/watch?v=GImwhD8l4Ho "Ver Video")

---


## 📩 Contacto

📧 Correo: [raniakacemi@gmail.com](mailto:raniakacemi@gmail.com)  
📌 GitHub: [github.com/Ranius7](https://github.com/Ranius7)  

---


🌟 ¡Espero que esta aplicación ayude a muchos entrenadores personales a mejorar su trabajo y a ofrecer un mejor servicio a sus clientes! 💪
