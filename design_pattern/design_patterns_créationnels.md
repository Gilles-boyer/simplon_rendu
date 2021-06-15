# les design patterns créationnels :

> En programmation orientée objet, le code s’organise essentiellement autour de la création et la configuration des objets. Je vais exposer trois design patterns créationnels :

## Factory Method :

> le design pattern Factory Method fournit une interface commune pour la création d’objets différents, qui partagent donc les mêmes fonctions.
> Exemple : 

- Le complexe loue essentiellement un circuit
- Sur le circuit, nous allons développé la logique location avec kart ou voiture
- dans la location kart, nous retrouvon kart enfant ou adulte
- dans voiture : easydrift ou Rs
- le circuit souhaite maintenant loué des avions
- la location avions va obéir a d'autre contraintes (temps, entretien, licence, ...)
  
> On peut bidouller pour que le code fonctionne, mais que se passera t il le jour ou l'entreprise voudra louer autre chose (jetski,...)

### Solution le Design Pattern Factory Method

> Le design pattern Factory Method consiste à remplacer les appels à la construction d’objets à l’aide de l’opérateur  new  par l’appel d’une méthode spéciale (que l’on nomme souvent factory, bien que l’on puisse la nommer comme on le souhaite). Cette classe chargée de cette responsabilité est appelée Usine (ou "factory") et les objets créés sont souvent appelés "produits".
> La création des objets produits sont délégué à la factory