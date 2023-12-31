# Challenge

## Repositorios del resultado

| No. | Repositorio                                                                       | Puerto | URL                    | Lenguaje    | Framework     | 
|:---:|-----------------------------------------------------------------------------------|:------:|------------------------|:-----------:|:-------------:|
| 1   | [Back End](https://github.com/gdayramirezdev/test-api.git)                        | 3001   | http://localhost:3001  | Typescript  | ReactJS(vite) |
| 2   | [Front End](https://github.com/gdayramirezdev/test-app.git)                       | 5173   | http://localhost:5173  | Typescript  | Express       |

#### Agrego instrucciones para lanzar imagen de mysql en docker (si es necesario)*
```bash
docker run --name mysql -d     -p 3306:3306     -e MYSQL_ROOT_PASSWORD=password     --restart unless-stopped     mysql:8
```

```bash
docker exec -it mysql mysql -p
```

Ingresar contraseña del usuario en mysql: password

#### Instrucciones para cargar base de datos

Crear base de datos:

```sql
create database test;
```

```sql
use test;
```

Crear tabla blogs

```sql
CREATE TABLE blogs (
  id MEDIUMINT NOT NULL AUTO_INCREMENT,
  title varchar(200) NOT NULL,
  autor varchar(200) NOT NULL,
  publishAt DATETIME NOT NULL,
  content TEXT NOT NULL,
  PRIMARY KEY (id)
);
```

Insertar un registros de prueba

```sql
INSERT INTO blogs (title, autor, publishAt, content) VALUES ('Titulo de prueba', 'Autor de prueba', '2022-04-23 10:34:53.4', 'Contenido restringido al publico');
INSERT INTO blogs (title, autor, publishAt, content) VALUES ('Foo', 'Bar', '2022-04-22 10:34:53.4', 'Este es un ejemplo que tiene mas de 30 chars y que es posible ocultar y mostrar su contenido desde la inferfaz, solo para probar la funcionalidad');
```

#### Instrucciones para lanzar API

Clonar repositorio del API
```bash
  git clone https://github.com/gdayramirezdev/test-api.git
  cd test-api
  npm install
```

Crear archivo .env en raiz del proyecto test-api

```ini
DB_HOST=localhost
DB_USER=root
DB_NAME=test
DB_PASSWORD=password
```

Lanzar API

```bash
  npm run dev
```

#### Instrucciones para lanzar APP

Ejecutar front end
```bash
  git clone https://github.com/gdayramirezdev/test-app.git
  cd test-app
  npm install
  npm run dev
```

ir a http://localhost:5173/
