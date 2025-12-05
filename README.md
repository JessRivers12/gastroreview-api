# API Gateway - GastroReview

Gateway de enrutamiento para todos los microservicios de GastroReview.

## 🚀 Tecnologías

- Java 21
- Spring Boot 3.3.3
- Spring Cloud Gateway
- Spring Cloud Netflix Eureka Client
- Maven

## 📦 Compilar

```bash
mvn clean package -DskipTests
```

## ▶️ Ejecutar Localmente

```bash
mvn spring-boot:run
```

## 🌐 Puerto

Este servicio corre en el puerto **8080**.

## 🔧 Configuración para Render

### Build Command
```
mvn clean package -DskipTests
```

### Start Command
```
java -jar target/*.jar
```

### Variables de Entorno
```
EUREKA_CLIENT_SERVICEURL_DEFAULTZONE=https://gastroreview-eureka.onrender.com/eureka/
JAVA_OPTS=-Xmx512m -Xms256m
PORT=8080
```

## 🔀 Rutas

El API Gateway enruta las peticiones a:
- `/users/**` → Users Service
- `/restaurants/**` → Restaurants Service
- `/reviews/**` → Reviews Service
- `/graphql` → Reviews Service (GraphQL)

## 📝 Notas

- Despliega DESPUÉS de Eureka Server
- Requiere la URL de Eureka para funcionar
- Es el punto de entrada principal a la aplicación

## 🔗 Enlaces

- [Spring Cloud Gateway](https://spring.io/projects/spring-cloud-gateway)
- [Documentación Spring Boot](https://spring.io/projects/spring-boot)
