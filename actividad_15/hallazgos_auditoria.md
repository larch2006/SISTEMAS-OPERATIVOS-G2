
# Actividad 3: Gestión de hallazgos de auditoría

## Objetivo
Elaborar no conformidades de seguridad de la información.

| Hallazgo | Evidencia | Riesgo | Recomendación |
|---|---|---|---|
| Contraseñas compartidas | Se identificó el uso de una misma cuenta por varios empleados (caso simulado). | Acceso no autorizado y falta de trazabilidad. | Asignar cuentas individuales y prohibir compartir contraseñas. |
| Archivos sensibles con permisos 777 | Los archivos sensibles presentan permisos rwxrwxrwx (caso simulado). | Cualquier usuario puede leer, modificar o ejecutar los archivos. | Aplicar permisos restrictivos, como chmod 640, según las necesidades de acceso. |
| Usuarios inactivos sin eliminar | Se identificaron cuentas de exempleados que permanecen habilitadas (caso simulado). | Accesos indebidos y posibles filtraciones de información. | Deshabilitar cuentas inactivas y revisar periódicamente los usuarios autorizados. |

## Conclusión
Los hallazgos evidencian riesgos relacionados con el control de acceso y la protección de la información. Se recomienda aplicar medidas correctivas y verificar posteriormente su cumplimiento.
