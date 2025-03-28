# Počítačová Typografie - LaTeX
>Předmět seznamuje studenty s počítačovou typografií a se základními typografickými pravidly. Pozornost je věnována zejména praktické sazbě dokumentů v systému LaTeX
- [Počítačová Typografie - LaTeX](#počítačová-typografie---latex)
  - [Struktura složek](#struktura-složek)
  - [Zápočet](#zápočet)
  - [Přednášky](#přednášky)
  - [Cvičení](#cvičení)
  - [Notes](#notes)
    - [Prednaska 4](#prednaska-4)
    - [Typografické minimum](#typografické-minimum)
  - [Setup](#setup)
    - [Requirements:](#requirements)

## Struktura složek

__Přednášky__: [PDF/Prednasky](/PDF/Prednasky/)

__Cvičení__: [PDF/Cviceni](/PDF/Cviceni/)

__Materiály__: [PDF/Learning](/PDF/Learning/)

## Zápočet

K udělení zápočtu je nutné odevzdat:
- Text v LaTeXu (min. 5 stran).
- Text musí splňovat typografické konvence a obsahovat: obsah, seznam literatury, obrázek nebo tabulku.
- Odevzdat PDF a zdrojové soubory do konce března 2024.

__Solution:__
- Seminární práce přepsat z Docs do Texu
## Přednášky

- Úvod, klasifikace písem
- 2. Vlastnosti písem, volba písma [Konflikt písmen](/PDF/Prednasky/prednaska2%20-%20volba%20pisma.pdf)
- 3. Principy sazby, interpunkce, pomlčky, data ... [Principy sazby](/PDF/Prednasky/prednaska3%20-%20princpi%20sazby.pdf)

## Cvičení

- Úvod do LaTeXu
- Speciální znaky a práce s písmem
- Obrázky a tabulky...

## Notes

### Prednaska 4 
- [Poznamky z prednasky](/Notes/Prednáška4.md)
### Prednaska 5
- [Poznamky z Prednasky]()
### Typografické minimum 
- [Dokument s poznámky](/PDF/Learning/Typografické_minimum_2024.pdf)
- Před odevzdáním práce si zkontrolovat chyby a dodržovat pravidla z tohoto dokumentu. Vyvaruješ se tak opak. vrácení práce.
- Pro kontrolu použít [typopo.org](https://app.typopo.org)
  - stará se o psaní *správných* uvozovek, mezer, zkratek atd.
  
  ```json
  "Den Mikuláše biskupa a vyznavače. Ješek sládek z Krumlova." 
  --> oprava
  „Den Mikuláše biskupa a vyznavače. Ješek sládek z Krumlova."
  ```

## Setup
- Configure LateX in VSCode or use online editor [Overleaf](https://www.overleaf.com/project)
### Requirements:
1. Install **TeX Live** via Homebrew:
   ```bash
   brew install texlive
2. Install **LaTeX Workshop** extension:
    - Name: LaTeX Workshop
    - [VS Marketplace Link:](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
3. Add **Tex Live** binaries to PATH 
   - export PATH="/usr/local/texlive/2024/bin/universal-darwin:$PATH" 
4. Configure **XeLaTeX** as a preferable compiler
- Put Xelatex **1. first** in settings.json:
```json
{
		"name": "xelatex",
		"command": "xelatex",
		"args": [
			"-synctex=1",
			"-interaction=nonstopmode",
			"-file-line-error",
			"%DOC%"
		],
		"env": {}
	},
  ```
  5. Restart VSCode