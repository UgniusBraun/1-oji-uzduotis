# Pažymių vidurkio skaičiuoklė

Programa atsitiktinai generuoja pažymius dideliam kiekiui studentų, suskaičiuoja jų galutinį pažymį, ir pagal jį skirsto studentus į geriau besimokančius "kietekus" bei prasčiau besimokančius "nenaudėlius".

## Veikimo principas

Paleidus programą ji atlieka šiuos veiksmus:

- Sukuria studentų failą, kiekvienam studentui atsitiktinai sugeneravusi tam tikrą skaičių namų darbų pažymių, bei egzamino pažymį.
- Apskaičiuoja kiekvieno studento galutinį pažymį.
- Pagal tai, ar galutinis pažymys yra didesnis už praeinamą penketą, ar ne, skirsto studentus į dvi grupes.
- Sukuria du failus, į kuriuos išvedami atitinkamai į grupes suskirstyti studentai.
- Skaičiuoja kiek laiko buvo vykdomas kiekvienas iš šių žingsnių, ir šį vykdymo laiką išveda į terminalo langą.

Po sėkmingo programos įvykdymo į terminalo langą išvedami rezultatai panašia forma:

```shell
Vardas      Pavarde         Galutinis Vid. Galutinis Med.
----------------------------------------------------------
Vardenis    Pavardenis      5.25
```

Galutinis vidurkis yra apskaičiuojamas pagal formulę `galutinis = 0.4 * vidurkis + 0.6 * egzaminas`.


## Naudojamos sistemos parametrai:
- CPU: Intel(R) Core(TM) i5-9300H CPU @ 2.40GHz, 2400 MHz, 4 Core(s), 8 Logical Processor(s)
- RAM: 8GB 3200MHz
- SSD: 475GB 


Programos veikimo greičio analizė:

### Failo nuskaitymo laikas su vector konteineriu:
| Studentų sk.       | 1000    | 10,000  | 100,000   | 1,000,000  | 10,000,000 |
| :----------    | :------ | :------ | :-------- | :--------- | :--------- |
| Laikas (s)  | 0.0079 | 0.0688 | 0.7845   | 6.1816    | 65.6402    |

### Failo grupavimo laikas su vector konteineriu:
| Studentų sk.       | 1000    | 10,000  | 100,000   | 1,000,000  | 10,000,000 |
| :----------    | :------ | :------ | :-------- | :--------- | :--------- |
| Laikas (s)  | 0.0009 | 0.0059 | 0.0478   | 0.5305   | 1.4129    |

### Failo nuskaitymo laikas su list konteineriu:
| Studentų sk.       | 1000    | 10,000  | 100,000   | 1,000,000  | 10,000,000 |
| :----------    | :------ | :------ | :-------- | :--------- | :--------- |
| Laikas (s)  | 0.0089 | 0.0788 | 0.6473   | 6.4587   | 64.1781    |

### Failo grupavimo laikas su list konteineriu:
| Studentų sk.       | 1000    | 10,000  | 100,000   | 1,000,000  | 10,000,000 |
| :----------    | :------ | :------ | :-------- | :--------- | :--------- |
| Laikas (s)  | 0 | 0.0050 | 0.0439   | 0.4374   | 4.4586    |


## Programos diegimas ir paleidimas

- Atsisiųskite programos versiją iš github'o,
- Programą sukompiliuokite.


### Changelog

- [v.01](https://github.com/UgniusBraun/1-oji-uzduotis/releases/tag/V0.1) - Pirmoji programos versija.
- [v.02](https://github.com/UgniusBraun/1-oji-uzduotis/releases/tag/V0.2) - Antroji programos versija. Pridėta galimybė duomenis nuskaityti iš failų.
- [v.03](https://github.com/UgniusBraun/1-oji-uzduotis/releases/tag/V.03) - Trečioji programos versija. Kodas išskirstytas į (.cpp) bei (.h) header failus. Taip pat implementuotas išimčių valdymas.
- [v.04](https://github.com/UgniusBraun/1-oji-uzduotis/releases/tag/V.04) - Ketvirtoji programos versija. Pridėta galimybė generuoti failą, su daug studentų, bei atliekama programos veikimo greičio analizė.
- [v.05](https://github.com/UgniusBraun/1-oji-uzduotis/releases/tag/V.05) - Penktoji programos versija. Pakeistas naudojamas konteineris iš vector į list. Taip pat patobulintos programos veikimo sparta palyginta su praeitos realizacijos veikimo sparta.
