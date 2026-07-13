# Práctica 05 – Generación de Dataset de Pacientes con Indicadores para el Cálculo de Riesgo de Infarto Cardíaco en Puebla

## Objetivo General

Generar un dataset clínico simulado con información de **5,000 pacientes generales del estado de Puebla**, que sirva como base para prácticas posteriores relacionadas con clasificación de pacientes, visualización de datos y aplicación de algoritmos de análisis supervisado.

## Descripción

Esta práctica consiste en la creación, validación y análisis exploratorio de un dataset ficticio con fines **exclusivamente académicos**. Los datos simulan registros clínicos de pacientes del estado de Puebla, incluyendo variables demográficas, antropométricas, clínicas, geográficas y factores de riesgo cardiovascular.

> **Nota:** Todos los datos son ficticios y generados con fines académicos. No se utilizan datos reales de pacientes ni información personal sensible.

## Autor

- **Nombre:** Estudiante 230758
- **Materia:** Extracción y Clasificación de Base de Datos (ECBD)
- **Grupo:** 9A IDGS

## Estructura del Proyecto

```
Practica05/
├── data/
│   └── pacientes_puebla_5000.csv    # Dataset simulado (5,000 registros)
├── notebooks/
│   └── 01_Validacion_EDA.ipynb      # Notebook de validación y EDA
├── docs/                            # Documentación adicional
├── src/                             # Scripts de soporte
├── outputs/                         # Gráficas y resultados exportados
└── README.md                        # Este archivo
```

## Contexto del Dataset

El dataset simula registros clínicos de **5,000 pacientes generales** atendidos en hospitales y centros de salud del estado de **Puebla, México**. Incluye información de **22 municipios** y **58 unidades médicas** distribuidas en zonas urbanas, semiurbanas y rurales.

Los datos están diseñados para permitir el análisis de factores de riesgo cardiovascular y la clasificación de pacientes según su nivel de riesgo de infarto cardíaco.

## Atributos del Dataset (47 columnas)

### Datos de Identificación
| Columna | Tipo | Descripción |
|---------|------|-------------|
| `id_paciente` | Texto | Identificador único del paciente (PUE00001–PUE05000) |
| `nombre` | Texto | Nombre completo ficticio del paciente |
| `sexo` | Categórico | Sexo biológico: M (Masculino) o F (Femenino) |
| `edad` | Numérico | Edad en años (rango: 19–94) |

### Datos Geográficos
| Columna | Tipo | Descripción |
|---------|------|-------------|
| `municipio` | Categórico | Municipio de Puebla (22 municipios) |
| `hospital` | Categórico | Unidad médica de atención (58 hospitales/centros) |
| `zona` | Categórico | Tipo de zona: Urbana, Semiurbana, Rural |

### Datos Socioeconómicos
| Columna | Tipo | Descripción |
|---------|------|-------------|
| `nivel_educativo` | Categórico | Sin estudios, Primaria, Secundaria, Preparatoria, Licenciatura, Posgrado |
| `nivel_socioeconomico` | Categórico | Bajo, Medio-bajo, Medio, Medio-alto, Alto |
| `tipo_seguro` | Categórico | IMSS, ISSSTE, Seguro Popular/INSABI, Privado, Sin seguro |
| `fecha_ultima_visita` | Fecha | Fecha de la última consulta médica |

### Datos Antropométricos
| Columna | Tipo | Rango |
|---------|------|-------|
| `talla_m` | Numérico | 1.45 – 1.93 m |
| `peso_kg` | Numérico | 40.0 – 129.9 kg |
| `imc` | Numérico | 13.6 – 49.4 |
| `clasificacion_imc` | Categórico | Bajo peso, Normal, Sobrepeso, Obesidad I/II/III |

### Datos de Presión Arterial
| Columna | Tipo | Rango |
|---------|------|-------|
| `presion_sistolica` | Numérico | 85 – 200 mmHg |
| `presion_diastolica` | Numérico | 50 – 113 mmHg |
| `clasificacion_pa` | Categórico | Normal, Elevada, HTA Estadio 1, HTA Estadio 2 |

