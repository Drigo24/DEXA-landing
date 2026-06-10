# Protocolo de Estudio Clínico

## Validación de un Modelo de Inteligencia Artificial Basado en Fotografía Intraoral para la Detección y Clasificación de Caries Dental (ICDAS) y Gingivitis (DEXA Vision)

**Versión:** 2.0
**Fecha:** Junio 2026
**Tipo de estudio:** Estudio de validación diagnóstica, retrospectivo, sobre base de datos de imágenes anónimas
**Diseño metodológico:** Conforme a la guía STARD 2015 (Standards for Reporting of Diagnostic Accuracy Studies)

---

## 1. Resumen Ejecutivo

**Antecedentes:** La caries dental y la enfermedad gingival son las patologías orales más prevalentes a nivel mundial. El diagnóstico temprano depende del acceso a profesionales y equipamiento, limitando la cobertura en poblaciones desatendidas. DEXA Vision es una aplicación móvil que utiliza un modelo de inteligencia artificial (IA) entrenado sobre fotografía intraoral para detectar y clasificar caries según el sistema ICDAS y para estratificar la gingivitis en niveles leve, moderado y severo.

**Objetivo:** Validar la precisión diagnóstica del modelo DEXA frente a la evaluación fotográfica realizada por odontólogos calibrados, sobre una base de datos de imágenes intraorales anónimas de pacientes adultos.

**Métodos:** Estudio de precisión diagnóstica retrospectivo. La prueba índice es el modelo IA DEXA procesando fotografías intraorales. El estándar de referencia es la evaluación independiente de las mismas fotografías por dos examinadores odontólogos calibrados. Se reportarán sensibilidad, especificidad, valores predictivos, exactitud, AUC, Kappa ponderado y concordancia inter-observador.

**Resultado primario esperado:** Exactitud global del modelo superior al 90%, con sensibilidad y especificidad ≥ 85% para ambas condiciones.

---

## 2. Justificación y Marco Teórico

### 2.1 Problema clínico
- La caries dental afecta aproximadamente al 60–90% de los adultos a nivel global (OMS).
- La gingivitis es reversible si se detecta tempranamente, pero progresa a periodontitis si no se trata.
- El diagnóstico convencional requiere examen clínico presencial con instrumentos y condiciones específicas, no siempre disponibles en atención primaria o zonas de baja cobertura.

### 2.2 Solución propuesta
DEXA Vision propone un cribado accesible mediante fotografía intraoral capturada con un dispositivo móvil. La validación de su precisión es el paso necesario previo a cualquier uso clínico o de tamizaje poblacional.

### 2.3 Brecha de conocimiento
No existe evidencia publicada que valide el desempeño del modelo DEXA frente a un estándar de referencia. Este estudio genera la primera evidencia de precisión diagnóstica del modelo y establece la base para estudios de validación prospectivos a mayor escala.

---

## 3. Objetivos e Hipótesis

### 3.1 Objetivo general
Evaluar la precisión diagnóstica del modelo de IA DEXA para la detección y clasificación de caries (ICDAS) y gingivitis (leve/moderada/severa) sobre fotografía intraoral, comparado con la evaluación fotográfica de referencia realizada por dos examinadores calibrados.

### 3.2 Objetivos específicos
1. Determinar la **sensibilidad y especificidad** del modelo para detectar presencia/ausencia de caries.
2. Determinar la **concordancia** entre la clasificación ICDAS del modelo y la del examinador (Kappa ponderado).
3. Determinar la **sensibilidad y especificidad** del modelo para detectar gingivitis.
4. Determinar la **concordancia** en la estratificación de severidad de gingivitis (Kappa ponderado).
5. Calcular la **concordancia inter-observador** entre los dos examinadores (Kappa de Cohen).

### 3.3 Hipótesis
- **H1:** El modelo DEXA presenta una exactitud global ≥ 90% para caries y gingivitis.
- **H0:** El modelo DEXA presenta una exactitud global < 90%.

> Nota: al ser un estudio piloto exploratorio, las estimaciones se reportan con intervalos de confianza del 95% como objetivo principal, más que como una prueba confirmatoria.

---

## 4. Diseño del Estudio

- **Tipo:** Estudio observacional, transversal, de precisión diagnóstica.
- **Carácter:** Retrospectivo, sobre base de datos de imágenes anónimas preexistentes.
- **Población:** Adultos exclusivamente.
- **Cegamiento:** El modelo de IA y los dos examinadores procesan las imágenes de forma **independiente y ciega** entre sí. Los examinadores no conocen el resultado del modelo al momento de su evaluación, y viceversa.
- **Unidad de análisis:** Dos niveles:
  - **Nivel imagen/cuadrante** (presencia/ausencia de la condición por fotografía).
  - **Nivel diente** para clasificación ICDAS cuando la imagen lo permita.

