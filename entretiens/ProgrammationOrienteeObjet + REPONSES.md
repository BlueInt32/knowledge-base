####Quels sont les 3 fondamentaux de la Poo ?

*Encapsulation* : les objets sont définis dans des entités bien définies, dont l'accès à certaines fonctionnalités sont restreintes afin d'en garantir l'intégrité.
Abstraction : possibilité de définir des contrats de comportement, abstraits dans le sens où l'on ne veut pas savoir comment le contrat sera rempli
*Polymorphisme* : possibilité de définir une forme de nomenclature commune pour utiliser les fonctionnalités différentes. Le polymorphisme est mis en oeuvre à différents niveaux : surchage de fonction, génériques afin de rendre le typage paramétrique, déclaration d'un type parent ou abstrait pour l'utilisation d'un ou plusieurs de ses sous-types
*Héritage* : possibilité pour un type d'hériter des fonctionnalités d'un autre type, et de l'étendre.



####Quelle est la différence entre abstract et virtual ?
le mot clef abstract permet de définir une fonction comme devant être implémentée dans une classe fille. Une classe contenant une méthode abstraite doit être marquée comme abstraite. Hériter d'une classe abstraite, c'est donc devoir remplir le contrat de l'implémentation de ses méthodes ou propriétés. Une classe abstraite ne peut pas être instanciée.
Le mot clef virtuel signale au compilateur qu'une méthode peut être redéfinie dans une classe fille. Virtuel permet donc la notion d'implémentation par défaut, ouvrant la possibilité de donner un comportement plus spécifique aux classes filles.

####A quoi sert une interface ?
L'interface permet de définir un contrat de fonctionnalités pour les classes qui l'implémentent. On utilise les interfaces pour encapsuler les modules et les rendre interchangeables, un module interagissant avec un autre n'ayant comme référence que l'interface n'a pas besoin de savoir les détails d'implémentations ce qui est sain pour la maintenance et la souplesse des programmes.

####Qu’elle est la différence entre type valeur et type référence ?
Le type valeur n'a comme empreinte mémoire que la valeur directe dans la stack, alors que le type référence en a 2 : l'objet lui-meme dans le heap, et sa référence dans la stack.
La différence se trouve dans la manière dont ils sont gérés par le CLR lors de la copie ou lors du passage en paramètres d'une fonction. Le type valeur est transféré tel quel alors que le type référence est manipulé via sa référence. Cela est important quand on manipule un 

####Quelle est la différence entre une classe et un objet ?
La classe représente le prototype de création d'un objet : comment il sera construit, quels seront ses attributs et ses fonctionnalités. L'objet est l'instance d'une classe, il a été créé et sera détruit. On développe des classes qui instancient des objets.


####Citer 5 design pattern ? les expliquer
MVC : http://weblogs.asp.net/stephenwalther/the-evolution-of-mvc
Singleton : une seule instance
Factory : construction d'objet
Observer : gestion d'abonnement aux evenement d'un objet
Adapter : permet d'adapter un objet à une interface afin d'encapsuler un comportement a priori incompatible
Décorateur : ajouter des fonctionalités à un objet sans modifier cet objet.

####Qu’est-ce que le transtypage ?
C'est le fait de convertir un type dans un autre type compatible. Le transtypage peut etre implicite quand la conversion est validée comme ne pouvant pas impliquer de perte de données, par exemple de int vers float.
La conversion doit être explicite (cast) quand il y a potentiellement une perte de données.
