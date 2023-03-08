# tp01

## Etape 5
```
docker run -v index.html:/usr/share/nginx/html -p 80:80 -d nginx
```

2. Editer le fichier html créé par nginx et y rajouter du HTML "maison" (Hello World dans notre cas)
3. Ouvrir l'URL "localhost:80" => TADAAAA


Avec docker cp
```
docker run -p 80:80 -d nginx
cp index.html e12:/usr/share/nginx/html
```

## Etape 6
```
docker build -t tp01 .
docker run -d -p 80:80 tp01
```
Avantage étape 6 : 
- on peut modifier le code source de l'application sans avoir à rebuild l'image docker
- Push l'image sur DockerHub et la récupérer sur un autre PC

## Etape 7
```
docker pull mysql:5.7
docker pull phpmyadmin/phpmyadmin
docker run -d -e MYSQL_ROOT_PASSWORD=root mysql:5.7
docker run -d -p 1234:80 phpmyadmin/phpmyadmin

- Accéder à phpmyadmin sur localhost:1234
- Se connecter avec root / root
```
## Etape 8
Créer le docker-compose.yml (voir sur github)
```
docker-compose up -d
```
- Accéder à phpmyadmin sur localhost:1234
- Se connecter avec root / root
- Accéder à la base
- Créer une table users
- Ajouter des utilisateurs (id, fistname, lastname)

a.
- Lancer plusieurs conteneurs d'un coup
- Plus simple pour gérer les variables d'environnement


b. 
- Utiliser des variables d'environnement
