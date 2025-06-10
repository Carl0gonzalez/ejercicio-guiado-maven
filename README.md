# TaskMaster

TaskMaster es una aplicación simple que permite gestionar tareas desde la consola. Fue creada como parte de un ejercicio guiado para aprender a usar Apache Maven de forma profesional, automatizando el ciclo de construcción y ejecución de software.

## 📌 Descripción del Proyecto

Este proyecto permite añadir y mostrar tareas pendientes desde la línea de comandos. Se utiliza Maven para:

- Gestionar dependencias.
- Ejecutar pruebas unitarias.
- Empaquetar y ejecutar el proyecto.
- Crear perfiles de configuración.

## 🛠 Comandos usados con Maven

```bash
# Crear el proyecto con estructura profesional
mvn archetype:generate -DgroupId=com.equipo.taskmaster -DartifactId=taskmaster -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false

# Compilar y empaquetar la aplicación
mvn clean package

# Ejecutar la aplicación desde Maven
mvn exec:java

# Ejecutar con un perfil
mvn exec:java -Pdev -Denv.name=Dev

# Ejecutar pruebas unitarias
mvn test

# Instalar el jar en el repositorio local
mvn install
```

## 📦 Dependencias y Plugins Utilizados

### Dependencias

```xml
<dependency>
  <groupId>org.apache.commons</groupId>
  <artifactId>commons-lang3</artifactId>
  <version>3.12.0</version>
</dependency>

<dependency>
  <groupId>junit</groupId>
  <artifactId>junit</artifactId>
  <version>3.8.1</version>
  <scope>test</scope>
</dependency>
```

### Plugins

```xml
<plugin>
  <groupId>org.apache.maven.plugins</groupId>
  <artifactId>maven-compiler-plugin</artifactId>
  <version>3.8.1</version>
  <configuration>
    <source>11</source>
    <target>11</target>
  </configuration>
</plugin>

<plugin>
  <groupId>org.codehaus.mojo</groupId>
  <artifactId>exec-maven-plugin</artifactId>
  <version>3.1.0</version>
  <configuration>
    <mainClass>com.equipo.taskmaster.App</mainClass>
  </configuration>
</plugin>
```

## 🔁 Estructura del Proyecto

```
taskmaster/
├── pom.xml
├── README.md
├── src/
│   ├── main/
│   │   └── java/
│   │       └── com/
│   │           └── equipo/
│   │               └── taskmaster/
│   │                   └── App.java
│   └── test/
│       └── java/
│           └── com/
│               └── equipo/
│                   └── taskmaster/
│                       └── AppTest.java
```

## 💡 Aprendizajes Técnicos

- Automatizar compilación, pruebas y empaquetado con Maven.
- Integrar librerías externas y pruebas unitarias.
- Uso de perfiles para configuración de entornos.
- Buenas prácticas en la estructura de un proyecto Java profesional.

## 🧗‍♀️ Desafío Enfrentado

Uno de los mayores retos fue entender y resolver errores relacionados con versiones de compilador y dependencias, así como mover correctamente la raíz del repositorio Git para que el proyecto estuviera bien estructurado desde GitHub.

