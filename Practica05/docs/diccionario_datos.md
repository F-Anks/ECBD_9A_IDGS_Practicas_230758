# Diccionario de Datos – Dataset de Pacientes del Estado de Puebla

## Información General

| Propiedad | Valor |
|-----------|-------|
| **Nombre del archivo** | `pacientes_puebla_5000.csv` |
| **Formato** | CSV (valores separados por comas) |
| **Codificación** | UTF-8 |
| **Total de registros** | 5,000 |
| **Total de columnas** | 47 |
| **Tipo de datos** | Simulados / Ficticios |
| **Propósito** | Académico |
| **Región geográfica** | Estado de Puebla, México |

---

## Descripción de Variables

### 1. Identificación del Paciente

| # | Variable | Tipo | Descripción | Ejemplo |
|---|----------|------|-------------|---------|
| 1 | `id_paciente` | Texto | Identificador único del paciente | PUE00001 |
| 2 | `nombre` | Texto | Nombre completo ficticio | Iván Martínez Villa |
| 3 | `sexo` | Categórico | Sexo biológico (M/F) | M |
| 4 | `edad` | Entero | Edad en años cumplidos | 54 |

### 2. Ubicación Geográfica

| # | Variable | Tipo | Descripción | Valores posibles |
|---|----------|------|-------------|-----------------|
| 5 | `municipio` | Categórico | Municipio del estado de Puebla | 22 municipios |
| 6 | `hospital` | Categórico | Unidad médica de atención | 58 hospitales/centros |
| 7 | `zona` | Categórico | Clasificación de zona | Urbana, Semiurbana, Rural |

### 3. Datos Socioeconómicos

| # | Variable | Tipo | Descripción | Valores posibles |
|---|----------|------|-------------|-----------------|
| 8 | `nivel_educativo` | Categórico | Nivel máximo de estudios | Sin estudios, Primaria, Secundaria, Preparatoria, Licenciatura, Posgrado |
| 9 | `nivel_socioeconomico` | Categórico | Clasificación socioeconómica | Bajo, Medio-bajo, Medio, Medio-alto, Alto |
| 10 | `tipo_seguro` | Categórico | Tipo de seguro médico | IMSS, ISSSTE, Seguro Popular/INSABI, Privado, Sin seguro |
| 11 | `fecha_ultima_visita` | Fecha | Fecha de la última consulta médica | 2024-10-02 |

### 4. Mediciones Antropométricas

| # | Variable | Tipo | Unidad | Rango | Descripción |
|---|----------|------|--------|-------|-------------|
| 12 | `talla_m` | Decimal | metros | 1.45 – 1.93 | Estatura del paciente |
| 13 | `peso_kg` | Decimal | kg | 40.0 – 129.9 | Peso corporal |
| 14 | `imc` | Decimal | kg/m² | 13.6 – 49.4 | Índice de Masa Corporal |
| 15 | `clasificacion_imc` | Categórico | — | — | Bajo peso, Normal, Sobrepeso, Obesidad I/II/III |

### 5. Presión Arterial

| # | Variable | Tipo | Unidad | Rango | Descripción |
|---|----------|------|--------|-------|-------------|
| 16 | `presion_sistolica` | Entero | mmHg | 85 – 200 | Presión arterial sistólica |
| 17 | `presion_diastolica` | Entero | mmHg | 50 – 113 | Presión arterial diastólica |
| 18 | `clasificacion_pa` | Categórico | — | — | Normal, Elevada, HTA Estadio 1/2 |

### 6. Indicadores Metabólicos

| # | Variable | Tipo | Unidad | Rango | Descripción |
|---|----------|------|--------|-------|-------------|
| 19 | `glucosa_ayuno_mg_dl` | Entero | mg/dL | 60 – 161 | Glucosa en ayuno |
| 20 | `clasificacion_glucosa` | Categórico | — | — | Normal, Prediabetes, Diabetes |
| 21 | `hba1c_pct` | Decimal | % | 3.5 – 11.5 | Hemoglobina glucosilada |

### 7. Perfil Lipídico

