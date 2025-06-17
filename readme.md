🍽️ dieta13  
`dieta13` es una aplicación web empresarial desarrollada en Java EE como parte de la asignatura **Test, Integració i Evolució del Software** del Grado de Ingeniería Informática en la **Universitat de les Illes Balears (UIB)**.

La aplicación simula un sistema de gestión de dietas, alimentos y usuarios, incluyendo operaciones CRUD, login, y gestión de restricciones alimentarias. Su objetivo académico es servir de base para aplicar técnicas de testing profesional: unitarias, de integración, BDD, y de caja negra.

---

📌 Funcionalidad General

La aplicación permite:

- 🥗 Gestionar alimentos y sus propiedades (nombre, calorías, restricciones, etc.)
- 👤 Registrar y autenticar usuarios
- 📋 Crear y asignar dietas personalizadas a usuarios
- ⚠️ Filtrar alimentos según restricciones médicas o preferencias

Desde la interfaz JSF, el usuario puede navegar entre diferentes vistas para consultar, añadir, modificar y eliminar registros relacionados con la dieta y los ingredientes.

---

📦 Estructura del Proyecto

El sistema está dividido en módulos Maven con arquitectura en capas:

```
dieta13/
├── dieta13-ear/          ← Empaquetado EAR
├── dieta13-ejb/          ← Lógica de negocio (servicios EJB)
├── dieta13-persistence/  ← Entidades JPA y DAOs
├── dieta13-web/          ← Interfaz web JSF y controladores
├── pom.xml               ← Configuración principal
```

---

🌐 Tecnologías Utilizadas

- Java EE 8 / Jakarta EE  
- JSF (JavaServer Faces)  
- JPA (Hibernate)  
- CDI (Inyección de dependencias)  
- Maven  
- WildFly (servidor de aplicaciones)  
- XHTML para la capa de vista  

---

🛠️ Requisitos

- JDK 11 o superior  
- Maven 3.6+  
- WildFly 26+ u otro contenedor Java EE compatible  
- Navegador web moderno  

---

🚀 ¿Cómo se ejecuta?

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/nasiiimb/dieta13.git
   cd dieta13
   ```

2. Compilar y empaquetar el proyecto:
   ```bash
   mvn clean install
   ```

3. Desplegar el archivo `.ear` generado:
   ```
   dieta13-ear/target/dieta13.ear
   ```
   en tu servidor (por ejemplo, WildFly).

4. Acceder desde el navegador:
   ```
   http://localhost:8080/dieta13-web/
   ```

---

🧪 Testing aplicado

El desarrollo se ha acompañado de pruebas automatizadas desde distintas capas:

| Tipo de Test         | Herramientas        | Objetivo                                       |
|----------------------|---------------------|------------------------------------------------|
| Unitarios            | JUnit 5             | Comprobar la lógica de negocio aislada         |
| Con mocks            | Mockito             | Simular dependencias externas en servicios     |
| BDD                  | Cucumber + Gherkin  | Describir escenarios funcionales con lenguaje natural |
| Caja negra           | Selenium            | Validar flujos completos desde la interfaz     |

Los tests garantizan una cobertura mínima del 80% de líneas de código, y permiten detectar errores en integración continua (GitLab CI/CD).

---

📜 Créditos

Desarrollado por:  
**Nasim Benyacoub Terki**  
**Felip Antoni Font Vicens**  

Curso 2024–2025 – Universitat de les Illes Balears  
Asignatura: *Test, integració i evolució del software*
