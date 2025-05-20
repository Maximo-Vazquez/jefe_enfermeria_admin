# Requerimientos y Mejoras - Gestión de Medicamentos

## Gestión de Medicamentos

- La ubicación de los medicamentos está determinada por una composición de A1 (considerar que es suficiente).
- Según la estructura actual, un medicamento solo puede estar en una ubicación particular (considerar que es suficiente).
- Permitir al jefe de enfermería modificar o eliminar un ajuste de stock realizado. (Evaluar)

---

## Inventario de Medicamentos

- Cambiar el botón **"Detalles"** por **"Gestión"**.
- Redireccionar al HTML de gestión de medicamentos correspondiente.

---

## Registrar Medicamento

- Eliminar el campo **"Fecha de vencimiento"** del formulario. puesto que el vencimiento estara dadao por el lote en el que se compro. 
n
---

## Tratamientos Médicos

- Cambiar el input de texto de **diagnóstico(s) principal(es)** por registros seleccionables de diagnósticos.
  - Esto permite una mejor gestión, análisis y detalle de los diagnósticos que tiene un paciente, en lugar de un texto plano.
- El campo **"notas_generales"** desaparecería, ya que las notas del tratamiento estarían asociadas a cada diagnóstico (una nota por diagnóstico).
- Modificar completamente los campos de medicación asociados al tratamiento:
  - Separar los datos en campos distintos: por ejemplo, "Paracetamol 500mg" debería dividirse en:
    - Medicamento: `"Paracetamol"`
    - medida: `"500mg"`
  - Usar selectores o campos con autocompletado para:
    - Medicamento
    - Dosis
    - Frecuencia (por ejemplo: cada 1, 8, 12 horas, etc.)
    - y demas campos
  - Lo ideal es que todos los campos sean seleccionables o con buscador, para evitar errores de carga. (ya que todo esos campos ya se los tiene cargado de ante mano)

---

## Historial de Medicación

- Evaluar si se mantiene o se elimina la opción de **"Exportar historial de medicación"**.

---

## Alerta de Stock

- Agregar una sección para configurar:
  - Frecuencia de las alertas
  - Otras configuraciones específicas de las alertas de stock (que consideren)

---

## Nueva Vista: Historia Médica

- Crear una nueva interfaz de usuario: **historia médica**.
- Debe ser accesible desde `TR-tratamiento.html` → **Historia médica** → `historia_medica.html`.
- Debe cumplir con los siguientes requisitos funcionales: 
    RF3.4.3 El sistema desplegará la opción de ver el historial médico del residente entre sus datos. (tiene falta redirecicon a historial medico.)
    RF3.4.4 El sistema desplegará una lista con el historial médico completo del residente.  falta
  (y otros que se consideren)

---

## Login

- Autenticación clásica con usuario y contraseña.
- No se puede cambiar la contraseña por cuenta propia.
- No se permite recuperación de contraseña por correo electrónico.

---

## General

- Corregir los estilos rotos en los inputs de texto de los buscadores .
- Eliminar del buscador horizontal (sidebar) las siguientes secciones:
  - Informe de uso semanal
  - Medicamentos administrados
  - Actualizar tratamiento (se accede por residente, no debería estar en el sidebar)
  - Historial de medicación (se accede por residente, no debería estar en el sidebar)

---

## Autorizaciones

### Gestión de Medicamentos

- El jefe de enfermería solo puede actualizar el stock a la baja, es decir:
  - Marcar que un medicamento de un lote determinado se utilizó pero no se registró correctamente.
  - Restar stock por pérdida.
- Las altas y correcciones de stock se realizan únicamente desde el área de compras, que registra los movimientos en la plataforma.
