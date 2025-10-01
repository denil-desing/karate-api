# Karate Gorest API Automation

Proyecto de automatización de APIs utilizando **Karate** para pruebas CRUD (Create, Read, Update, Delete) sobre la API pública de [GoRest](https://gorest.co.in/).
Este proyecto está preparado con **pipeline CI/CD** en GitHub Actions y buenas prácticas de testing.

Se cubren escenarios típicos de CRUD de usuarios en GoRest:

1. **List users** → Verifica que la API devuelve usuarios correctamente.  
2. **Create user** → Genera usuarios con correos dinámicos.  
3. **Update user** → Modifica información de usuarios existentes.  
4. **Delete user** → Elimina usuarios y valida la operación.  

Se implementa **reutilización de escenarios** mediante `call` a otros features y validaciones con `match` de Karate.

## Tecnologías
- Java 11+
- Maven
- Karate Framework
- Git / GitHub
- GitHub Actions (CI/CD)
- GoRest API (https://gorest.co.in/)
## Estructura del proyecto
karate-gorest-api/
├── src/test/java/com/gorest/
│ ├── users.feature
│ ├── update-user.feature
│ └── delete-user.feature
├── pom.xml
├── README.md
└── .github/workflows/karate.yml

##  Requisitos
- Java 11 o superior
- Maven 3.6+
- Git instalado
- Conexión a Internet para llamar a la API GoRest
---
##  Ejecución local

Para correr todos los tests de Karate:

```bash
mvn test
## Buenas prácticas aplicadas

Uso de UUIDs para generar correos únicos y evitar conflictos.
Validaciones dinámicas con match de Karate.
Separación de escenarios CRUD en features individuales para reutilización.
Pipeline CI/CD automatizado para integración continua.
Reportes claros de ejecución y resultados.
