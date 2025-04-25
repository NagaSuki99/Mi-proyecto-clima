
# CORRECCION.md

## 1. ¿Qué mala práctica identificaste?
Se identificó una variable CSS duplicada en el archivo `index.css`:
```css
--color-primary: #3498db;
--color-info: #3498db;
```
Ambas variables almacenaban el mismo valor hexadecimal para un color, lo cual es redundante.

Además, el archivo tenía una escasa cantidad de comentarios explicativos en bloques de código clave.

---

## 2. ¿Por qué es considerada una mala práctica?
- **Variables duplicadas:** Tener variables CSS con el mismo valor sin una justificación clara puede generar confusión, mantenimiento innecesario y riesgo de inconsistencias si se actualiza solo una.
- **Falta de comentarios:** La ausencia de documentación dificulta la comprensión del código por parte de otros desarrolladores o incluso por el autor después de un tiempo.

---

## 3. ¿Cómo la solucionaste?
- Se eliminó la línea con `--color-info: #3498db;` dejando únicamente `--color-primary`, ya que ambas tenían el mismo valor.
- Se agregaron comentarios explicativos en secciones clave del código CSS como:
  - `.weather-card__temp` para explicar que representa la temperatura principal.
  - `.weather-detail__value` para describir el propósito del valor visual del detalle del clima.

---

## 4. ¿Qué beneficios aporta tu solución?
- **Claridad:** El código es más fácil de entender y mantener.
- **Eficiencia:** Se reduce la redundancia y se evita la confusión entre variables con el mismo valor.
- **Escalabilidad:** Un CSS más limpio y bien documentado facilita futuras modificaciones, colaboraciones o migraciones a entornos más complejos.
