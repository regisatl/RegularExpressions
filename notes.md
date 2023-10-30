Les expressions régulières, également appelées regex, sont des séquences de caractères qui forment un motif de recherche permettant de trouver des correspondances dans des chaînes de texte. Voici quelques expressions régulières couramment utilisées avec des exemples dans chaque cas :

1. **Correspondance de caractères simples :**
   - **Expression régulière :** 
     - `a` : Recherche du caractère 'a' dans une chaîne.

2. **Classes de caractères :**
   - **Expression régulière :**
     - `[aeiou]` : Correspond à n'importe quelle voyelle.
     - `[0-9]` : Correspond à n'importe quel chiffre.
  
3. **Quantificateurs :**
   - **Expression régulière :**
     - `a+` : Correspond à une ou plusieurs occurrences de 'a'.
     - `a*` : Correspond à zéro ou plusieurs occurrences de 'a'.
     - `a?` : Correspond à zéro ou une occurrence de 'a'.

4. **Ancrage :**
   - **Expression régulière :**
     - `^a` : Correspond à 'a' au début de la chaîne.
     - `a$` : Correspond à 'a' à la fin de la chaîne.

5. **Métacaractères :**
   - **Expression régulière :**
     - `.` : Correspond à n'importe quel caractère sauf le saut de ligne.
     - `\d` : Correspond à un chiffre (équivaut à `[0-9]`).
     - `\w` : Correspond à un caractère alphanumérique (équivaut à `[a-zA-Z0-9_]`).
     - `\s` : Correspond à un espace, tabulation ou saut de ligne.
  
6. **Groupes et Alternatives :**
   - **Expression régulière :**
     - `(abc)` : Groupe correspondant à la séquence 'abc'.
     - `a|b` : Correspond à 'a' ou 'b'.

7. **Quantificateurs spécifiques :**
   - **Expression régulière :**
     - `a{3}` : Correspond à exactement trois occurrences de 'a'.
     - `a{2,4}` : Correspond à deux, trois ou quatre occurrences de 'a'.

8. **Échappement :**
   - **Expression régulière :**
     - `\.` : Recherche du caractère point (utilisation du backslash pour échapper le caractère spécial).

Exemples :
- Pour une expression régulière `a*`, elle correspondra à des chaînes telles que : "", "a", "aa", "aaa", etc.
- L'expression régulière `[0-9]+` correspondra à des séquences de chiffres tels que "123", "9", "4567", mais pas à "abc".
- Avec l'expression `^a`, on trouvera une correspondance pour "abc" mais pas pour "bac".

Ces exemples représentent une base des expressions régulières, mais il existe de nombreuses autres combinaisons et possibilités en fonction des besoins spécifiques de recherche de motifs dans les chaînes de texte.

Les expressions régulières (regex) sont des séquences de caractères qui forment des motifs de recherche. Elles sont largement utilisées pour la validation, la recherche, et la manipulation de chaînes de caractères. Voici une liste des métacaractères et des exemples d'utilisation :

1. **Les caractères littéraux :**
   - Les caractères littéraux correspondent à eux-mêmes. Par exemple, l'expression régulière `/hello/` correspondra à la chaîne de caractères "hello".

2. **Les métacaractères :**
   - **Point (.) :** Correspond à n'importe quel caractère sauf les sauts de ligne. Par exemple, `/h.t/` correspondra à "hat", "hot", "hit", etc.
   - **Ancre de début (^) :** Utilisé pour indiquer le début d'une chaîne. Par exemple, `/^hello/` correspondra à une chaîne commençant par "hello".
   - **Ancre de fin ($) :** Utilisé pour indiquer la fin d'une chaîne. Par exemple, `/world$/` correspondra à une chaîne se terminant par "world".
   - **Classe de caractères ([ ]) :** Correspond à n'importe quel caractère contenu dans les crochets. Par exemple, `/gr[ae]y/` correspondra à "gray" ou "grey".
   - **Classe de caractères négative ([^ ]) :** Correspond à tout ce qui n'est pas dans la classe. Par exemple, `/[^0-9]/` correspondra à tout sauf des chiffres.
   - **Quantificateurs (*, +, ?) :**
     - **Étoile (*) :** Correspond à zéro ou plusieurs occurrences de l'élément précédent. Par exemple, `/go*d/` correspondra à "god", "good", "gooood", etc.
     - **Plus (+) :** Correspond à une ou plusieurs occurrences de l'élément précédent. Par exemple, `/go+d/` correspondra à "good", "gooood", mais pas à "god".
     - **Point d'interrogation (?) :** Correspond à zéro ou une occurrence de l'élément précédent. Par exemple, `/colou?r/` correspondra à "color" ou "colour".

