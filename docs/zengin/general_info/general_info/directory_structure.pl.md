---
title: Struktura katalogów
---
# Struktura katalogów silnika ZenGin

Modowanie polega przede wszystkim na wprowadzaniu zmian w plikach gry. Aby to osiągnąć, musimy poznać strukturę katalogów (folderów) Gothica.

```
├── Data
│   ├── $Templates$
│   ├── modvdf
│   └── Plugins
├── Miles
├── Saves
├── System
│   └── Autorun
└── _work
    └── DATA
        ├── Anims
        │   └── _Compiled
        ├── Meshes
        │   └── _Compiled
        ├── Music
        ├── Presets
        ├── Scripts
        │   ├── _compiled
        │   └── content
        │       └── CUTSCENE
        ├── Sound
        ├── Textures
        ├── Video
        └── Worlds
```

## `Data`

Katalog Data zawiera pliki [`.vdf` woluminów](vdfs.md) gry. Konkretnie chodzi o `anims.vdf` - animacje, `speech.vdf` - dubbing, `worlds.vdf` - plik ZEN świata gry.

## `Saves`

Zawiera zapisy z gry.

## `System`

Katalog System zawiera pliki exe Gothic Startera (programu do uruchamiania modów) czyli `GothicStarter.exe` oraz `GothicStarter_mod.exe`, pliki konfiguracyjne o rozszerzeniu `.ini`, oraz opisy dla modów i ikonki ich skrótów z rozszerzeniem `.rtf`.

**`system/Autorun`** to katalog utworzony na potrzeby Uniona. Służy jako domyślny katalog w którym Union szuka injection skryptów Daedalusa razem z zParserExtenderem oraz pluginami.

## `_work/DATA`

To tutaj dzieje się cała magia:

- `Anims` - zawiera animacje razem z animowanymi modelami.
    - `_compiled` - zawiera skompilowane animacje.
- `Meshes` - zawiera źrodła meshów oraz skompilowane pliki.
    - `_compiled` - zawiera skompilowane meshe.
- `Music` - zawiera pliki z muzyką.
- `Presets` - zawieta podstawowe presety.
- `Scripts`
    - `_compiled` - zawiera skompilowane skrypty - pliki z rozszerzeniem `.dat`.
      - `Content` - zawiera skrypty tworzące całą zawartość gry.
      - `System` - zawiera skrypty tworzące menu.
- `Sound` - zawiera efekty dźwiękowe w formacie `.wav` oraz `.ogg` (tylko dla Uniona).
- `Video` - zawiera filmy w formacie `.bik`.

