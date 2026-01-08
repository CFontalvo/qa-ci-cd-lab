qa-ci-cd-lab

![CI](https://github.com/CFontalvo/qa-ci-cd-lab/actions/workflows/ci.yml/badge.svg)

Repositorio de laboratorio para aprender y demostrar Git, CI y CD desde cero hasta nivel profesional, usando Python y pytest con un enfoque práctico orientado a QA Engineers.

Este proyecto evoluciona por iteraciones reales: cada cambio en el código se versiona, se prueba y (más adelante) se automatiza con pipelines de CI/CD.

Objetivos del proyecto

Aprender Git de forma práctica con cambios reales en el código

Construir pipelines de CI/CD desde cero

Aplicar buenas prácticas profesionales:

estructura src/

tests automatizados

commits semánticos

control de versiones

Servir como evidencia técnica pública para roles QA / Automation / SDET

Stack técnico

Python 3.10+

pytest

Git + GitHub

(Próximamente) GitHub Actions

Estructura del proyecto
qa-ci-cd-lab/
│
├── src/
│   └── qa_ci_cd_lab/
│       ├── __init__.py
│       └── calculator.py
│
├── tests/
│   ├── __init__.py
│   └── test_calculator.py
│
├── requirements.txt
├── pyproject.toml
├── .gitignore
├── LICENSE
└── README.md

Setup en 60 segundos
1. Clonar el repositorio
git clone git@github.com:CFontalvo/qa-ci-cd-lab.git
cd qa-ci-cd-lab

2. Crear y activar entorno virtual

Windows (PowerShell)

python -m venv .venv
.\.venv\Scripts\Activate.ps1


Linux / macOS

python -m venv .venv
source .venv/bin/activate

3. Instalar dependencias
pip install --upgrade pip
pip install -r requirements.txt

4. Ejecutar pruebas
pytest -q


Si todo está correcto, verás todas las pruebas pasando.

Módulo actual: Calculator

El proyecto inicia con un módulo simple que permite:

Sumar

Restar

Multiplicar

Dividir (con manejo de división por cero)

Archivo:
src/qa_ci_cd_lab/calculator.py

Ejemplo de uso:

from qa_ci_cd_lab.calculator import add, divide

result = add(2, 3)
print(result)  # 5

print(divide(10, 2))  # 5.0

Pruebas automatizadas

Las pruebas están escritas con pytest y cubren:

Casos exitosos

Manejo de errores (división por cero)

Archivo:
tests/test_calculator.py

La configuración de pytest se maneja desde pyproject.toml, usando la estructura src/.

Buenas prácticas aplicadas

Estructura src/ (evita problemas de importación en CI)

Tests separados del código de producción

Repositorio público con licencia

Commits descriptivos y orientados a cambios reales

Proyecto diseñado para crecer hacia CI/CD

Roadmap (próximos pasos)

 Configurar CI con GitHub Actions

 Ejecutar tests automáticamente en cada PR

 Generar reportes de cobertura

 Implementar quality gates

 Versionado y releases automáticos

 CD (deploy de artifacts / documentación)

Licencia

Este proyecto está licenciado bajo la licencia MIT.
Puedes usarlo, modificarlo y adaptarlo libremente.

Autor

Christian Fontalvo
QA Engineer | Automation | CI/CD
Blog: https://christianfontalvo.com

Nota final

Este repositorio no es un “demo de tutorial”.
Es un laboratorio vivo: cada commit cuenta una historia real de aprendizaje y evolución técnica.