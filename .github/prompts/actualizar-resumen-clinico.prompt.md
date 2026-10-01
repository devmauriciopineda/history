---
name: "Actualizar resumen clínico"
description: "Actualiza summary.md con nueva evidencia clínica sin inventar datos ni modificar información no respaldada"
argument-hint: "Pega o adjunta la nueva historia clínica, consulta, resultado de prueba u otra evidencia médica"
agent: "agent"
---
Actualiza el resumen clínico del proyecto usando exclusivamente la nueva evidencia proporcionada en esta solicitud.

## Archivos

- Lee primero [summary.md](../../summary.md), si existe.
- Guarda el resultado final en [summary.md](../../summary.md).
- Si `summary.md` no existe, créalo con la estructura indicada abajo.

## Reglas de actualización

1. Conserva la información existente que no sea afectada por la nueva evidencia.
2. Agrega o modifica únicamente datos respaldados explícitamente por la nueva evidencia.
3. No inventes, completes por contexto ni infieras diagnósticos, fechas, dosis, resultados o antecedentes.
4. Si la nueva evidencia contradice un dato anterior, no lo sobrescribas silenciosamente: conserva ambos datos, indica la fecha o fuente cuando esté disponible y marca la discrepancia para revisión.
5. Si un campo no aparece en la evidencia disponible, escribe `No reportado en la evidencia disponible` cuando el campo deba estar presente en una sección nueva. No elimines datos anteriores solo porque no aparezcan en el documento nuevo.
6. Distingue entre condiciones confirmadas, reportadas por el paciente y diagnósticos registrados.
7. En medicamentos, conserva nombre, dosis, frecuencia, indicación, estado y cambios solo cuando estén documentados.
8. En mediciones y exámenes, conserva unidades, fecha y contexto cuando estén disponibles. No mezcles resultados de fechas diferentes.
9. En consultas, agrega una entrada solo por cada atención identificable e incluye fecha, lugar, especialidad, objeto breve y resumen breve. No dupliques una consulta ya registrada.
10. Mantén el resumen conciso, clínico y en español. No incluyas explicaciones sobre el proceso ni recomendaciones médicas que no estén en la evidencia.

## Estructura obligatoria

Usa exactamente estas secciones y este orden:

```markdown
## 1. Datos fijos del paciente

**Personales y demográficos**
- **Nombre:** ...
- **Identificación:** ...
- **Fecha de nacimiento:** ...
- **Sexo:** ...
- **Estado civil:** ...
- **Ocupación:** ...
- **Nacionalidad y residencia:** ...
- **Etnia:** ...
- **Zona:** ...
- **Afiliación:** ...

**Antecedentes**
- Alergias: ...
- Antecedentes quirúrgicos: ...
- Tabaquismo: ...
- Alcohol: ...
- Sustancias psicoactivas: ...
- Actividad física: ...
- Antecedentes familiares: ...

## 2. Condiciones médicas confirmadas o reportadas

- ...

## 3. Medicamentos

- ...

## 4. Resultados de mediciones y exámenes

- ...

## 5. Consultas

- **Fecha, lugar, especialidad:** objeto breve. Resumen breve.
```

Si un campo no está disponible al crear el archivo, usa `No reportado en la evidencia disponible`. Si una sección no tiene información, conserva su encabezado y escribe `No reportado en la evidencia disponible`.

Al finalizar, verifica que `summary.md` conserve las cinco secciones, que los cambios correspondan solo a la nueva evidencia y que no haya datos clínicos inventados.
