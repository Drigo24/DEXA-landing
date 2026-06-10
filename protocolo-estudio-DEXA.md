# Protocolo de Estudio Clínico

## Validación de un Modelo de Inteligencia Artificial Basado en Fotografía Intraoral para la Detección y Clasificación de Caries Dental (ICDAS) y Gingivitis (DEXA Vision)

**Versión:** 1.0
**Fecha:** Junio 2026
**Tipo de estudio:** Estudio piloto de validación diagnóstica, prospectivo, multicéntrico
**Diseño metodológico:** Conforme a la guía STARD 2015 (Standards for Reporting of Diagnostic Accuracy Studies)

---

## 1. Resumen Ejecutivo (Abstract estructurado)

**Antecedentes:** La caries dental y la enfermedad gingival son las patologías orales más prevalentes a nivel mundial. El diagnóstico temprano depende del acceso a profesionales y equipamiento, lo que limita la cobertura en poblaciones desatendidas. DEXA Vision es una aplicación móvil que utiliza un modelo de inteligencia artificial (IA) entrenado sobre fotografía intraoral para detectar y clasificar caries según el sistema ICDAS y para estratificar la gingivitis en niveles leve, moderado y severo.

**Objetivo:** Validar la precisión diagnóstica del modelo DEXA frente al examen clínico realizado por odontólogos calibrados, en una muestra piloto de pacientes pediátricos y adultos.

**Métodos:** Estudio de precisión diagnóstica con prueba índice (IA DEXA sobre fotografía intraoral) comparada contra un estándar de referencia (examen clínico presencial por dos examinadores calibrados). Se reportarán sensibilidad, especificidad, valores predictivos, exactitud (accuracy), índice Kappa ponderado y concordancia inter-observador.

**Resultado primario esperado:** Exactitud global del modelo superior al 90%, con sensibilidad y especificidad ≥ 85% para ambas condiciones.

---

## 2. Justificación y Marco Teórico

### 2.1 Problema clínico
- La caries dental afecta a aproximadamente el 60–90% de los escolares y a la mayoría de los adultos a nivel global (OMS).
- La gingivitis es reversible si se detecta tempranamente, pero progresa a periodontitis si no se trata.
- El diagnóstico convencional requiere examen clínico presencial, exploración con sonda y, frecuentemente, radiografías — recursos no siempre disponibles en atención primaria o zonas rurales.

### 2.2 Solución propuesta
DEXA Vision propone un cribado (screening) accesible mediante fotografía intraoral capturada con un dispositivo móvil, procesada por un modelo de IA. La validación científica de su precisión es el paso necesario previo a cualquier uso clínico o de tamizaje poblacional.

### 2.3 Brecha de conocimiento
No existe aún evidencia publicada que valide el desempeño del modelo DEXA frente a un estándar clínico. Este estudio piloto busca generar la primera evidencia de precisión diagnóstica y establecer las bases para un estudio de validación a mayor escala.

---

## 3. Objetivos e Hipótesis

### 3.1 Objetivo general
Evaluar la precisión diagnóstica del modelo de IA DEXA para la detección y clasificación de caries (ICDAS) y gingivitis (leve/moderada/severa) sobre fotografía intraoral, comparado con el examen clínico de referencia.

### 3.2 Objetivos específicos
1. Determinar la **sensibilidad y especificidad** del modelo para detectar presencia/ausencia de caries.
2. Determinar la **concordancia** entre la clasificación ICDAS del modelo y la del examinador clínico (Kappa ponderado).
3. Determinar la **sensibilidad y especificidad** del modelo para detectar gingivitis.
4. Determinar la **concordancia** en la estratificación de severidad de gingivitis (leve/moderada/severa).
5. Calcular la **concordancia inter-observador** entre los dos examinadores clínicos (Kappa de Cohen).
6. Explorar el desempeño diferencial en **población pediátrica vs. adulta** (análisis de subgrupos exploratorio).

### 3.3 Hipótesis
- **H1:** El modelo DEXA presenta una exactitud global ≥ 90% para caries y gingivitis.
- **H0:** El modelo DEXA presenta una exactitud global < 90%.

> Nota metodológica: al ser un estudio **piloto exploratorio**, las estimaciones de sensibilidad/especificidad se reportan con sus intervalos de confianza del 95% como objetivo principal, más que como una prueba de hipótesis confirmatoria.

---

## 4. Diseño del Estudio

