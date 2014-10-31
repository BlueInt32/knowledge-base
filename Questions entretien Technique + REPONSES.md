#General


# Programmation orientée objet
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



# C&#35; / .NET 

###Questions générales
####Quelle est la différence entre les versions 2.0 / 3.5 / 4.0 de .NET ?
2.0 a apporté une nouvelle version du CLR avec notemment le support des generics
3.5 a essentiellement apporté (avec la 3.0) wpf, wcf et wwf et LINQ
4.0 coté web 
####Quelle version du framework préférez-vous ? 
La dernière :)

### Language C&#35;
#####Quelle est l'utilité de using ? 
La directive using sert à éviter l'écriture d'un namespace qualifié dans un fichier pour chaque utilisation d'une de ses classes. On peut également créer un alias de ce namespace.
using peut également être utilisée dans un bloc de code pour assurer la bonne utilisation d'un type implémentant IDisposable.

####A quoi servent les mots clef is et as ?
Is sert à tester le type d'une variable, assurant que le cast ne remontera pas d'exception.
As permet de caster une variable vers un type sans remontée d'exception en cas d'erreur. La variable sera null dans ce cas.


####Qu’est-ce qu'une classe générique ?
Les classes génériques sont des templates de classes agissant sur un ou plusieurs types non définis, évitant au développeur d'avoir à dupliquer certaines fonctionnalités similaires, n'ayant comme variation qu'un ou plusieurs types manipulés par la classe générique.
Une classes générique prend un ou plusieurs paramètres de types qu'elle manipule, pour permettre de différer la spécification de ces types au moment de la déclaration et de l'instanciation. On aura ainsi la possibilité de n'écrire qu'une classe manipulant de manière similaires plusieurs types différents.

####Qu’est-ce qu’un delegate ? A quoi ça peut servir ? Et une lambda expression ?
C'est un pointeur de fonction. Il peut être typiquement utilisé en tant que handler d'evenement, ou dans le cadre d'utilisation de requetes LINQ pour effectuer facilement des actions sur des collections. Depuis la version 3 de .net on peut utiliser les expressions lambda qui encapsulent les delegates dans une syntaxe particulière. 
Le delegate est une notion qu'on rencontre beaucoup en javascript.

####Comment fonctionnent Async, await, Task ?
http://msdn.microsoft.com/en-us/magazine/jj991977.aspx
http://msdn.microsoft.com/en-us/library/hh191443.aspx

#### Quels sont les différents niveaux d'encapsulsation en .NET ? A quoi servent-ils ?
public private protected internal, que fait "protected internal" ?



### LINQ
#### Etes-vous à l'aise en LINQ ?

####Comment fait-on un left outer join en LINQ ?
????

#### Connaissez-vous la fonction Aggregate de LINQ ? Pourriez-vous me montrer comment elle fonctionne ("juste la lambda expression") ?

# Méthodologies / Développement
#### Pouvez-vous me dire ce qu'est l'intégration continue ? Ce qu'elle apporte ?


# ASP.NET Webforms/MVC
#### Très succintement, pouvez-vous différencier le déroulement d'une requete serveur en ASP.NET webform et en ASP.NET MVC ?

## ASP.NET MVC
#### Qu'est-ce qu'une vue partielle ? A quoi cela correspond-il en webform ?
#### Comment définit-on une vue partielle ?


#### Savez-vous ce qu'est un editor template ? Quel est la différence avec une vue partielle ?


# Web / Front
#####Que signifient les codes HTTP 404, 301, 302, 500, 200 ? 
404 : page introuvable, 301 : redirection temporaire
500 erreur serveur,
200 ok

####Comment te sens-tu sur HTML/CSS ?
J'ai voulu pendant un temps être designer, j'en suis revenu mais aujourd'hui j'estime qu'un développeur de sites web asp.net ne peut plus faire l'impasse sur les langages déclaratifs front. Les codes métiers ont tendance à se déporter coté client, et comme j'ai mis le pieds dans le framework angular JS, avec LESS comme préprocesseur ce monde ne me fait pas peur.


# SQL Server

####Différences entre inner join et left join, éventuellement donner un exemple
####A quoi sert une procédure stockée ? Dans quel contexte peut-on préférer mettre des fonctionnalités dans la bdd plutot que coté objet ? (infrastructure)
####Quelles sont les différences entre truncate table et delete from
####quels sont les différents types de tables temporaires ? (tables préfixées avec #, @, ...)
####(pas posée car j'en ai parlé avant) Qu'est-ce qu'un trigger ?

