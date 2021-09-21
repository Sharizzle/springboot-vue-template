# Vue 3 & Java Spring Boot Template

### Technologies

- Java 8+
- Node.js
- Maven
- Spring Boot
- Vue 3
- Postgres SQL
- Spring Boot Dev Tools
- Babel
- Core JS
- Spring Data JPA
- Lombok

## Monolothic Build Order

Maven is configured to compile and build the Vue 3 as a part of the end `.jar` file.

1. Maven will run `npm install` and `npm build`
2. The output is stored in `/src/js/dist`
3. A Maven plugin will copy the `dist` folder to the `target/classes/static` folder
4. Maven will package the app in a `.jar` file

## Development

During development, run a terminal instance that will serve the local vue dev server using

```bash
npm run serve
```

and run the 

```java
TemplateApplication.main() 
```
function as usual.

## Build to Production

To build to production simply run

```bash
mvn clean package
```

and a `.jar` file will be produced.