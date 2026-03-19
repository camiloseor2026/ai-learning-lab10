# Protocolo de Review para Código Generado por IA

Antes de hacer commit, revisar estos 5 puntos críticos.

---

## 1. Validación de librerías y dependencias
**Pregunta clave:**  
¿Los imports, librerías y funciones usadas realmente existen y son compatibles con el entorno?

**Qué revisar:**
- que cada import exista
- que la librería sea real, mantenida y segura
- que sea compatible con la versión del lenguaje o framework
- que no se hayan inventado métodos o módulos

**Cómo detectarlo:**
- revisar documentación oficial
- revisar repositorio del paquete
- correr el proyecto o tests
- validar instalación en el entorno

---

## 2. Revisión de lógica de negocio
**Pregunta clave:**  
¿La solución respeta correctamente las reglas del problema y los casos edge?

**Qué revisar:**
- fórmulas críticas
- redondeos o acumulaciones
- validaciones de negocio
- casos límite
- manejo de errores funcionales

**Ejemplos comunes:**
- uso incorrecto de floats para dinero
- comparaciones defectuosas
- errores en cálculos acumulativos
- reglas incompletas para estados o excepciones

---

## 3. Revisión de seguridad
**Pregunta clave:**  
¿El código generado es funcional pero inseguro?

**Qué revisar:**
- inputs sin validación
- posibles inyecciones SQL
- credenciales expuestas
- autenticación/autorización mal implementada
- logs con datos sensibles
- sanitización insuficiente

**Señales de alerta:**
- queries armadas con strings
- secretos hardcodeados
- ausencia de validación en endpoints
- respuestas con información sensible

---

## 4. Verificación de contexto y cumplimiento del brief
**Pregunta clave:**  
¿La IA respetó realmente el brief completo o olvidó restricciones importantes?

**Qué revisar:**
- requerimientos técnicos solicitados
- constraints definidos
- estructura esperada
- librerías permitidas
- formato de input/output solicitado
- alcance real de la tarea

**Señales de pérdida de contexto:**
- usa herramientas no permitidas
- modifica archivos fuera del alcance
- cambia arquitectura sin justificación
- entrega algo funcional pero distinto a lo pedido

---

## 5. Chequeo personalizado según mi stack
**Pregunta clave:**  
¿La solución cumple con los estándares específicos de mi entorno técnico?

**Qué revisar:**
- que los tests nuevos corran correctamente
- que el código respete la arquitectura del proyecto
- que no registre datos sensibles en logs
- que cumpla estándares de naming y linting
- que sea mantenible y legible por el equipo

**Personalización sugerida:**
Agrega aquí reglas propias de tu stack, por ejemplo:
- compatibilidad con FastAPI
- type hints obligatorios
- pytest obligatorio
- separación por capas
- cobertura mínima de tests

---

## Checklist rápida antes de commit
- [ ] Los imports y librerías existen
- [ ] La lógica de negocio fue validada
- [ ] No hay riesgos obvios de seguridad
- [ ] Se respetaron todos los constraints del brief
- [ ] Cumple con los estándares de mi stack