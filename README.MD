
# Entrainement au Cherry-picking

### Contexte

Ce projet de test liste dans un fichier **auto.txt** des marques de voitures et dans **serie.txt** des titres de series.

Ce d�p�t poss�de deux branches : 

- master
- asie

### Objectif
La branche asie a �t� cr�� alors que la branche master ne poss�dait que les informations FR. (commit e73a02cb953af622260e31bb7467ebc56e0e1d41 )

On souhaitait ajouter sur la branche asie toutes les informations venant des pays d'Asie. Ca commen�ait bien avec le commit 98a412c22478fcd27e7db6fbacd3eebf8f2a3d05 pour la Cor�e.

Entre temps sur la master, d'autre personne ont remont�es les informations pour les US ( commit d7874788e38f183298f8395fcae6d6d5609d3b1d )
ainsi que pour le Japon ( commit eafcb727e92c036df38b57bb12d084e27eacdd71 ).

En r�alisant que sur le master les informations du Japon sont d�j� dispo, il faudrait les r�cup�rer sur la branche asie, sans pour autant r�cup�rer les informations US.

### Methode
Se mettre sur la branche o� l'on veut r�cup�rer les modifs:
`git checkout asie`

"Picorer" les modifications du commit qui nous int�resse:
`git cherry-pick eafcb727e92c036df38b57bb12d084e27eacdd71 `

R�soudre les �ventuels conflits et commit.