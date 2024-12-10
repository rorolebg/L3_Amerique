# Structure de la base de données (Geoffroy Zhang)
## Présentation du MCD
    - Inclure le schéma
    - Explication du choix des entités, de leurs attributs et de leurs relations
    - Explication des cardinalités
    - Utilisation des identifiants ARK comme clés primaires
## Dictionnaire des données
## Recodage des données
    - Siècles des éditions
    - Régions couvertes par les ouvrages
    - Fonctions/métiers des auteurs

# Structure de la base de données (Geoffroy Zhang)

Inventée par le mathématicien Edgar F. Codd, la base de données relationnelle se définie comme : "un ensemble structuré de données reliées entre elles et stockées de manière cohérentes, sans redondance inutile" (Marc Humbert, *Les bases de données*, Paris, Hermes, 1991). 
Notre base de données relationnelle se structure, comme toutes les bases, d'un ensemble de tables et de divers autres éléments que nous expliquerons ci-dessous.  

## Le modèle conceptuel des données (MCD) de notre corpus

**<ins>Schéma du MCD d'apès le corpus Amérique du catalogue de la BnF : </ins>**
![MCD_Corpus_Amérique](https://github.com/user-attachments/assets/9480eb4f-377d-4c63-b89c-f94cfed6cb01)

Le MCD est l'étape préalable à la conception d'une base de données. En effet, celui-ci nous a permis, dans le cadre de ce projet, de modéliser les données du corpus au sein d'une structure organisée qui indique différents éléments :
- Les **entités** : la chose que l'on décrit ;
- Les **attributs** : ce qui décrit ou caractérise une chose ;
- Les **relations** : les relaations entre les entités.

Le MCD est composé de : 
- Les **tables** ;
- Leurs **champs** ;
- Leur **type de donnée** (int, str, booléen); 
- Les **clés primaires** et **étrangères** ;
- Les **relations entre les tables** et leur **signification** ;
- Les **cardinalités**.

**<ins>Explication du choix des entités, de leurs attributs et de leurs relations :</ins>**

Tout d'abord nous avons identifié les entités, les attributs et leur relation, après l'analyse du corpus. Cette ébauche nous a permis de dresser notre MCD. Les entités sont représentées par des tables en forme de boîte aux angles à 90 degrés ; alors que les relations sont caractérisées par des boîtes aux angles plus arrondis et contiennent souvent des verbes (Ex. *Parle de* pour la relation de l'entité *TEXTE* et *SUJET_RAMEAU*). Ainsi, la base de données est composées de diverses tables ou entités que sont : les tables *EDITION*, *FONCTION*, *TEXTE*, *AUTEUR*, *FONCTION* et *ECRIT_PAR*. 

Le choix des entités a été le produit d'une réflexion en classe après avoir analyser la structure du corpus et le détail des ouvrages. En effet, chaque nom d'entité (Ex. TEXTE) caractérise l'élément que nous décrivons. L'entité TEXTE correspond à un texte de la base de données ; il est donc important de connaître son contexte d'édition d'où la relation *Publié dans* avec l'entité *EDITION*, en effet, on part du principe que chaque texte a été édité au moins une fois. 
Les attributs de l'entité *EDITION* permettent donc de connaître diverses informations sur la forme de l'ouvrage et son contenu. En effet, l'attribut  "Nb de pages" permet de savoir précisément le nombre de pages de l'ouvrage ce qui est intéressant si on essaie de situer le texte dans une certaine époque.  
L'entité *SUJET_RAMEAU* permet de décrire le sujet du texte, autrement dit savoir de quoi parle le texte (Ex. L'attribut "désignation" dans la table *SUJET_RAMEAU* permet de connaître l'intitulé précis du texte).  




Ces entités sont décritent par des champs (Ex. Titre). Autrement dit, le champ "titre" correspond au titre du texte qui correspond à l'entité *TEXTE*.  

Les identifiants Ark permettent de retrouver les éléments plus facilement. 

**<ins>Explication des cardinalités :</ins>**

Les cardinalités indiquent le nombre d'entités pouvant entrer en relation. 

**<ins>Utilisation des identifiants ARK comme clés priamires :</ins>**

La clé primaire est un champ qui doit être présent dans chaque table avec une numérotation unique. 
La clé étrangère est un champ qui fait référence à la clé primaire d'une autre table. 
On ne considère que le maximum. 

3 types principaux de cardinalité : 
1 : 1 = fusion des tables 
1 : n = deux tables séparées ; une clé étrangère nécessaire dans celle de l'entité ou de l'attribut multiple 
n : n = table de jonction 

## Dictionnaire des données 

Le dictionnaire des données est un référentiel d'informations relatif aux bases de données. Autrement dit, c'est une liste des informations que l'on veut enregistrer dans la base de données. C'est la description complète des chanps de chaque table (nom, type, description). Par exemple, dans notre MCD, le champ "Prénom" de la colonne "Auteur" a pour type un entier avec une description sur le nom de famille. 

## Recodage des données 

**<ins>Siècles des éditions :</ins>**

**<ins>Régions couvertes par les ouvrages :</ins>**

**<ins>Fonctions/métiers des auteurs :</ins>**
