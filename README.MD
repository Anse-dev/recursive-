# Algorithme de Vérification de Palindrome

## Description

Cet algorithme vérifie si un mot donné est un palindrome. Un palindrome est un mot qui se lit de la même manière de gauche à droite et de droite à gauche (par exemple, "radar", "level", "deed").

## Utilisation

Pour utiliser cet algorithme, appelez la fonction `IsPalindrome` avec un mot en tant qu'argument. La fonction renverra `TRUE` si le mot est un palindrome et `FALSE` sinon.

```plaintext
ALGORITHME palindrome
VAR
   word: STRING
BEGIN
  Écrire(IsPalindrome(word));
END
```

## Fonction IsPalindrome

```
FONCTION IsPalindrome(word: string) : boolean
VAR
    length: entier
BEGIN
    length = longueur(word)

    SI length <= 1
        RETOURNER VRAI
    FIN SI

    SI word[0] != word[length - 1]
        RETOURNER FAUX
    FIN SI

    RETOURNER IsPalindrome(SousChaine(word, 2, length - 2))
END

```

## Fonction SousChaine

```
FONCTION SousChaine(word: string, start: entier, length: entier) : string
VAR
    result: string
    i: entier
BEGIN
    result := ""
    POUR i DE start À start + length - 1 FAIRE
        result := result + word[i]
    FIN POUR

    RETOURNER result
END

```
