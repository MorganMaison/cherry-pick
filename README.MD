
# Entrainement au Cherry-picking

### Contexte

Ce projet de test liste dans un fichier **auto.txt** des marques de voitures et dans **serie.txt** des titres de series.

Ce dépôt possède deux branches : 

- master
- asie

### Objectif
La branche asie a été créé alors que la branche master ne possédait que les informations FR. (commit e73a02cb953af622260e31bb7467ebc56e0e1d41 )

On souhaitait ajouter sur la branche asie toutes les informations venant des pays d'Asie. Ca commençait bien avec le commit 98a412c22478fcd27e7db6fbacd3eebf8f2a3d05 pour la Corée.

Entre temps sur la master, d'autre personne ont remontées les informations pour les US ( commit d7874788e38f183298f8395fcae6d6d5609d3b1d )
ainsi que pour le Japon ( commit eafcb727e92c036df38b57bb12d084e27eacdd71 ).

En réalisant que sur le master les informations du Japon sont déjà dispo, il faudrait les récupérer sur la branche asie, sans pour autant récupérer les informations US.

### Methode
Se mettre sur la branche où l'on veut récupérer les modifs:
`git checkout asie`

"Picorer" les modifications du commit qui nous intéresse:
`git cherry-pick eafcb727e92c036df38b57bb12d084e27eacdd71 `

Résoudre les éventuels conflits et commit.