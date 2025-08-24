# 🎤 Paroles.net Wrapper 🎶

[![PyPI version](https://img.shields.io/pypi/v/paroles-net-wrapper.svg)](https://pypi.org/project/paroles-net-wrapper/)
[![Build Status](https://img.shields.io/travis/com/Starland9/paroles-net-wrapper.svg)](https://travis-ci.com/Starland9/paroles-net-wrapper)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Hey there, music lover! 🎧 Ever wanted to grab song lyrics from the massive collection at [paroles.net](https://www.paroles.net/)? Well, you're in for a treat! This fun little Python wrapper is here to make your life easier.

It's like having a backstage pass to a huge library of songs. Search for your favorite artists, get the latest hits, and even download the lyrics right to your computer! 🚀

## ✨ Features

*   **🎵 Search for any artist:** Find all the songs from your favorite artists.
*   **📈 Get Top Hits:** Instantly access the current top songs.
*   **🆕 Discover New Music:** Get the list of the newest songs added.
*   **📜 Fetch Lyrics:** Grab the full lyrics for any song.
*   **💾 Save Lyrics:** Save lyrics to a text file on your computer.
*   **🤖 Easy-to-use:** A simple and intuitive object-oriented design.

## 🛠️ Installation

Getting started is as easy as one, two, three! Just open your terminal and type:

```bash
pip install paroles-net-wrapper
```

And voilà! You're ready to rock! 🎸

## 🚀 How to Use

Let's get this party started! Here’s how you can use the wrapper to find some cool tunes.

First, you'll need to import the `ParolesNet` class:

```python
from paroles_net import ParolesNet

# Create an instance of the wrapper
paroles_net = ParolesNet()
```

### 🕵️‍♀️ Searching for an Artist

Let's search for the amazing **Imagine Dragons**:

```python
# Let's find some songs by Imagine Dragons
print("Searching for Imagine Dragons songs... 🐉")
imagine_dragons_songs = paroles_net.search_song("Imagine Dragons")

# Let's see what we found!
for song in imagine_dragons_songs:
    print(f"✅ Found: {song.name} by {song.artist}")

# Let's pick the first song from the list
if imagine_dragons_songs:
    first_song = imagine_dragons_songs[0]
    print(f"\nLet's get the lyrics for '{first_song.name}'... 📜")

    # Get the lyrics!
    lyrics = first_song.get_lyrics()
    print(lyrics)

    # You can also save them directly to a file!
    # This will create a file like: paroles_net/Imagine Dragons/Believer.txt
    print("\nSaving lyrics to a file... 💾")
    first_song.save_lyrics()
    print("Done!")
```

### 📈 Getting the Best Songs

Want to know what's hot right now? Easy peasy!

```python
# Get the list of the best songs
print("Fetching the best songs... 🔥")
best_songs = paroles_net.get_best_songs()

for song in best_songs:
    print(f"🏆 {song.name} - {song.artist}")
```

### 🆕 Getting New Songs

Discover the latest tracks added to the site.

```python
# Get the list of new songs
print("Fetching new songs... 🎶")
new_songs = paroles_net.get_new_songs()

for song in new_songs:
    print(f"✨ {song.name} - {song.artist}")
```

## 📦 The `Song` Object

When you get a list of songs, each one is a `Song` object with these handy attributes and methods:

*   `.name` (str): The name of the song.
*   `.artist` (str): The artist of the song.
*   `.link` (str): The URL to the lyrics page.
*   `.get_lyrics()` (method): Fetches the song's lyrics.
*   `.save_lyrics()` (method): Saves the song's lyrics to a file.

## 🙌 Contributing

Got an idea to make this wrapper even more awesome? Contributions are welcome! Feel free to fork the repository, make your changes, and submit a pull request. Let's make this the best lyrics scraper out there!

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Happy coding and enjoy the music! 🎉