- **Tipo:** Estudio observacional, transversal, de precisión diagnóstica.
- **Carácter:** Prospectivo, multicéntrico.
- **Cegamiento:** El modelo de IA y los examinadores clínicos evalúan de forma **independiente y ciega** entre sí. El operador que captura la fotografía no comunica el resultado de la IA al examinador clínico, y viceversa.
- **Unidad de análisis:** Se realizará el análisis en **dos niveles**:
  - **Nivel paciente** (presencia/ausencia de la condición).
  - **Nivel diente/superficie** (para la clasificación ICDAS y la localización de hallazgos), que es la unidad recomendada para reportar precisión a nivel de lesión.

---

## 5. Población y Muestra

### 5.1 Centros participantes
Estudio multicéntrico. Se reclutará en 2 o más centros clínicos colaboradores. (Definir y listar los centros en la versión final del protocolo, con sus respectivos investigadores responsables.)

### 5.2 Criterios de elegibilidad
- **Inclusión:** Pacientes pediátricos y adultos que acudan a consulta odontológica y otorguen consentimiento (o asentimiento + consentimiento del tutor en menores).
- **Exclusión:** No se aplican criterios de exclusión clínicos. Se documentará cualquier condición que impida la captura fotográfica adecuada (ej. imposibilidad de apertura bucal, no cooperación).
- **Protocolo combinado:** niños y adultos se incluyen en el mismo protocolo, con análisis de subgrupo por edad.

### 5.3 Cálculo del tamaño muestral

Para estimar la sensibilidad/especificidad esperada (p = 0.90) con un margen de error d = ±0.10 y confianza del 95% (Z = 1.96):

```
n = Z² · p(1−p) / d²
n = (1.96)² · (0.90)(0.10) / (0.10)²
n = 3.8416 · 0.09 / 0.01
n ≈ 35 casos positivos por condición
```

Considerando un número equivalente de controles (casos sin la condición) y el solapamiento de pacientes que presentan simultáneamente caries y gingivitis:

| Condición | Casos positivos | Casos negativos | Subtotal |
|-----------|-----------------|------------------|----------|
| Caries (ICDAS) | 35 | 35 | 70 |
| Gingivitis | 35 | 35 | 70 |
| Solapamiento estimado | — | — | (reduce el total) |

**Tamaño muestral objetivo: 80–100 pacientes.**

Este rango es metodológicamente sólido y consistente con la literatura de estudios piloto de validación diagnóstica en odontología. Se recomienda reclutar **100 pacientes** para compensar pérdidas, imágenes no evaluables y asegurar suficientes casos en cada categoría ICDAS y de severidad de gingivitis.

### 5.4 Muestreo
Muestreo consecutivo de pacientes elegibles que acudan a los centros participantes durante el periodo de reclutamiento.

---

## 6. Variables y Definiciones

### 6.1 Prueba índice (Index test) — Modelo DEXA
- **Insumo:** fotografía intraoral capturada con dispositivo móvil siguiendo un protocolo estandarizado de captura.
- **Salida para caries:** clasificación **ICDAS (códigos 0–6)** por diente/superficie.
- **Salida para gingivitis:** clasificación de severidad **leve / moderada / severa**, más score numérico.
- El modelo puede analizar dientes y encías de forma conjunta; para este estudio se analizan y reportan **por separado** (caries y gingivitis como dominios independientes).

### 6.2 Estándar de referencia (Reference standard) — Examen clínico
- **Caries:** examen clínico visual-táctil con criterios **ICDAS** por odontólogo calibrado, bajo iluminación adecuada y secado del diente según el protocolo ICDAS.
- **Gingivitis:** evaluación clínica de signos visibles — inflamación, eritema, recesión, cálculo visible y sangrado visible/al sondaje — clasificada en leve/moderada/severa según criterios clínicos predefinidos.
- **Dos examinadores** evalúan a los **mismos pacientes** de forma independiente, permitiendo calcular la concordancia inter-observador.

### 6.3 Calibración de examinadores
Previo al inicio, los dos examinadores realizarán una sesión de calibración (sobre un set de casos de entrenamiento) hasta alcanzar un Kappa inter-observador ≥ 0.70. Se documentará el resultado de la calibración.

---

## 7. Procedimiento del Estudio (Flujo)

1. Reclutamiento y consentimiento/asentimiento informado.
2. Registro de datos demográficos (edad, sexo, antecedentes relevantes).
3. **Captura fotográfica intraoral** estandarizada → procesamiento por el modelo DEXA → registro del resultado (ICDAS y severidad de gingivitis). La salida queda almacenada y **cegada** para los examinadores clínicos.
4. **Examen clínico** por Examinador 1 (ciego al resultado de la IA).
5. **Examen clínico** por Examinador 2 (ciego al resultado de la IA y al de Examinador 1).
6. Consolidación de datos en la base de datos del estudio.
7. Análisis estadístico.

