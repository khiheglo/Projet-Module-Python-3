# Projet-Module-Python-3
Projet final du module Python  3

## Projet Final

```python
import sys

def menu():
    print("")
    print("Choisissez parmi les 6 options suivantes :")
    print("2: Ajoutez un élément à la liste")
    print("3: Retirez un élément à la liste")
    print("4: Affichez la liste")
    print("5: Videz la liste")
    print("6: Quitter")
    choix = int(input("Votre choix :"))
    while choix < 2 or choix > 5:
        choix = int(input("Votre choix n'est pas valide. Choisissez un nombre compris entre 2 et 5 :"))

    return choix

def ajout(pan):
    element = input("Entrez le nom de l'élément à ajouter à la liste de course : ?")
    pan = pan.append(element)
    print(f"L'élément {element} a bien été ajouté. {chr(14)}")

def supprime (pan):
    element = input("Entrez le nom de l'élément à rétirer de la liste de course : ")
    if element in pan:
        pan = pan.remove(element)
        print(f"L'élément {element} a bien été supprimé de la liste.")
    else:
        print(f"L'élément {element} n'est pas dans la liste.")

def affiche (pan):
    if len(pan)>0:
        print("Voici le contenu de la liste : ")
        for i in pan:
            print(f" {pan.index(i) +1} - {i}")
    else:
        print(f"Votre liste ne contient aucun élément.")

def nettoye (pan):
    pan.clear()
    print("La liste a été vidée de son contenu.")

panier = []
x = menu()
while x != 5:
    if x == 1:
        ajout(panier)

    elif x == 2:
        supprime(panier)

    elif x == 3:
        affiche(panier)

    elif x == 4:
        nettoye(panier)

    x = menu()

sys.exit()

```
