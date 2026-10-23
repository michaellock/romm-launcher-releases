# Thèmes de couleurs pour RomM Launcher

## Format d'un thème

Un thème est un fichier JSON simple décrivant des couleurs. Aucun CSS ni code arbitraire n'est autorisé.

```json
{
  "name": "Nord",
  "author": "RomM Launcher",
  "base": "dark",
  "colors": {
    "bg-0": "#2e3440",
    "bg-1": "#3b4252",
    "accent": "#88c0d0",
    "radius": "10px"
  }
}
```

### Champs

| Champ    | Requis | Description                                                  |
|----------|--------|--------------------------------------------------------------|
| `name`   | oui    | Nom affiché dans les réglages.                               |
| `author` | non    | Auteur du thème.                                             |
| `base`   | oui    | `dark` ou `light` : thème intégré dont sont issues les couleurs non redéfinies. |
| `colors` | non    | Objet contenant les variables CSS redéfinies (voir ci-dessous). |

### Clés de couleurs permises

Les variables de couleur de l'interface :

- `bg-0`, `bg-1`, `bg-2`, `bg-3` : arrière-plans (du plus foncé au plus clair)
- `border` : bordures des contrôles
- `text` : texte principal
- `text-dim` : texte secondaire
- `accent` : couleur d'accentuation (liens, boutons primaires)
- `accent-soft` : accent en transparence (fonds de sélection)
- `danger` : erreurs, actions destructives
- `warn` : avertissements
- `ok` : succès, validations
- `radius` : arrondi des angles (longueur CSS : `8px`, `0.5rem`…)

### Formats de valeur admis

- **Couleurs** : `#rgb`, `#rrggbb`, `#rrggbbaa`, `rgb()`, `rgba()`, `hsl()`
- **Radius** : une longueur CSS simple (`8px`, `1.2rem`)

Toute autre clé ou format est refusé pour empêcher l'injection CSS.

## Comment importer un thème

1. Ouvrez RomM Launcher
2. Allez dans **Réglages** → **Général** → **Thème**
3. Cliquez sur **« Importer un thème… »**
4. Sélectionnez un fichier `.json` de thème
5. Le thème apparaît dans la grille ; cliquez dessus pour l'activer

Pour supprimer un thème importé, cliquez sur la croix en haut à gauche de sa vignette.

## Astuces de contraste

- Pour un écran OLED, le thème **OLED noir** (`bg-0: #000`) économise la batterie et améliore le contraste.
- Le mode **Automatique (système)** suit la préférence de votre OS (sombre le soir, clair le jour).
- Un thème importé dont `base` est `light` reprend les couleurs du thème Clair pour les variables non définies.
- Testez toujours votre thème sur les deux bases (sombre et claire) si vous le partagez.

## Modèles fournis

- `nord.json` — palette Nord (froid, bleuté)
- `dracula.json` — thème Dracula (violet profond)
- `solarized-light.json` — Solarized Light (doux, jaunâtre)
- `gruvbox-dark.json` — Gruvbox Dark (rétro, orangé)
- `catppuccin-mocha.json` — Catppuccin Mocha (rose pâle, moderne)

---

# Color Themes for RomM Launcher

## Theme Format

A theme is a simple JSON file describing colors. No CSS or arbitrary code is allowed.

```json
{
  "name": "Nord",
  "author": "RomM Launcher",
  "base": "dark",
  "colors": {
    "bg-0": "#2e3440",
    "bg-1": "#3b4252",
    "accent": "#88c0d0",
    "radius": "10px"
  }
}
```

### Fields

| Field    | Required | Description                                                  |
|----------|----------|--------------------------------------------------------------|
| `name`   | yes      | Name displayed in settings.                                  |
| `author` | no       | Theme author.                                                |
| `base`   | yes      | `dark` or `light`: built-in theme used as fallback for undefined colors. |
| `colors` | no       | Object containing redefined CSS variables (see below).       |

### Allowed Color Keys

The interface color variables:

- `bg-0`, `bg-1`, `bg-2`, `bg-3`: backgrounds (darkest to lightest)
- `border`: control borders
- `text`: primary text
- `text-dim`: secondary text
- `accent`: accent color (links, primary buttons)
- `accent-soft`: transparent accent (selection backgrounds)
- `danger`: errors, destructive actions
- `warn`: warnings
- `ok`: success, validations
- `radius`: corner radius (CSS length: `8px`, `0.5rem`…)

### Allowed Value Formats

- **Colors**: `#rgb`, `#rrggbb`, `#rrggbbaa`, `rgb()`, `rgba()`, `hsl()`
- **Radius**: simple CSS length (`8px`, `1.2rem`)

Any other key or format is rejected to prevent CSS injection.

## How to Import a Theme

1. Open RomM Launcher
2. Go to **Settings** → **General** → **Theme**
3. Click **Import a theme…**
4. Select a `.json` theme file
5. The theme appears in the grid; click it to activate

To delete an imported theme, click the × at the top-left of its swatch.

## Contrast Tips

- For OLED screens, the **OLED noir** theme (`bg-0: #000`) saves battery and improves contrast.
- **Automatique (système)** mode follows your OS preference (dark in the evening, light during the day).
- An imported theme with `base: light` uses the Light built-in theme's colors for undefined variables.
- Always test your theme on both bases (dark and light) if you share it.

## Included Templates

- `nord.json` — Nord palette (cool, bluish)
- `dracula.json` — Dracula theme (deep purple)
- `solarized-light.json` — Solarized Light (soft, yellowish)
- `gruvbox-dark.json` — Gruvbox Dark (retro, orange)
- `catppuccin-mocha.json` — Catppuccin Mocha (pale pink, modern)