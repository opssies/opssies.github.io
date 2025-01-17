[FR] 

OpssiesD1JsonSchemaValidator (alpha) permet à un industriel de contrôler, en amont de toute émission de données et en autonomie, la validité générale d'une instance json produite sur la base du schéma d'interopérabilité OPSSIES-V2 v013 décliné pour le D1, hors volet sémantique.
L'outil est mis à disposition des industriels à titre indicatif.

Téléchargement
==============

OpssiesD1JsonSchemaValidator est téléchargeable à l'adresse suivante :
https://opssies.github.io/v013/OpssiesD1JsonSchemaValidator/OpssiesD1JsonSchemaValidator.zip

Installation
============

-- Linux --

Exécuter les commandes suivantes depuis un terminal :

[pour décompresser le fichier "OpssiesD1JsonSchemaValidator.zip" dans un répertoire de votre choix]
1. unzip OpssiesD1JsonSchemaValidator.zip -d destination_folder 

[Pour décompresser le fichier "OpssiesD1JsonSchemaValidator.zip" dans le répertoire courant]
1. unzip OpssiesD1JsonSchemaValidator.zip 

[Accès au répertoire OpssiesD1JsonSchemaValidator]
2. cd OpssiesD1JsonSchemaValidator

[Installation du module OpssiesD1JsonSchemaValidator, depuis le répertoire des ressources à installer]
3. cd OpssiesD1JsonSchemaValidator
3. perl Makefile.PL
4. make
5. make install

Note : 
- cette version du dispositif repose sur le langage Perl (version 5.38).
- l'installation du module peut nécessiter des droits en écriture réservés au compte root ou assimilé.


-- Windows --

L'installation dans cet environnement n'a pas été testée, mais est a priori possible (via Strawberry Perl ou ActiveState Perl).


Usage
=====

-- Linux --

Une fois le module installé, exécuter la commande suivante depuis un terminal, dans le répertoire retenu (incluant les ressources json) :

perl OpssiesD1JsonSchemaValidator.pl --schema schema-d1.json --instance instance-d1.json

Les deux arguments attendus sont ici respectivement introduits par "--schéma" et par "--instance". 
Le schéma utilisé ici est une déclinaison simplifiée du schéma général, dédiée à la transmission d'éléments (dont certains sont obligatoires, et d'autres, optionnels) pour le programme CaRe D1.

A titre indicatif, trois instances-exemples sont fournies, en complément de l'instance "illustrative" (instance-d1.json) valide :

COMPANY-D1-20250101-101520 : instance correcte
COMPANY-D1-20250101-101521 : instance incorrecte (anomalie d'encodage UTF-8)
COMPANY-D1-20250101-101522 : instance incorrecte (anomalie sur un type d'objet)

Evolutions
==========

- L'inclusion de clauses de contrôle sur le volet sémantique est envisagée. Il est rappelé que les instances de "test" doivent impérativement répondre aux conventions rappelées dans la documentation (https://opssies.github.io/v013/introduction_care_d1.html - étape 5) et le cahier des charges CaRE D1.





