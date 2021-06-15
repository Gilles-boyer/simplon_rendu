## Factory Method :

> le design pattern Factory Method fournit une interface commune pour la création d’objets différents, qui partagent donc les mêmes fonctions.
> Exemple : 

- Le complexe loue un materiel sur circuit
- Sur le circuit, nous allons développé la logique location avec kart ou voiture
- le circuit souhaite maintenant loué des motos
- la location moto va obéir a d'autre contraintes (temps, entretien, licence, ...)
  
> On peut bidouller pour que le code fonctionne, mais que se passera t il le jour ou l'entreprise voudra louer autre chose (jetski,...)

### Solution le Design Pattern Factory Method

> Le design pattern Factory Method consiste à remplacer les appels à la construction d’objets à l’aide de l’opérateur  new  par l’appel d’une méthode spéciale (que l’on nomme souvent factory, bien que l’on puisse la nommer comme on le souhaite). Cette classe chargée de cette responsabilité est appelée Usine (ou "factory") et les objets créés sont souvent appelés "produits".
> La création des objets produits sont délégué à la factory
 ---------------------------------------
 >Exemple :
 ---------------------------------------
 > Interface Circuit
 > {
 >> public function locationMateriel();        
 > }

---------------------------------------

> class Kart implement Circuit {
> public function locationMateriel(){
> //...
> }
> }

--------------------------------------

> class Voiture implement Circuit {
> public function locationMateriel(){
> //...
> }
> }

---------------------------------------

----------- Design Pattern ------------
> interface MaterielLoue
> {
>>public function createMaterial():Circuit;
>>public function location(); 
> }
---------------------------------------
> abstract class AbstractMaterielLoue implements MaterielLoue
>{
>>abstract public function createMaterial : Circuit;
>> final public function location()
>>>{
>>>>$materiel = $this->createMaterial();   
>>>>return $materiel->locationMateriel();
>>>}
>}
---------------------------------------
>class KartMaterielLoue extends AbstractMaterielLoue
>>{
>>>public function createMaterial()
>>>>{
>>>>>return new Kart();
>>>>}
>>}
----------------------------------------
>Nous avons rendu notre système de location complètement indépendant de chaque materiel, et rendu possible l’ajout d’un nombre infini Materiel. Pour cela, il nous suffit de créer deux nouvelles classes : le type de Materiel et le MaterielLoue, dont il faudra seulement implémenter la méthode createMateriel.