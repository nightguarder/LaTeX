# Prednáška 5 - Pravidla

## Základní pravidla dělení slov
- Dělení na hranici slabik, ideálně mezi částmi složených slov.
  - Příklad: `země-koule`, `kolem-jdoucí`.
- Slova s předponami se dělí za předponou.
  - Příklad: `na-zdar`, `ne-bez-pečí`.
- Neponechávat jednopísmenné znaky na konci řádku.
- Na konci řádku min. 2 písmena, na začátku min. 3.

## Automatické dělení v TeXu
- TeX dělí automaticky podle tabulek vzorů (`babel`, `polyglossia`).
- Parametry ovlivňující dělení:
  - `\hyphenpenalty`: hodnota 10000 zakáže dělení.

## Ruční úprava dělení
1. **V záhlaví dokumentu**:
   ```latex
   \hyphenation{Net-Ware pa-ra-šu-tis-ta}
   ```
2. **Lokální dělení v textu:**
    ```latex
    rov\-ně a do\-le\-va
    ```
3. **Pokročilé úpravy pomocí \discretionary:**
    ```latex
    Bett\discretionary{-}{t}{}uch
    ```
## Bloky a jejich vlastnosti

- TeX skládá text z bloků a tzv. lepidla (mezery).
- Bloky mají tři rozměry: `width`, `height`, `depth`.
### Skládání bloků

**Vodorovné skládání:**
- příklad vodorovného bloku – slovo „ahoj“
    - `width` = součet width
    - `height` = max height
    - `depth` = max depth
    - `ref` = ref1 (referenční bod čára)

- `\hbox{text}`: text na šířku řádku.
- `\mbox{text}`: na přirozenou šířku textu
- `\framebox[text]`: text navíc s rámečkem kolem.
    - \framebox[5cm]{tři čtyři}

**Svislé skládání:**
LaTeX nabízí dvě varianty:
1. ```latex
    \begin{minipage}[zarovnání]{šířka}
    text
    \end{minipage}
    ```
2. ```latex
    \parbox[zarovnání]{šířka}{text}
    \parbox[b]{3.2em}{pár slov do boxu}
    ```
## Lepidlo
- ke spojování bloků, reprezentuje prázdné místo (mezery)
- **tři složky**
    - optimální velikost (např. 6pt)
    - roztažitelnost (2pt)
    - stlačitelnost (1pt)
```latex
    \hskip 6pt plus 2pt minus 1pt
    \vskip 6pt plus 2pt minus 1pt
```

## Lámání řádků
- TeX vezme celý odstavec a vyznačí si všechna místa,
na kterých lze zlomit řádek
- **pokuty za:**
- nízkou kvalitu řádků (např. příliš řídký)
- nesourodé sousední řádky
- více rozdělených slov pod sebou
- rozdělený poslední řádek
- dělení slov a další ...

- **priklady**
- []()
```latex
\\[velikost]
\newline
% zahájí nový řádek (nezarovná pravý okraj),
```

```latex
\pagebreak[číslo]
\nopagebreak[číslo]
analogie \linebreak
```

```latex
\newpage
\clearpage
\cleardoublepage
ukončí odstavec a stránku, \clear
```