---

## 5. Base de Datos de Imágenes

### 5.1 Características de la base de datos
- Imágenes intraorales de pacientes adultos, **sin ningún identificador personal** (nombre, RUT, fecha de nacimiento u otro dato que permita vinculación al paciente).
- Tipo de imagen: fotografías por **cuadrante** y algunas de **arco completo**.
- Calidad: homogénea. Las imágenes fueron capturadas bajo condiciones similares de iluminación y encuadre.
- La base de datos es de carácter anónimo desde su origen, no derivada de un proceso de anonimización posterior.

### 5.2 Consideraciones éticas sobre el uso de la base de datos
Al tratarse de imágenes sin ningún identificador que permita vincularlas a personas naturales, los datos no son considerados datos personales bajo los marcos normativos estándar de protección de datos e investigación (incluido el marco GDPR y sus equivalentes). Por lo tanto:

- **No se requiere consentimiento informado** de los sujetos de las imágenes.
- Se recomienda de todas formas presentar el protocolo ante el **Comité de Ética (IRB)** para obtener una **exención formal de consentimiento (waiver)**, lo que fortalece la validez institucional del estudio ante HKU y para futura publicación.

---

## 6. Tamaño de Muestra

Para estimar sensibilidad/especificidad esperada (p = 0.90) con margen de error d = ±0.10 y confianza del 95%:

```
n = Z² · p(1−p) / d²
n = (1.96)² · (0.90)(0.10) / (0.10)²
n ≈ 35 imágenes positivas por condición
```

Considerando controles (imágenes sin la condición) y solapamiento entre caries y gingivitis:

| Condición | Imágenes positivas | Imágenes negativas | Subtotal |
|-----------|--------------------|--------------------|----------|
| Caries | 35 | 35 | 70 |
| Gingivitis | 35 | 35 | 70 |

**Objetivo: 80–100 imágenes/cuadrantes únicos.**

Dado que cada imagen puede mostrar tanto caries como gingivitis, el solapamiento permite alcanzar ambos objetivos con el mismo set de imágenes. Se recomienda seleccionar **100 imágenes** de la base de datos para compensar imágenes de baja calidad o no evaluables.

### Distribución recomendada de las 100 imágenes

| Grupo | N imágenes |
|-------|-----------|
| Con caries + gingivitis | ~40 |
| Solo caries (encías sanas) | ~20 |
| Solo gingivitis (sin caries) | ~20 |
| Sanas (controles negativos) | ~20 |
| **Total** | **~100** |

---

## 7. Variables y Definiciones

### 7.1 Prueba índice — Modelo DEXA
- **Insumo:** fotografía intraoral (por cuadrante o arco completo).
- **Salida caries:** clasificación ICDAS (códigos 0–6) por diente/imagen.
- **Salida gingivitis:** clasificación leve / moderada / severa, más score numérico (0–1).
- Las dos condiciones se analizan y reportan de forma **independiente**.

### 7.2 Estándar de referencia — Evaluación fotográfica por examinadores
- Los dos examinadores (odontólogos calibrados) evalúan **las mismas imágenes** de forma independiente.
- **Para caries:** clasificación visual ICDAS (0–6) basada en lo visible en la fotografía.
- **Para gingivitis:** clasificación de severidad (Sano / Leve / Moderada / Severa) basada en signos visibles: inflamación, eritema, recesión, cálculo visible, sangrado visible.
- En caso de discrepancia entre examinadores, se tomará la **moda** (valor coincidente) o se resolverá por consenso entre ambos, documentándolo.

> **Limitación inherente al diseño:** la evaluación fotográfica no reemplaza al examen clínico presencial (sin sondaje, sin secado, sin palpación). Esta limitación se declara explícitamente. El estudio valida la concordancia entre el modelo y un odontólogo evaluando la misma fotografía, que es la condición de uso real de la aplicación.

### 7.3 Calibración de examinadores
Antes del inicio, los dos examinadores evalúan un set de 20 imágenes de entrenamiento hasta alcanzar Kappa inter-observador ≥ 0.70. Se documenta el resultado.

---

## 8. Procedimiento

```
Base de datos (100 imágenes anónimas)
            │
            ├──► Modelo DEXA procesa cada imagen
            │    → Registra: ICDAS + Severidad gingivitis + Score
            │
            ├──► Examinador 1 evalúa cada imagen (ciego al modelo y a Examinador 2)
            │    → Registra: ICDAS + Severidad gingivitis
            │
            └──► Examinador 2 evalúa cada imagen (ciego al modelo y a Examinador 1)
                 → Registra: ICDAS + Severidad gingivitis
                          │
                          ▼
                   Base de datos consolidada
                          │
                          ▼
                   Análisis estadístico
```

