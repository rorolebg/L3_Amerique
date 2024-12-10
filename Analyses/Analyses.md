    Analyses (Damien Vandenheede)

   ## Structure du corpus (détailler le nombre de livres par siècle, le nombre de livres par région)
   
Afin de constituer notre corpus nous avons pris les informations sur le site de la Bibliothèque Nationale de France (BNF). Dans le but de mieux analyser les données nous avons répertorié les ouvrages en fonction du nombre de livres qui ont été publié par siècle. Nous pouvons voir qu'il y a plus de livres au cours du XIXe siècle. Nous ne devons néanmoins pas négliger la période précédente qui est très importante pour la naissance des États-Unis.
    
  ## Importance du XIXe
  
L'augmentation du nombre de livre portant sur les États-Unis en France au XIXe siècle s'explique par le fait qu'il y a une amélioration de l'alphabétisation qui est principalement due aux lois Ferry entre 1880 et 1881 pour rendre l'école gratuite et obligatoire jusqu'à l'âge de treize ans. Nous pouvons voir une multiplication des livres petits formats qui font parfois quelques dizaines de pages qui sont destinés aux plus pauvres. Un livre avec 
plusieurs centaines de pages restent assez coûteux au XIXe siècle. 
  

## Importance des Etats-Unis
Nous avons décidé d'étudier la vision que les Français ont des États-Unis. Le lien entre ces deux pays est important. En effet, la France sous Louis XVI a aidé les insurgés dans leur lutte contre la Grande-Bretagne pour leur indépendance. La France est l'une des première à avoir reconnu l'indépendance des États-Unis. Quand Benjamin Franklin, l'un des Pères fondateurs est venu en France pour voir Louis XVI et s'allier avec le roi. Ce dernier a permis que l'on traduise en français, que l'on fasse imprimer et que l'on diffuse la déclaration d'indépendance de juillet 1776. Il est important de souligner que normalement la censure aurait interdit ce texte qui critique le régime monarchique. La déclaration a une grande influence en France. Elle inspire les révolutionnaires français comme par exemple Brissot qui est un fervent défenseur de la Révolution américaine. Les États-unis et la France gardent de bonnes relations, au fil des décennies et des siècles les États-Unis se développe et devienne une puissance importante qui rivalise avec les pays européens et qui fascine ces derniers. C'est pour cela que nous nous sommes intéressés à la vision que les Français avaient des États-Unis.


Nous avons créé une base de données afin de pouvoir analyser, grâce à des requêtes SQL, la matérialité des livres. 

Nous avons calculé le nombre de pages moyen des livres écrits entre le XVIIe et le XXe siècle grâce à la requête suivante :
`SELECT AVG(Nb_pages) AS "Nb de pages moyen" FROM EDITIONS WHERE Nb_pages IS NOT NULL`

Nous pouvons voir que le nombre moyen de pages est de 251 pages en moyenne. Un livre de 251 pages est relativement important pour cette période. Cela nous montre l'importance des États-Unis pour les Français.

Nous avons calculé le nombre de pages moyen par ouvrages et par siècle grâce à la requête suivante : 

`SELECT Siecle_edition, AVG(Nb_pages) AS "Nb de pages moyen" FROM EDITIONS WHERE Nb_pages IS NOT NULL GROUP BY Siecle_edition`

| Siècle | Nombres moyen de pages |
| ---------- | -------------|
| XVIIe |320|
|XVIIIe|224|
|XIXe|247|
|XXe|293|


Nous pouvons voir qu'il y a une diminution du nombre moyen de pages puis une augmentation. Nous pouvons interprêter cela de plusieurs manières : premièrement nous l'avons vu il y a une amélioration de l'alphabétisation de la population, les plus pauvres ne pouvaient se procurer que des livres avec peu de pages. Deuxièmement, l'augmentation du nombre de pages au XXe siècle s'explique par le fait que les États-Unis est une puissance importante qui continue de fasciner les Européens et surtout les Français. Ce ne sont que des suppositions, nous ne pouvons pas connaître les causes de ces évolutions.



    Présence d'illustrations

    Analyse des auteurs

    Evolution des fonctions

    Auteurs presque exclusivement masculins

    Focus sur les ouvrages parlant des Etats-Unis au XIXe

    Analyse des régions (via les sujets)
    Evolution de l'intérêt pour certaines régions au fil des siecles 

    |Région |16|17|18|19|20|NULL|TOTAL|
    |----|----|----|----|----|----|----|----|
    |Antilles ou Amérique Latine| |18,18%|17,07%|1,43%| | |4,59%|
    |Canada| |45,45%|7,32%|14,29%|4,35%| |14,43%|
    |Est Etats-Unis|100%| |26,83%|11,90%| |12,50%|12,46%|
    |Louisiane| |4,55%|19,51%|4,29%|13,04%| |6,89%|
    |NULL| |31,82%|29,27%|53,33%|60,87%|75%|49,51%|
    |Ouest Etats-Unis| | | |14,76%|21,74%|12,50%|12,13%|
    |TOTAL|100%|100%|100%|100%|100%|100%|100%|
    
