# tp01

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