3. **Les groupes et les captures :**
   - **Parenthèses ( ) :** Utilisées pour grouper des éléments. Par exemple, `/(ab)+/` correspondra à "ab", "abab", "ababab", etc.
   - **Références arrière (\1, \2, etc.) :** Permet de faire référence aux groupes capturés. Par exemple, `/([0-9])\1/` correspondra à des doublons de chiffres consécutifs comme "11", "22", etc.

4. **Échappements :**
   - **Antislash (\) :** Utilisé pour échapper les métacaractères. Par exemple, `/\./` correspondra à un point.

5. **Modificateurs :**
   - **i (insensible à la casse) :** Permet de faire une recherche insensible à la casse. Par exemple, `/hello/i` correspondra à "hello", "Hello", "HELLO", etc.
   - **g (global) :** Cherche toutes les occurrences, pas seulement la première.

6. **Exemples supplémentaires :**
   - **Courrier électronique :** `/[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}/` pour valider un format d'adresse e-mail.
   - **Numéro de téléphone :** `/\(\d{3}\)\s*\d{3}-\d{4}/` pour un format de numéro de téléphone comme (123) 456-7890.

Il est essentiel de noter que les expressions régulières peuvent varier en fonction du langage de programmation ou de l'outil utilisé. Chaque langage a sa propre implémentation des expressions régulières.


Voici les expressions régulières qui peuvent être utilisées pour valider les différentes entrées :

## Réponses :

### Question 1 : Validation d'une adresse email
Expression régulière : 
```regex
^[a-zA-Z0-9.%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,3}$
```
Cette expression régulière valide une adresse email standard. Elle commence par une série de lettres, de chiffres, de points, de pourcentages ou de tirets, suivis par le symbole "@", et se termine par un nom de domaine valide.

### Question 2 : Validation d'un numéro de téléphone au format américain
Expression régulière :
```regex
^\(?\d{3}\)?[-.\s]?\d{3}[-.\s]?\d{4}$
```
Cette expression régulière valide un numéro de téléphone au format américain, qu'il soit écrit comme "(123) 456-7890", "123-456-7890", "123 456 7890" ou "123.456.7890".

### Question 3 : Validation d'une adresse IP au format IPv4
Expression régulière :
```regex
^((25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$
```
Cette expression régulière valide une adresse IP au format IPv4 comprise entre 0.0.0.0 et 255.255.255.255.

### Question 4 : Validation d'un code postal au format américain
Expression régulière :
```regex
^\d{5}(-\d{4})?$
```
Cette expression régulière valide un code postal au format ZIP standard (par exemple, "12345") ou au format ZIP+4 (par exemple, "12345-6789").

### Question 5 : Validation d'une date au format "YYYY-MM-DD"
Expression régulière :
```regex
^(19|20)\d{2}-(0[1-9]|1[0-2])-(0[1-9]|[12]\d|3[01])$
```
Cette expression régulière valide une date au format "YYYY-MM-DD", où l'année est entre 1900 et 2099, le mois est entre 01 et 12, et le jour est approprié pour chaque mois (par exemple, 01 à 31).

Ces expressions régulières peuvent être utilisées pour valider les formats spécifiques mentionnés dans chaque question. Elles peuvent être intégrées dans du code pour la validation des données.