1. Selección y numeración de las 100 imágenes (ID anónimo: IMG_001 a IMG_100).
2. Procesamiento por el modelo DEXA → registro en planilla.
3. Evaluación por Examinador 1 → registro en planilla.
4. Evaluación por Examinador 2 → registro en planilla (en sesión separada).
5. Consolidación y análisis.

---

## 9. Análisis Estadístico

### 9.1 Resultado primario
- **Sensibilidad, especificidad, VPP, VPN y exactitud (accuracy)** del modelo DEXA vs. estándar de referencia, con **intervalos de confianza del 95%** (método de Wilson).
- **Curva ROC y AUC** utilizando el score numérico continuo del modelo.

### 9.2 Concordancia
- **Kappa ponderado** (lineal) para ICDAS (0–6) y severidad de gingivitis (Sano/Leve/Moderada/Severa) entre DEXA y examinadores.
- **Kappa de Cohen** para concordancia inter-observador entre Examinador 1 y Examinador 2.

| Valor Kappa | Interpretación |
|-------------|----------------|
| < 0.20 | Pobre |
| 0.21 – 0.40 | Débil |
| 0.41 – 0.60 | Moderado |
| 0.61 – 0.80 | Bueno |
| 0.81 – 1.00 | Muy bueno |

### 9.3 Análisis por tipo de imagen
- Desempeño comparado entre imágenes **por cuadrante** vs. **arco completo** (análisis exploratorio).

### 9.4 Imágenes no evaluables
Las imágenes que no cumplan estándar mínimo de calidad se documentan y reportan como "no evaluables". No se imputan. Se reporta la proporción.

### 9.5 Software
R (pROC, irr) o Python (scikit-learn, statsmodels). Se reportará versión.

---

## 10. Consideraciones Éticas

- La base de datos no contiene identificadores personales → los datos **no son datos personales** según los marcos normativos estándar.
- **No se requiere consentimiento informado.**
- Se recomienda presentar el protocolo al IRB para obtención de **waiver de consentimiento**, lo que fortalece la validez del estudio para publicación y para HKU.
- **Conflicto de interés:** los desarrolladores de DEXA participan en el estudio. Se declarará explícitamente. Se recomienda que el análisis estadístico sea realizado o auditado por un tercero independiente.
- Las imágenes se almacenan en servidor seguro con acceso restringido al equipo investigador.

---

## 11. Limitaciones Previstas

1. **Gold standard fotográfico:** la evaluación por fotografía no equivale al examen clínico presencial (sin sondaje, secado ni palpación). El estudio valida la concordancia en condiciones de uso real de la app.
2. **Sesgo de espectro:** la distribución de severidades en la base de datos puede no reflejar la prevalencia poblacional real.
3. **Tamaño muestral piloto:** las estimaciones son preliminares. Los intervalos de confianza serán amplios; los resultados orientan un estudio de validación mayor.
4. **Conflicto de interés:** los desarrolladores son los validadores — mitigado mediante cegamiento y análisis independiente.

---

## 12. Cronograma

| Fase | Duración estimada |
|------|-------------------|
| Presentación a IRB (waiver) | 2–4 semanas |
| Calibración de examinadores | 1 semana |
| Evaluación de imágenes por examinadores | 2–3 semanas |
| Procesamiento por modelo DEXA | 1 semana |
| Análisis estadístico | 1 semana |
| Redacción del informe / manuscrito | 2 semanas |
| **Total estimado** | **~8 semanas** |

---

## 13. Resultados Esperados y Difusión

- Reporte de precisión diagnóstica del modelo DEXA (sensibilidad, especificidad, AUC, Kappa ponderado).
- Evidencia preliminar para justificar un estudio de validación prospectivo a mayor escala con examen clínico presencial como gold standard.
- Manuscrito para publicación en revista odontológica revisada por pares, siguiendo la lista de verificación STARD 2015.

---

## Apéndices

- **Apéndice A:** Protocolo estandarizado de evaluación fotográfica para examinadores.
- **Apéndice B:** Planilla de registro — Caries (ICDAS).
- **Apéndice C:** Planilla de registro — Gingivitis.
- **Apéndice D:** Lista de verificación STARD 2015 completada.
- **Apéndice E:** Plan de análisis estadístico detallado.

---

*Documento preparado para presentación a la University of Hong Kong (HKU). DEXA Vision — Validación de modelo de IA para tamizaje odontológico. Versión 2.0 — Junio 2026.*
