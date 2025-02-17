# 🌎 Internacionalización en Spring Boot con Gradle

Este proyecto es una aplicación **Spring Boot** con soporte para **internacionalización (i18n)**, lo que permite mostrar mensajes en diferentes idiomas según la configuración del usuario.

## 🚀 Tecnologías Utilizadas

- **Java 21**
- **Spring Boot**
- **Gradle**
- **Postman** (para pruebas)

---

## 📥 Instalación y Configuración

### 1️⃣ Clonar el Repositorio

```bash
git clone https://github.com/krat214/parcial2.git
cd proyecto-spring-i18n
```

### 2️⃣ Construir el Proyecto con Gradle

```bash
./gradlew build  # En Linux/Mac
gradlew.bat build  # En Windows
```

### 3️⃣ Ejecutar la Aplicación

```bash
./gradlew bootRun  # En Linux/Mac
gradlew.bat bootRun  # En Windows
```

Si todo está bien, verás en la consola:

```bash
Tomcat started on port(s): 8080 (http)
```

---

## 🌍 Configuración de Internacionalización

Los mensajes están almacenados en archivos **.properties** dentro de `src/main/resources/`:

- **Español** → `messages_es.properties`
  ```properties
  welcome.message=¡Hola! Bienvenido a nuestra aplicación internacionalizada.
  ```
- **Inglés** → `messages_en.properties`
  ```properties
  welcome.message=Hello! Welcome to our internationalized application.
  ```

---

## 🔥 Probando la API con Postman o cURL

### **Usando Postman**

1. Abre **Postman** y selecciona **GET**.
2. Introduce la URL:
   ```
   http://localhost:8080/saludo
   ```
3. Agrega un **Header**:
   - **Key:** `Accept-Language`
   - **Value:** `es` (para español) o `en` (para inglés).
4. Presiona **Send** y revisa la respuesta.

### **Usando cURL en la Terminal**

- Para español:

  ```bash
  curl -H "Accept-Language: es" http://localhost:8080/saludo
  ```

  🔹 **Salida esperada:** `¡Hola! Bienvenido a nuestra aplicación internacionalizada.`

- Para inglés:

  ```bash
  curl -H "Accept-Language: en" http://localhost:8080/saludo
  ```

  🔹 **Salida esperada:** `Hello! Welcome to our internationalized application.`

---

## 📂 Estructura del Proyecto

```
📦 src/main/java/com/parcial2/
 ┣ 📂 config/ → Configuración de i18n
 ┃ ┗ 📜 ConfiguracionInternacionalizacion.java
 ┣ 📂 controllers/ → Controlador REST
 ┃ ┗ 📜 InternacionalizacionController.java
📦 src/main/resources/
 ┣ 📜 messages_en.properties
 ┣ 📜 messages_es.properties
```

---

## 🛠️ Autor y Contribuciones

- **Autor:** Angel Enrique Renteria (https://github.com/krat214)
- Pull Requests y mejoras son bienvenidas 🚀

---

## 📜 Licencia

Este proyecto está bajo la licencia **MIT**. Puedes usarlo y modificarlo libremente.

