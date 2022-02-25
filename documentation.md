<h1 align="center">Convert-SK - Documentation</h1>
<p align="center">Convert-Sk est un skript permettant de faire une conversion d'une valeur.</p><br />

## 🏹 Plus d'informations ?
Vous souhaitez avoir des informations sur comment télécharger et installer ce code ?
Rendez vous sur cette page : [README.md](https://github.com/MaxouLeKangou/Convert-SK/blob/main/README.md)

## 👨‍💻 convert
- **_Cette partie si dessous, va vous permettre de convertir une valeur._**
```
function convert(n: integer) :: text:
    set {_t} to "%{_n}%"
    set {_1} and {_2} to 0

    set {_l} to "K"
    {_n} is between 100 and 999:
        set {_2} to the first 1 characters of {_t}

    {_n} is between 1000 and 999999:
        set {_2} to the last 3 characters of {_t}

        {_n} is between 1000 and 9999:
            set {_1} to the first 1 characters of {_t}
            set {_2} to the first 1 characters of {_2}
        {_n} is between 10000 and 99999:
            set {_1} to the first 2 characters of {_t}
            set {_2} to the first 1 characters of {_2}
        {_n} is between 100000 and 999999:
            set {_1} to the first 3 characters of {_t}
            set {_2} to the first 1 characters of {_2}

    {_n} is between 1000000 and 999999999:
        set {_2} to the last 6 characters of {_t}
        set {_l} to "M"

        {_n} is between 1000000 and 9999999:
            set {_1} to the first 1 characters of {_t}
            set {_2} to the first 1 characters of {_2}
        {_n} is between 10000000 and 99999999:
            set {_1} to the first 2 characters of {_t}
            set {_2} to the first 1 characters of {_2}
        {_n} is between 100000000 and 999999999:
            set {_1} to the first 3 characters of {_t}
            set {_2} to the first 1 characters of {_2}

    return "%{_1}%.%{_2}%%{_l}%"
```
- **_Pour convertir une valeur dans votre code, utiliser cette ligne._** ⚠️**REMPLACER "valeur" PAR UNE VALEUR ENTIÈRE**
```
set {_convert} to convert(valeur)
```