### Datos Metabólicos y Bioquímicos
| Columna | Tipo | Rango |
|---------|------|-------|
| `glucosa_ayuno_mg_dl` | Numérico | 60 – 161 mg/dL |
| `clasificacion_glucosa` | Categórico | Normal, Prediabetes, Diabetes |
| `hba1c_pct` | Numérico | 3.5 – 11.5 % |
| `colesterol_total_mg_dl` | Numérico | 120 – 360 mg/dL |
| `colesterol_ldl_mg_dl` | Numérico | 40 – 250 mg/dL |
| `colesterol_hdl_mg_dl` | Numérico | 25 – 95 mg/dL |
| `trigliceridos_mg_dl` | Numérico | 50 – 456 mg/dL |
| `creatinina_mg_dl` | Numérico | 0.40 – 1.94 mg/dL |
| `hemoglobina_g_dl` | Numérico | 9.4 – 19.0 g/dL |

### Factores de Estilo de Vida
| Columna | Tipo | Descripción |
|---------|------|-------------|
| `actividad_fisica` | Categórico | Sedentario, Leve, Moderada, Intensa |
| `tabaquismo` | Binario | 0 = No, 1 = Sí |
| `alcoholismo` | Binario | 0 = No, 1 = Sí |

### Comorbilidades (variables binarias 0/1)
| Columna | Descripción |
|---------|-------------|
| `diabetes_mellitus_t2` | Diabetes Mellitus tipo 2 |
| `hipertension_arterial` | Hipertensión arterial |
| `obesidad` | Obesidad diagnosticada |
| `sobrepeso` | Sobrepeso diagnosticado |
| `dislipidemia` | Dislipidemia |
| `cardiopatia` | Cardiopatía previa |
| `enfermedad_renal` | Enfermedad renal |
| `depresion` | Depresión |
| `hipotiroidismo` | Hipotiroidismo |
| `num_comorbilidades` | Conteo total de comorbilidades (0–6) |

### Tratamiento Farmacológico (variables binarias 0/1)
| Columna | Descripción |
|---------|-------------|
| `metformina` | Uso de Metformina |
| `insulina` | Uso de Insulina |
| `antihipertensivos` | Uso de antihipertensivos |
| `estatinas` | Uso de estatinas |

### Antigüedad de Enfermedad
| Columna | Tipo | Rango |
|---------|------|-------|
| `anios_con_dm2` | Numérico | 0 – 35 años |
| `anios_con_hta` | Numérico | 0 – 40 años |

### Variable Objetivo
| Columna | Tipo | Rango |
|---------|------|-------|
| `riesgo_cardiovascular_score` | Numérico | 0.0 – 7.7 |

La variable objetivo es un score numérico continuo que se clasifica en tres niveles de riesgo:
- **Bajo** (score < 2.0)
- **Medio** (2.0 ≤ score < 4.0)
- **Alto** (score ≥ 4.0)

## Reglas de Generación de Datos

- **Edad:** Rango de 19 a 94 años, distribución representativa de la población adulta.
- **Talla y peso:** Rangos realistas para población mexicana adulta.
- **IMC:** Calculado como peso / talla², con clasificación según criterios de la OMS.
- **Presión arterial:** Rangos según clasificación AHA (Normal, Elevada, HTA Estadio 1 y 2).
- **Glucosa en ayuno:** 60–161 mg/dL, con clasificación Normal (<100), Prediabetes (100–125), Diabetes (≥126).
- **HbA1c:** 3.5–11.5%, correlacionado con el estado glucémico.
- **Perfil lipídico:** Colesterol total, LDL, HDL y triglicéridos en rangos clínicamente coherentes.
- **Comorbilidades:** Asignadas con coherencia clínica (ej: pacientes con DM2 tienen mayor probabilidad de dislipidemia).
- **Geografía:** 22 municipios reales del estado de Puebla con hospitales y centros de salud existentes.
- **Variable objetivo:** Score de riesgo calculado considerando factores como edad, comorbilidades, perfil lipídico y presión arterial.

## Observaciones de Validación

- ✅ **5,000 registros** verificados (dimensiones correctas).
- ✅ **47 columnas** con nombres claros en formato snake_case.
- ✅ **Sin valores nulos** en todo el dataset.
- ✅ **Sin registros duplicados** (IDs únicos para cada paciente).
- ✅ **Rangos clínicos válidos** para la mayoría de las variables.
- ⚠️ **4 registros con IMC < 14** (mínimo 13.6), valores que están en el límite pero son clínicamente posibles en pacientes con bajo peso extremo.
- ✅ **22 municipios** corresponden a localidades reales del estado de Puebla.
- ✅ **58 unidades médicas** con nombres consistentes con la infraestructura de salud de Puebla.
- ✅ **3 zonas geográficas** (Urbana, Semiurbana, Rural) correctamente clasificadas.
