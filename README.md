Para levantar el proyecto
1.- Debe tener instalado: librerias_necesarias/lombok.jar
2.- Renombrar el archivo: website/pom.xml.example.intellij_java_21 a pom.xml
2.- Renombrar el archivo: website\src\main\resources\application.properties.example a application.properties



------------------------------
# 🛠 Proyecto en equipo con Git (4 personas)

## 🌳 Estructura de ramas

- `main`: Rama principal (protegida). Solo se actualiza desde `dev`.
- `dev`: Rama de desarrollo compartida por todos.
- `feature/xyz`: Ramas individuales por funcionalidad, creadas desde `dev`.

---

## 🔄 Flujo de trabajo

### 1. Clonar el repositorio (solo la primera vez)
```bash
git clone https://github.com/yaircaballero15/proyecto-ci-agenda-digital.git
cd proyecto
```

---

### 2. Crear una nueva rama para tu funcionalidad
```bash
git checkout dev
git pull origin dev
git checkout -b feature/mi-tarea
```

---

### 3. Trabajar en tu tarea
```bash
# Hacer cambios
git add .
git commit -m "Mi avance o tarea finalizada"
git push origin feature/mi-tarea
```

---

### 4. Crear un Pull Request
- Ir a GitHub.
- Abrir un Pull Request desde tu rama: `feature/mi-tarea` → `dev`.
- Esperar revisión y aprobación.
- Hacer merge desde GitHub.
- Eliminar la rama (opcional, pero recomendado).

---

### 5. Fusionar `dev` a `main` (solo el responsable)
- Una vez que `dev` está estable y probado:
  - Crear Pull Request de `dev` → `main`.
  - Hacer merge desde GitHub.

---

## ✅ Recomendaciones

- Siempre crear ramas desde `dev`.
- No trabajar en `main` ni en `dev` directamente.
- Usar ramas con nombres claros: `feature/login`, `feature/validacion-email`, etc.
- Eliminar tu rama `feature/*` luego del merge.
- Evitar dejar ramas viejas sin usar.

---

## 🧠 Buenas prácticas

- Hacer commits pequeños y claros.
- Pedir revisión antes del merge.
- Mantener `dev` funcionando correctamente para todos.