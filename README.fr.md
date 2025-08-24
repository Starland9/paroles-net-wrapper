# 🎤 Paroles.net Wrapper 🎶

[English](README.md) | [Français](README.fr.md)

[![PyPI version](https://img.shields.io/pypi/v/paroles-net-wrapper.svg)](https://pypi.org/project/paroles-net-wrapper/)
[![Build Status](https://img.shields.io/travis/com/Starland9/paroles-net-wrapper.svg)](https://travis-ci.com/Starland9/paroles-net-wrapper)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Salut l'ami musicien ! 🎧 Vous avez toujours rêvé de récupérer les paroles de chansons de l'immense collection de [paroles.net](https://www.paroles.net/) ? Eh bien, vous allez être servi ! Ce petit wrapper Python amusant est là pour vous simplifier la vie.

C'est comme avoir un pass backstage pour une immense bibliothèque de chansons. Recherchez vos artistes préférés, obtenez les derniers hits, et téléchargez même les paroles directement sur votre ordinateur ! 🚀

## ✨ Fonctionnalités

*   **🎵 Recherchez n'importe quel artiste :** Trouvez toutes les chansons de vos artistes favoris.
*   **📈 Obtenez les Top Hits :** Accédez instantanément aux meilleures chansons du moment.
*   **🆕 Découvrez de nouvelles musiques :** Obtenez la liste des dernières chansons ajoutées.
*   **📜 Récupérez les paroles :** Obtenez les paroles complètes de n'importe quelle chanson.
*   **💾 Sauvegardez les paroles :** Enregistrez les paroles dans un fichier texte sur votre ordinateur.
*   **🤖 Facile à utiliser :** Une conception orientée objet simple et intuitive.

## 🛠️ Installation

Pour commencer, rien de plus simple ! Ouvrez simplement votre terminal et tapez :

```bash
pip install paroles-net-wrapper
```

Et voilà ! Vous êtes prêt à rocker ! 🎸

## 🚀 Comment l'utiliser

Que la fête commence ! Voici comment vous pouvez utiliser le wrapper pour trouver des morceaux sympas.

D'abord, vous devrez importer la classe `ParolesNet` :

```python
from paroles_net import ParolesNet

# Créez une instance du wrapper
paroles_net = ParolesNet()
```

### 🕵️‍♀️ Rechercher un artiste

Cherchons l'incroyable groupe **Imagine Dragons** :

```python
# Cherchons quelques chansons d'Imagine Dragons
print("Recherche de chansons d'Imagine Dragons... 🐉")
imagine_dragons_songs = paroles_net.search_song("Imagine Dragons")

# Voyons ce que nous avons trouvé !
for song in imagine_dragons_songs:
    print(f"✅ Trouvé : {song.name} par {song.artist}")

# Choisissons la première chanson de la liste
if imagine_dragons_songs:
    first_song = imagine_dragons_songs[0]
    print(f"\nRécupérons les paroles de '{first_song.name}'... 📜")

    # Obtenez les paroles !
    lyrics = first_song.get_lyrics()
    print(lyrics)

    # Vous pouvez aussi les sauvegarder directement dans un fichier !
    # Cela créera un fichier comme : paroles_net/Imagine Dragons/Believer.txt
    print("\nSauvegarde des paroles dans un fichier... 💾")
    first_song.save_lyrics()
    print("Terminé !")
```

### 📈 Obtenir les meilleures chansons

Vous voulez savoir ce qui est populaire en ce moment ? C'est facile !

```python
# Obtenez la liste des meilleures chansons
print("Récupération des meilleures chansons... 🔥")
best_songs = paroles_net.get_best_songs()

for song in best_songs:
    print(f"🏆 {song.name} - {song.artist}")
```

### 🆕 Obtenir les nouvelles chansons

Découvrez les derniers morceaux ajoutés sur le site.

```python
# Obtenez la liste des nouvelles chansons
print("Récupération des nouvelles chansons... 🎶")
new_songs = paroles_net.get_new_songs()

for song in new_songs:
    print(f"✨ {song.name} - {song.artist}")
```

## 📦 L'objet `Song`

Lorsque vous obtenez une liste de chansons, chacune est un objet `Song` avec ces attributs et méthodes pratiques :

*   `.name` (str) : Le nom de la chanson.
*   `.artist` (str) : L'artiste de la chanson.
*   `.link` (str) : L'URL vers la page des paroles.
*   `.get_lyrics()` (méthode) : Récupère les paroles de la chanson.
*   `.save_lyrics()` (méthode) : Sauvegarde les paroles de la chanson dans un fichier.

## 🙌 Contribuer

Vous avez une idée pour rendre ce wrapper encore plus génial ? Les contributions sont les bienvenues ! N'hésitez pas à forker le dépôt, à faire vos modifications et à soumettre une pull request. Faisons de ce scraper le meilleur qui soit !

## 📜 Licence

Ce projet est sous licence MIT - voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

Bon codage et profitez de la musique ! 🎉
