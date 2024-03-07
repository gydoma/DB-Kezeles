# Adatbázis kezelés

## Relációs (adat)model

<u>Mező:</u> Egy cellája a táblának
<u>Rekord:</u> Egy sora a táblának
<u>Reláció:</u> Azonos típusú rekord, névvel ellátott halmaz
<u>Adatbázis:</u> Összetartozó relációk
<u>Egyedtípus:</u> Bármi amiről adatot rögzítünk
<u>Egyedhalmaz:</u> A reláció rekordjainak egy összessége
<u>Egyedérték:</u> Egy adott rekord
<u>Kulcs:</u> Olyan attribútum, amely egyértelműen meghatároz egy rekord
    - <u>Egyszerű kulcs:</u> attribútum, amely önmagában meghatároz egy rekordot
    - <u>Összetett kulcs:</u> attribútum összessége, amik csak egy rekordot határoz meg
    - <u>Elsődleges kulcs:</u> meghatározott kulcs egy reláción
    - <u>Külső kulcs: </u> elsődleges kulcs egy másik reláción
<u>Adatmodell:</u> Szerkezeti leírás, ábrázolás _pl.: ER-modell, relációs modell, relációs séma_

---

### ER-modell példák
---
```Mermaid
flowchart TB
    subgraph 1
        H(Egyedtípus)
        I((Attribútum fa:fa-pen))
        J{Kapcsolat}
    end
    subgraph 2
        A((Attribútum fa:fa-pen))
        B((Attribútum fa:fa-pen))
        C((Attribútum fa:fa-pen))
        D(Egyedtípus)
        D --- A & B & C
    end

    subgraph 3
        E(Egyedtípus)
        F{Kapcsolat}
        G(Egyedtípus)
        E---F---G
    end
```
---
### ER-Modell
```Mermaid
flowchart RL
    subgraph ER-Modell Példa
    D((Dátum))
    B(Autó)
    A{Birtokba Vétel}

    C(Tulajdonos)
    E((Rendszám fa:fa-key))
    F((Típus))
    G((Márka))
    H((Szín))

    I((Név))
    J((Cím))
    K((Telefon))
    L((Ügyfélazonosító fa:fa-key))

    D --- A
    A --- B
    A --- C

    B --- E
    B --- F
    B --- G
    B --- H

    C --- I
    C --- J
    C --- K
    C --- L

    end
```

## Relációs Modell

```
╔══════════════╗
║       E      ║
╠════╦════╦════╣
║ A1 ║ A2 ║ A3 ║
╠════╩════╩════╣
║    Rekord1   ║
╠══════════════╣
║    Rekord2   ║
╠══════════════╣
║    Rekord3   ║
╚══════════════╝
```

## Relációs Séma

E(<u>A1</u>,A2,A3);E2(<u>A1</u>,A2,A3);K(<u>K1,K2</u>)

---

## Kapcsolatok

### 1:1 Kapcsolat (egy-egy)
### 1:N Kapcsolat (egy-több)
### N:M Kapcsolat (több-több)

