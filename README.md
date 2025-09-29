[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/6Fb5sosR)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=20769924&assignment_repo_type=AssignmentRepo)
# Práctica 00 · GitHub Classroom + VS Code (versión sencilla)

Objetivo: practicar el flujo **clonar → implementar → probar → commit/push** con dos funciones muy simples.

## Pasos

1) **Acepta la tarea** en GitHub Classroom (enlace del profesor/a).
2) **Clona** tu repositorio:
```bash
git clone <URL-de-tu-repo>
cd <carpeta-del-repo>
```
3) (Opcional) **Crea un entorno** y activa:
```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate
```
4) **Instala dependencias**:
```bash
pip install -r requirements.txt
```
5) **Ejecuta los tests** (verás que FALLAN al principio):
```bash
pytest -q
```
6) **Implementa** las funciones en `src/` siguiendo los `# TODO`:
- `src/math_ops.py` → `add(a, b)` suma y devuelve el resultado.
- `src/strings.py` → `shout(text)` devuelve el texto en MAYÚSCULAS.
7) **Vuelve a probar**:
```bash
pytest -q
```
8) **Commit + push**:
```bash
git add -A
git commit -m "Implemento add y shout"
git push origin main
```
GitHub Actions ejecutará los tests automáticamente (Autograding en Classroom).

---

## Estructura
```
src/
  __init__.py
  math_ops.py
  strings.py
test/
  test_math_ops.py
  test_strings.py
```
