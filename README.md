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
## 🚀 Instrucciones de Instalación
## 📋 Requisitos Previos

* **Unreal Engine:** Versión 5.5
* **Plataforma:** Windows 64-bit
* **FMOD:** Integración requerida (ver instrucciones abajo).

## ⚠️ Instalación y Configuración de FMOD (Crítico)

Aunque el repositorio incluye las carpetas de los plugins de FMOD, es **necesario realizar una acción manual** para asegurar que los binarios se generen correctamente y el proyecto compile sin errores.

Las carpetas afectadas dentro de `Plugins/` son:
* `FMODStudio`
* `FMODStudioNiagara`
* `FMODStudioOpenXR`

Para solucionar esto, por favor elige **una** de las siguientes dos opciones:

### Opción A: Método Rápido (Cortar y Pegar)
Este método fuerza al motor a reconocer los archivos como "nuevos" y regenerar los binarios necesarios.

1.  Navega a la carpeta `Plugins` dentro del directorio del proyecto.
2.  Selecciona las tres carpetas mencionadas arriba (`FMODStudio`, `FMODStudioNiagara`, `FMODStudioOpenXR`).
3.  **Córtalas** (Ctrl+X) y pégalas temporalmente en tu Escritorio.
4.  Vuelve a **cortarlas** del Escritorio y **pégalas de nuevo** dentro de la carpeta `Plugins` del proyecto.
5.  Ejecuta el archivo `.uproject`.

### Opción B: Reinstalación Limpia (Recomendada)
Si la opción A no funciona, descarga e instala manualmente los plugins para asegurar la integridad de los archivos.

1.  Descarga el plugin oficial de FMOD. https://www.fmod.com/download#fmodforunreal
    * **Versión exacta:** `2.03.11`
    * **Motor:** Unreal Engine 5.5
    * **Plataforma:** Windows 64-bit
    * **Nombre del instalador:** `fmodstudio20311ue5.5win64`
2.  Descomprime el plugin.
3.  Copia las carpetas resultantes y **sobrescribe (machaca)** las carpetas existentes en el directorio `Plugins` de este proyecto.
4.  Al abrir el proyecto, permite que se recompilen los módulos si se solicita.

> **Nota:** Este paso es fundamental para que se generen los `.dll` y binarios correctos vinculados a tu instalación local de Unreal Engine.

## 📂 Estructura del Proyecto

Para facilitar la corrección, el proyecto sigue la siguiente estructura de carpetas:

```text
Actividad03AudioUnrealEngineFMOD/
├── Content/                # Contenido de Unreal Engine
├── Plugins/                # Contenido del plugin FMOD para la integración con UNREAL
├── Content/FMOD/           # Archivos generados por el plugin
├── Content/FMOD_Project/   # << PROYECTO DE FMOD STUDIO AQUÍ (Archivos fuente .fspro)
└── Actividad03.uproject    # Archivo principal del proyecto