```
Paciente elegible
      │
      ▼
Consentimiento ──► Datos demográficos
      │
      ▼
Foto intraoral ──► Modelo DEXA (ICDAS + gingivitis)  [cegado]
      │
      ▼
Examinador 1 (clínico)  [ciego a IA]
Examinador 2 (clínico)  [ciego a IA y a Examinador 1]
      │
      ▼
Base de datos ──► Análisis estadístico
```

---

## 8. Análisis Estadístico

### 8.1 Resultado primario
- **Sensibilidad, especificidad, valor predictivo positivo (VPP), valor predictivo negativo (VPN) y exactitud (accuracy)** del modelo DEXA frente al estándar de referencia, con **intervalos de confianza del 95%** (método de Wilson o Clopper-Pearson).
- Curva ROC y **AUC** cuando se utilice el score numérico continuo.

### 8.2 Concordancia
- **Kappa ponderado (lineal o cuadrático)** para la clasificación ordinal ICDAS (0–6) y para la severidad de gingivitis (leve/moderada/severa) entre el modelo y el examen clínico.
- **Kappa de Cohen** para la concordancia inter-observador entre Examinador 1 y Examinador 2.
- Interpretación según Landis y Koch: <0.20 pobre; 0.21–0.40 débil; 0.41–0.60 moderado; 0.61–0.80 bueno; 0.81–1.00 muy bueno.

### 8.3 Análisis de subgrupos (exploratorio)
- Desempeño en **población pediátrica vs. adulta**.
- Desempeño por categoría ICDAS y por severidad de gingivitis.

### 8.4 Manejo de datos faltantes / imágenes no evaluables
Las fotografías que no cumplan el estándar mínimo de calidad se documentarán y reportarán como "no evaluables" (proporción reportada), sin imputación.

### 8.5 Software
Análisis en R, Python (scikit-learn / statsmodels) o SPSS. Se reportará el software y versión.

---

## 9. Consideraciones Éticas

- Aunque este protocolo se presenta en **fase piloto**, todo estudio con seres humanos debe contar con la **aprobación de un Comité de Ética en Investigación (IRB)** antes del reclutamiento.
- **Consentimiento informado** de adultos y, en menores, **consentimiento del tutor legal + asentimiento del menor**.
- **Confidencialidad:** las fotografías intraorales y los datos se anonimizan/seudonimizan. Las imágenes faciales no se capturan (solo intraoral).
- **Protección de datos:** almacenamiento cifrado, acceso restringido al equipo de investigación, cumplimiento de la normativa local de protección de datos.
- **Riesgo:** mínimo. La captura fotográfica intraoral y el examen clínico no invasivo no añaden riesgo más allá de la consulta odontológica habitual.
- **Declaración de conflicto de interés:** los desarrolladores de DEXA participan en el estudio; se declarará explícitamente y el análisis estadístico debe ser, idealmente, realizado o auditado por un tercero independiente para reducir sesgo.

---

## 10. Limitaciones Previstas

- Tamaño muestral piloto: las estimaciones son preliminares y orientan un estudio de validación mayor.
- Verificación parcial: posible sesgo de espectro al incluir muestreo consecutivo.
- El estándar de referencia clínico (sin radiografía/histología) puede subestimar caries proximales/ocultas — se reconoce como limitación del gold standard elegido.
- Generalización limitada al no excluir pacientes: alta validez externa pero mayor heterogeneidad.

---

## 11. Cronograma (propuesto)

| Fase | Duración estimada |
|------|-------------------|
| Aprobación ética (IRB) | 1–2 meses |
| Calibración de examinadores | 2 semanas |
| Reclutamiento y recolección de datos | 2–3 meses |
| Análisis estadístico | 1 mes |
| Redacción del informe / manuscrito | 1 mes |

---

## 12. Resultados Esperados y Difusión

- Reporte de precisión diagnóstica del modelo DEXA (sensibilidad, especificidad, AUC, Kappa).
- Evidencia preliminar para justificar un estudio de validación a mayor escala y multicéntrico ampliado.
- Manuscrito para publicación en revista odontológica revisada por pares, siguiendo la lista de verificación STARD 2015.

---

## Apéndices (a desarrollar en versión final)

- **Apéndice A:** Protocolo estandarizado de captura fotográfica intraoral.
- **Apéndice B:** Hoja de registro clínico (ICDAS y gingivitis).
- **Apéndice C:** Formularios de consentimiento informado y asentimiento.
- **Apéndice D:** Lista de verificación STARD 2015 completada.
- **Apéndice E:** Plan de análisis estadístico detallado.

---

*Documento preparado para presentación a la University of Hong Kong (HKU). DEXA Vision — Validación de modelo de IA para tamizaje odontológico.*
