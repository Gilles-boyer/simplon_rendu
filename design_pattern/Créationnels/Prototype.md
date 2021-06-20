# design pattern Prototype

>Parfois, la construction d’un objet peut prendre énormément de temps et de ressources, par exemple si elle fait appel à des fichiers, à des appels réseau ou encore à des informations que l’on retrouve en base de données. Par souci d’optimisation de performance, on peut préférer copier un objet existant et le modifier plutôt qu’en recréer un en partant de zéro.
>Le problème est que ce n’est pas si simple de copier un objet à l’identique !

> Pouvoir utiliser un objet, sans avoir à l'altérer, pourquoi pas créer un copie, mais comment ?

## Appliquez le design pattern Prototype

>Le design pattern Prototype (aussi appelé "Clone") consiste à permettre la copie d’un objet sans créer de dépendances fortes entre l’original et sa copie.
> Pour réalisé cet exploit nous allons délégué la création de l'objet  (clone) à lui même.

## Exemple

><?php

class Voiture
{
    private $color;

    public function getColor() 
    {
        return $this->color;
    }
    
    public function setTheme(Color $color)
    {
        $this->color = $color;
    }
    
    public function __clone()
    {
        // maintenant qu'il est différent
        // on pourra mettre à jour le theme seulement sur la copie
        $this->color = clone $this->color;
    }
}
------------------------------
<?php

class VoitureCloner
{
    public function cloneWithColor(Voiture $voiture, Color $color)
    {
        $newVoiture = clone $voiture;
        $newVoiture->setTheme($color);
        return $newVoiture;
    }
}

$voiture = new Voiture->createVoiture(/* ... */); // beaucoup d'opérations
$voitureCloner = new VoitureCloner();
$color = new Color('red'); // par exemple

$newVoiture = $voitureCloner->cloneWithTheme($voiture, $color);

var_dump($voiture->getTheme() === $newVoiture->getTheme()); // false