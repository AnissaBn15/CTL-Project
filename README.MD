********************* PROJET DE SPECIFICATION ET RESOLUTION DE SYSTEMES CRITIQUES ********************
Projet Réalisé Par :
- BEN BOUDAOUD Anissa
- LAGHOUB Nassim


*********************************** POUR LANCER LE PROGRAMME *******************************************
Commencez par compiler : javac *.java
Ensuite, exécutez : java CTL_Main

À ce stade, vous devez entrer le nom du fichier « xxxx.txt » (situé dans le dossier "automates") à utiliser, avec l'automate correspondant. Par exemple, le fichier de base (par défaut) : « graph1.txt » correspond à la structure suivante :

states:
q1;
q2;
q3;
q4;

transitions:
q1 -> q2;
q2 -> q3;
q2 -> q4;
q4 -> q4;

labels:
q1 : "p q";
q2 : "p";
q3 : "q";

Vous avez la possibilité de créer vos propres automates (fichiers) que le programme pourra lire. Assurez-vous qu'un fichier soit valide en respectant la structure suivante :

Une ligne « states: » suivie, à chaque ligne suivante, du nom de l'état suivi d'un point-virgule, comme ceci : « e1; »

Une ligne « transitions: » suivie, à chaque ligne suivante, du nom de l'état de départ, puis d'une flèche ->, suivi du nom de l'état d'arrivée, avec un point-virgule à la fin comme ceci : « e1 -> e2; »

Une ligne « labels: » suivie, à chaque ligne suivante, du nom de l'état, suivi de deux points, suivi entre guillemets du nom des labels, séparés par des virgules s'il y en a plusieurs, avec un point-virgule à la fin comme ceci : « 1 : "q"; » ou « 2 : "p,q"; » en miniscule.

Assurez-vous que les informations récupérées par le programme (états, transitions et étiquettes) soient correctes. Ensuite, vous pouvez écrire une formule.

SAISIR UNE FORMULE
Pour saisir une formule, respectez la syntaxe suivante :


p = proposition, nom d'une étiquette (ex: a,b,p,q,r,x,y,z)
- = Not (Non)
& = And (Et)
| = Or (Ou)
> = Implication
? = Equivalence
E = Il existe
A = Pour Tout
X = Next (suivant)
F = Future (dans le futur)
G = Globally (Global)
U = Until
La syntaxe reconnue (f = formule) est la suivante :


p = proposition (ou étiquette), ex : « a,b,p,q,r,x,y,z »
-f = NOT f, ex : « -a,-b,-p,-q,-r,-x,-y,-z »
(f1&f2) = f1 AND f2, ex: « (a&b) » (Attention: parenthèses extérieures obligatoires)
(f1|f2) = f1 OR f2, ex: « (a|b) » (Attention: parenthèses extérieures obligatoires)
(f1>f2) = f1 IMPLIQUE f2, ex: « (a>b) » (Attention: parenthèses extérieures obligatoires)
(f1?f2) = f1 EQUIVALENT f2, ex: « (a?b) » (Attention: parenthèses extérieures obligatoires)
EXf = il existe NEXT f, ex: « EXa »
EFf = il existe FUTUR f, ex: « EFa »
EGf = il existe GLOBAL f, ex: « EGa »
E(f1Uf2) = il existe f1 UNTIL f2, ex: « E(aUb) » (Attention : parenthèses après le E obligatoires)
AXf = pour tout NEXT f, ex: « AXa »
AFf = pour tout FUTUR f, ex: « AFa »
AGf = pour tout GLOBAL f, ex: « AGa »
Vous pouvez également afficher les détails en tapant : « voirDetails ».

L'option « voirDetails » est utile pour consulter toutes les évaluations précédentes (les marquages récursifs intermédiaires inclus). Attention -> les détails fournis concernent toutes les anciennes formules tapées depuis le début (il faut quitter le programme pour vider cela).