| # | Variable | Tipo | Unidad | Rango | Descripción |
|---|----------|------|--------|-------|-------------|
| 22 | `colesterol_total_mg_dl` | Entero | mg/dL | 120 – 360 | Colesterol total |
| 23 | `colesterol_ldl_mg_dl` | Entero | mg/dL | 40 – 250 | Colesterol LDL (malo) |
| 24 | `colesterol_hdl_mg_dl` | Entero | mg/dL | 25 – 95 | Colesterol HDL (bueno) |
| 25 | `trigliceridos_mg_dl` | Entero | mg/dL | 50 – 456 | Triglicéridos |

### 8. Otros Indicadores Clínicos

| # | Variable | Tipo | Unidad | Rango | Descripción |
|---|----------|------|--------|-------|-------------|
| 26 | `creatinina_mg_dl` | Decimal | mg/dL | 0.40 – 1.94 | Creatinina sérica |
| 27 | `hemoglobina_g_dl` | Decimal | g/dL | 9.4 – 19.0 | Hemoglobina |

### 9. Estilo de Vida

| # | Variable | Tipo | Descripción | Valores |
|---|----------|------|-------------|---------|
| 28 | `actividad_fisica` | Categórico | Nivel de actividad física | Sedentario, Leve, Moderada, Intensa |
| 29 | `tabaquismo` | Binario | Fumador activo | 0 = No, 1 = Sí |
| 30 | `alcoholismo` | Binario | Consumo frecuente de alcohol | 0 = No, 1 = Sí |

### 10. Comorbilidades

| # | Variable | Tipo | Descripción |
|---|----------|------|-------------|
| 31 | `diabetes_mellitus_t2` | Binario (0/1) | Diabetes Mellitus tipo 2 |
| 32 | `hipertension_arterial` | Binario (0/1) | Hipertensión arterial diagnosticada |
| 33 | `obesidad` | Binario (0/1) | Obesidad diagnosticada |
| 34 | `sobrepeso` | Binario (0/1) | Sobrepeso diagnosticado |
| 35 | `dislipidemia` | Binario (0/1) | Dislipidemia |
| 36 | `cardiopatia` | Binario (0/1) | Cardiopatía previa |
| 37 | `enfermedad_renal` | Binario (0/1) | Enfermedad renal crónica |
| 38 | `depresion` | Binario (0/1) | Depresión diagnosticada |
| 39 | `hipotiroidismo` | Binario (0/1) | Hipotiroidismo |
| 40 | `num_comorbilidades` | Entero | Conteo total de comorbilidades (0–6) |

### 11. Tratamiento Farmacológico

| # | Variable | Tipo | Descripción |
|---|----------|------|-------------|
| 41 | `metformina` | Binario (0/1) | Uso de Metformina |
| 42 | `insulina` | Binario (0/1) | Uso de Insulina |
| 43 | `antihipertensivos` | Binario (0/1) | Uso de antihipertensivos |
| 44 | `estatinas` | Binario (0/1) | Uso de estatinas |

### 12. Antigüedad de Enfermedad

| # | Variable | Tipo | Unidad | Rango | Descripción |
|---|----------|------|--------|-------|-------------|
| 45 | `anios_con_dm2` | Entero | años | 0 – 35 | Años viviendo con Diabetes tipo 2 |
| 46 | `anios_con_hta` | Entero | años | 0 – 40 | Años viviendo con Hipertensión |

### 13. Variable Objetivo

| # | Variable | Tipo | Rango | Descripción |
|---|----------|------|-------|-------------|
| 47 | `riesgo_cardiovascular_score` | Decimal | 0.0 – 7.7 | Score numérico de riesgo cardiovascular |

**Clasificación derivada:**

| Nivel de Riesgo | Rango del Score | Descripción |
|-----------------|-----------------|-------------|
| **Bajo** | score < 2.0 | Riesgo cardiovascular bajo |
| **Medio** | 2.0 ≤ score < 4.0 | Riesgo cardiovascular moderado |
| **Alto** | score ≥ 4.0 | Riesgo cardiovascular alto |

---

## Notas Importantes

- Todos los datos son **ficticios** y generados con fines **exclusivamente académicos**.
- No se utilizaron datos reales de pacientes ni información personal sensible.
- Los municipios, hospitales y centros de salud corresponden a ubicaciones reales del estado de Puebla para dar realismo geográfico al dataset.
- Los rangos de variables clínicas se basan en valores médicamente plausibles según literatura clínica.
