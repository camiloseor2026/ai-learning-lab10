# Plantilla Maestra de Briefs para IA

## Título de la tarea
Describe en una frase corta qué se necesita construir, corregir o mejorar.

**Ejemplo:**  
Implementar un endpoint en FastAPI para registrar usuarios.

---

## Contexto
Explica el entorno y el problema antes de pedir la solución.

Incluye:
- sistema actual o entorno
- problema que se intenta resolver
- objetivo concreto de la tarea

**Plantilla:**
- **Sistema actual:**  
- **Problema:**  
- **Objetivo:**  

**Ejemplo:**  
- **Sistema actual:** Existe una API en FastAPI con autenticación básica y conexión a PostgreSQL.  
- **Problema:** Actualmente no existe un endpoint para registrar nuevos usuarios.  
- **Objetivo:** Crear un endpoint seguro para registrar usuarios con validación y persistencia en base de datos.

---

## Requerimientos técnicos
Define cómo debe implementarse la solución.

Incluye:
- lenguaje
- framework
- arquitectura o patrones
- input/output esperado
- integraciones necesarias

**Plantilla:**
- **Lenguaje:**  
- **Framework:**  
- **Patrones/arquitectura:**  
- **Input esperado:**  
- **Output esperado:**  
- **Integraciones:**  

**Ejemplo:**  
- **Lenguaje:** Python 3.11  
- **Framework:** FastAPI  
- **Patrones/arquitectura:** separación en router, service y repository  
- **Input esperado:** nombre, email y password  
- **Output esperado:** id del usuario y mensaje de éxito  
- **Integraciones:** PostgreSQL usando SQLAlchemy

---

## Constraints
Indica reglas, límites y estándares que la IA debe respetar.

**Plantilla:**
- usar type hints
- incluir tests automatizados
- cumplir linter del proyecto
- no usar librerías externas no autorizadas
- no modificar archivos fuera del alcance de la tarea

**Ejemplo:**  
- Todo el código debe incluir type hints.  
- Deben agregarse tests unitarios.  
- No se permite usar librerías externas distintas a las ya aprobadas.  
- La solución debe seguir la arquitectura actual del proyecto.  
- No deben exponerse credenciales ni datos sensibles.

---

## Definition of Done
Define criterios verificables para considerar la tarea terminada.

**Plantilla:**
- funcionalidad implementada
- tests pasando
- formato de salida correcto
- performance o validaciones mínimas cumplidas
- documentación mínima actualizada si aplica

**Ejemplo:**  
- El endpoint permite registrar usuarios válidos.  
- Los usuarios duplicados son rechazados correctamente.  
- Los tests unitarios pasan.  
- El linter no reporta errores.  
- La respuesta JSON cumple el formato esperado.

---

## Instrucción final para la IA
Usa esta tarea para pedirle a la IA que implemente la solución con base en lo anterior.

**Ejemplo:**  
Con base en este brief, implementa la solución completa respetando los requerimientos técnicos, constraints y Definition of Done. Explica decisiones importantes y añade tests.