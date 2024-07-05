[FR] 

instancesGenerator (alpha) permet de générer des instances json de test conformes au schéma d'interopérabilité OPSSIES-V2 v013.
L'outil est mis à disposition à titre introductif.

Téléchargement
==============

instancesGenerator est téléchargeable à l'adresse suivante :
https://opssies.github.io/v013/opssiesToolkit/opssiesToolkit.zip

Installation
============

-- Linux --

Exécuter les commandes suivantes depuis un terminal :

[pour décompresser le fichier "Opssies.zip" dans un répertoire de votre choix]
1. unzip Opssies.zip -d destination_folder 

[Pour décompresser le fichier "Opssies.zip" dans le répertoire courant]
1. unzip Opssies.zip 

[Accès au répertoire Opssies]
2. cd Opssies

[Installation du module Opssies]
3. perl Makefile.PL
4. make
5. make install

Note : 
- cette version du dispositif repose sur le langage Perl (version 5.38).
- l'installation du module peut nécessiter des droits en écriture réservés au compte root ou assimilé.


-- Windows --

L'installation dans cet environnement n'a pas été testée, mais est possible (via Strawberry Perl ou ActiveState Perl).


Usage
=====

[Editer le script app_instancesGenerator.pl via l'éditeur de votre choix]
Préciser le nombre (N) d'instances à générer : CaRED1SampleGenerate(N)

Note : 
- l'appel de la fonction "print" interroge le module Opssies et sa méthode CaRED1SampeGenerate
- des méthodes complémentaires sont prévues, couvrant d'autres profils


Evolutions
==========

- La version actuelle génére des données (FINESS, SIREN, qualifiants D1) pour une structure prédéfinie.
- Une version couvrant le volet multi-événementiel pourrait être proposée, en cohérence avec le dispositif instancesChecker (à venir).






