[![CircleCI](https://circleci.com/gh/eloirobe/mdas_mongodb.svg?style=svg)](https://circleci.com/gh/eloirobe/mdas_mongodb)

# MDAS NoSQL MongoDB
Bienvenidos a la imagen de MongoDB para a la asignatura de NoSQL del master [Máster en Desarrollo y Arquitectura de Software (MDAS)](https://www.salleurl.edu/es/estudios/master-en-desarrollo-y-arquitectura-software)

Para arrancar el MongoDB y empezar a utilizar la imagen de docker realizar lo siguiente:

*Requisitos previo tener instalado docker*

1) Clonar el repositorio
```bash
git clone https://github.com/eloirobe/mdas_mongodb.git
```
2) Arrancar la imagen de docker
```bash
cd mdas_mongodb
## En modo stdout
docker-compose up
## En modo silencioso
docker-compose up -d
```
3) Una vez haya arrancado loguearse en la console
```bash
docker-compose exec mongo bash
```
4) Importar la base de datos de test
```bash
mongoimport --db test --collection restaurants --drop --file /dataset/restaurants.json
```
- Deberia devolver algo parecido:
```bash
2019-04-28T15:26:24.535+0000	connected to: localhost
2019-04-28T15:26:24.536+0000	dropping: test.restaurants
2019-04-28T15:26:25.639+0000	imported 25359 documents
```


## Dataset Utilizados

- [https://raw.githubusercontent.com/mongodb/docs-assets/primer-dataset/primer-dataset.json](https://raw.githubusercontent.com/mongodb/docs-assets/primer-dataset/primer-dataset.json)