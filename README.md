# 🔊 Actividad 03: Implementación de Audio en Unreal Engine y FMOD

![Unreal Engine](https://img.shields.io/badge/Unreal_Engine-5.5.4-black?style=for-the-badge&logo=unrealengine)
![FMOD Studio](https://img.shields.io/badge/FMOD_Studio-2.03.11-black?style=for-the-badge&logo=fmod)
![Status](https://img.shields.io/badge/Status-Completado-green?style=for-the-badge)

Este repositorio contiene la entrega de la **Actividad de Laboratorio 03** para la asignatura de *Sonido y Música*. El proyecto demuestra la implementación de un sistema de audio dinámico e inmersivo utilizando **FMOD Studio** como middleware integrado en **Unreal Engine 5**.

---

## 🎓 Información del Estudiante

| Campo | Detalle |
| :--- | :--- |
| **Estudiante** | Guillem Muñoz Pueyo |
| **Asignatura** | Sonido y Música |
| **Grado** | Diseño y Desarrollo de Videojuegos |
| **Universidad** | Universidad Internacional de La Rioja (UNIR) |
| **Curso Académico** | 2025 - 2026 |

---

## 📺 Demo y Explicación

Puedes ver el funcionamiento del sistema de audio y la explicación técnica de la implementación en el siguiente video:

[![Ver Video en YouTube](https://img.youtube.com/vi/G3JsEv-6w0g/maxresdefault.jpg)](https://www.youtube.com/watch?v=G3JsEv-6w0g)

> **[Haz clic aquí para ver el video completo en YouTube](https://www.youtube.com/watch?v=G3JsEv-6w0g)**

---

## 🛠️ Características de la Implementación

El proyecto se centra en la creación de un paisaje sonoro reactivo en un entorno de tercera persona, abarcando las siguientes áreas:

### 1. Integración de Middleware (FMOD + UE5)
- Configuración y validación del plugin de FMOD en Unreal Engine 5.5.4.
- Comunicación bidireccional mediante **Blueprints** para la llamada de eventos.

### 2. Personaje (Foley)
- **Sistema de Pasos:** Implementación de eventos de pasos sincronizados con la animación del personaje.
- **Modulación:** Variación aleatoria de `Pitch` (tono) y `Volume` en FMOD para evitar la repetición mecánica y dar realismo ("Machine Gun Effect").

### 3. Ambiente y Espacialización
- **Sonido 3D:** Emisores de sonido posicionados en el mapa con curvas de atenuación personalizadas.
- **Ambiente Dinámico:** Loops de fondo (viento/atmósfera) que dan contexto al nivel.

### 4. Interacción
- Eventos sonoros disparados por *Triggers* o acciones específicas del jugador dentro del nivel.

---

## 📂 Estructura del Proyecto

Para facilitar la corrección, el proyecto sigue la siguiente estructura de carpetas:

```text
Actividad03AudioUnrealEngineFMOD/
├── Content/                # Contenido de Unreal Engine
├── FMOD/                   # Archivos generados por el plugin
├── FMOD_Project/           # << PROYECTO DE FMOD STUDIO AQUÍ (Archivos fuente .fspro)
├── Source/                 # Código fuente (si aplica)
└── Actividad03.uproject    # Archivo principal del proyecto