####SQL, no lock ? comment il est utlisé dans un select ?
Le nolock signale au moteur qu'il n'a pas à attendre qu'une eventuelle transaction soit commitée avant de lire les données. Cela peut donc économiser de la resource systême, mais on risque de lire des données "sales" pouvant faire l'objet d'un rollback de transaction.
`Select * from dbo.product(nolock)` ou `Select * from dbo.product with (NOLOCK)`


> Question similaire : différence entre `Select * from tableA` et `Select * from tableB(nolock)` ?

#### Que retournerait cette requete : select top 1 * from Product order by newid() ?
Retourne un élément de la table Product au hasard.

#### Comment copier/coller les données d’une table source vers une table cible qui fait 800 000 lignes ?
Si la table n'est pas vraiment énorme, l'utilisation de la requete 
Select * into dbo.newTable from dbo.Product peut suffire (il faudra recréer les contraintes et indexes)
En changeant le Recovery mode à Bulk_logged, on minimise la création de logs et on peut gagner beaucoup de temps sur la requete.

#### Corriger la requête suivante 
`Delete * from TableA where ename = ‘toto’`

L'étoile ne sert à rien, car on supprime toute la ligne de toute façon.

#### Comment lister les indexes d’une table donnée ?
Il faut requeter la table sys.indexes avec object_id= object_id('nomtable') 

#### Comment écrit-on un curseur ?

#### Comment écrit-on un trigger ?


# Test Papier
####Soit la suite de Fibonnacci (1 1 2 3 5 8 13...) N(i) = N(i-2) + N(i-1). Coder la fonction N(i) (avec stylo et papier, en langage parlé, ou c#, comme on veut)




# A trier

### C&#35;
####qu'est-ce que l'héritage ? 
####différences entre overloading et overriding ?
####si une classe mère est développée dans une assembly non modifiable et que je veux redéfinir une méthode dans une classe fille, comment faire ? (mot clef new)
####à quoi sert une interface ?
####Qu'est-ce qu'une shallow copy ?
####Qu'est-ce qu'un type générique ?
####quelle est la différence entre les mots clef c# var et object ?
####Qu'est-ce qu'une lambda expression ? Dans quel contexte l'utilise-t-on souvent ? 
####Avez-vous déjà utilisé les types anonymes ?
####avez-vous déjà utilisé le type dynamic ? 
####savez-vous pourquoi on dit que le xmlserializer n'est pas très optimisé ?
####quelle est la différence entre web.config et global.asax ?
####comment définit-on les routes en asp.net MVC?

### Architecture :
####qu'est-ce qu'une architecture N-Tiers ?
####que savez-vous de MVVM ? Databinding, etc...
####Quels design patterns connaissez-vous ? Fatalement, on évoque le singleton, quel est le point auquel il faut faire attention avec ce pattern ? (thread lock)

### Services :
####qu'est-ce qu'une architecture orientée service ? (ça a semblé bien d'évoquer le parallèle avec la notion de bonne conception avec utilisations d'interfaces)
####qu'est-ce que REST ?
####pourquoi utiliserait-on plutot une approche REST ou une approche Soap ?

### JS / AngularJS / Jquery :
####comment est organisée une application angular ? 
####comment définit-on une directive ? 
####comment peut-on comparer jquery et AngularJS, que pouvez-vous dire sur l'un par rapport à l'autre ?
####notion de templates / directive ? parallèle avec .net (user controls, custom controls, component)
####comment définit-on les routes en angularJS ? Comment définit-on des paramètres dans le routing


#### Qu'est-ce que le DependencyResolver ?
#### Qu'est-ce que le type WebViewPage<T> en ASP.NET MVC ?
Definir un helper du genre @MaMethodeDirecte() : 
    public abstract class WebViewPage<TModel> : System.Web.Mvc.WebViewPage<TModel>
    {
	    public MvcHtmlString T(string ressourceKey, params object[] parameters)
	    {
	    var applicationContext = DependencyResolver.Current.GetService<IApplicationContext>();
	    
	    return new MvcHtmlString(applicationContext.GetMessage(ressourceKey, parameters));
	    }
    }
