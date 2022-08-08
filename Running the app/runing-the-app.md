
# résumé.
>après avoir complété ce Markdown:
- vous devez etre capable d'accéder a votre instance EC2 en utilisant SSH, key et adresse IP fournies.
- vous pouver Lancer et interagir avec l'application d'apprés votre navigateur favorite.
- vous aurez accés à un autre markdown qui vous guide durant l'exploration du code source et sa documentation sur demande. 


## Contenu
* [SSH to your EC2 Instance](#ssh-to-your-ec2-instance)
* [Accéder au répertoire du Projet](#accéder-au-répertoire-du-projet)
* [Build le projet](#build-le-projet)
* [upload data vers elasticsearch](#upload-data-vers-elasticsearch)
* [ReBuild le projet](#rebuild-le-projet)
* [accés à l'application](#accés-à-l'application)



## SSH to your EC2 Instance
- Vos Credentials et IP respectives vous seront envoyés sur le chat
- Une clé SSH .pem vous sera transmise sur le chat
- username : `ec2-user`
- adresse ip : `adresse ip fournie`
- Se rendre dans le repertoire où vous  avez mis votre fichier pem
  Par exemple, si vous êtes sur windows et que vous l'avez mis dans le dossier téléchargements :

```
cd downloads
```
- et puis connectez-vous à l'instance EC2 :
 ```
ssh -i "cle-ssh.pem" ec2-user@ec2-addresse_ip.compute-1.amazonaws.com
```

## Execution du Script IP

Ce script met a jour votre IP publique dans l'application 

```console
cd /tmp
sudo chmod +x ip.sh
./ip.sh
```


## Arret des packages interferant:

- executer les deux commandes suivants.


```
sudo -i service elasticsearch stop
```

```
sudo -i service kibana stop
```

## Démarrage de Docker

```console
sudo service docker start
```

## Acceder au répertoire du Projet 

- Utiliser cette commande pour le faire.

```
cd Full-Text-Search-App-ES
```



## Build Docker & Run du Projet

- Utiliser cette commande pour le faire.

```
docker-compose up -d --build
```

## upload data vers elasticsearch 
- Utiliser cette commande pour le faire.

```
docker exec gs-api "node" "server/load_data.js"
```

## Re-Build le projet 

- Utiliser cette commande pour le faire.

```
docker-compose up -d --build
```

## accés à l'application 

1. Ouvrir votre navigateur favorite.
2. accéder à l'URL suivant :

```
http://votre.adresse.IP.amazon:5601
```
