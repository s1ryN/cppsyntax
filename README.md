# Základní syntaxe C++

Tento repozitář obsahuje přehled základní syntaxe jazyka C++ s ukázkami kódu a stručnými vysvětleními. Slouží jako rychlá reference pro začátečníky.

---

## Obsah

- [Úvod](#úvod)
- [Hello World](#hello-world)
- [Proměnné a datové typy](#proměnné-a-datové-typy)
- [Operátory](#operátory)
- [Řídicí struktury](#řídicí-struktury)
- [Funkce](#funkce)
- [Ukládání a načítání ze souboru](#ukládání-a-načítání-ze-souboru)

---

## Úvod

C++ je výkonný, víceparadigmatický programovací jazyk podporující procedurální, objektově orientované i generické programování. Tento dokument pokrývá základní konstrukce, které vám pomohou rychle začít.

---

## Hello World

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, World!" << endl;
    return 0;
}
```

> **Vysvětlení:**
> - `#include <iostream>`: Zahrnuje knihovnu pro vstup a výstup.
> - `using namespace std;`: Umožňuje používat prvky jmenného prostoru std bez předpony.
> - `int main()`: Hlavní funkce, vstupní bod programu.
> - `cout`: Výstupní proud pro konzoli.
> - `endl`: Konec řádku a vyprázdnění proudu.
> - `return 0;`: Signalizuje úspěšné ukončení programu.

---

## Proměnné a datové typy

```cpp
#include <string>
using namespace std;

int    a = 5;            // Celé číslo
float  b = 3.14f;        // Desetinné číslo (jednoduchá přesnost)
double c = 2.71828;      // Desetinné číslo (dvojnásobná přesnost)
char   d = 'A';          // Jeden znak
bool   e = true;         // Pravdivostní hodnota
string s = "Hello";      // Řetězec znaků
```

- **Primární typy:** `int`, `float`, `double`, `char`, `bool`, `string`
- Proměnné lze deklarovat s inicializací nebo bez ní:
  ```cpp
  int x;        // bez inicializace
  int y = 10;   // s inicializací
  ```

---

## Operátory

| Typ           | Operátory                                             | Popis                              |
| ------------- | ----------------------------------------------------- | ---------------------------------- |
| Aritmetické   | `+`, `-`, `*`, `/`, `%`                               | Základní matematické operace       |
| Přiřazovací   | `=`, `+=`, `-=`, `*=`                                 | Přiřazení a rozšířené přiřazení    |
| Relační       | `==`, `!=`, `<`, `>`, `<=`, `>=`                      | Porovnání hodnot                   |
| Logické       | `&&` (and), OR (dvě svislé čáry), `!` (not)           | Logické operace                    |
| Alternativní  | `and`, `or`, `not`                                    | Slovní ekvivalenty logických op.   |

---

## Řídicí struktury

### Podmínky

```cpp
if (a > b) {
    // kód, když a je větší než b
} else if (a == b) {
    // kód, když jsou stejné
} else {
    // kód v ostatních případech
}
```

## Switch

```cpp
#include <iostream>
using namespace std;

int main() {
    int x = 2;
    switch (x) {
        case 1:
            cout << "Jedna" << endl;
            break;
        case 2:
            cout << "Dva" << endl;
            break;
        default:
            cout << "Jiné" << endl;
    }
    return 0;
}
```

> **Poznámka:** `switch` umožňuje větvení na základě hodnoty celočíselných výrazů.

---

### Smyčky

```cpp
// for
for (int i = 0; i < 10; ++i) {
    // opakovaný kód
}

// while
while (condition) {
    // dokud je podmínka pravdivá
}

// do-while
do {
    // vykoná se alespoň jednou
} while (condition);
```

---

## Funkce

```cpp
#include <iostream>
using namespace std;

double sum(double x, double y) {
    return x + y;
}

int main() {
    double result = sum(3.5, 2.5);
    cout << "Součet: " << result << endl;
    return 0;
}
```

- Deklarace funkce: `návratový_typ název(parametry) { ... }`
- Funkce může vracet libovolný datový typ nebo `void`.
- Parametry lze předávat podle hodnoty nebo referenčně.

## Ukládání a načítání ze souboru

```cpp
#include <fstream>
#include <iostream>
using namespace std;

int main() {
    // Uložení do souboru
    ofstream out("data.txt");
    if (out.is_open()) {
        out << "Hello, file!" << endl;
        out.close();
    }

    // Načtení ze souboru
    ifstream in("data.txt");
    string line;
    if (in.is_open()) {
        while (getline(in, line)) {
            cout << line << endl;
        }
        in.close();
    }
    return 0;
}
```

> **Vysvětlení:**
> - `#include <fstream>`: Práce se soubory.
> - `ofstream`: Výstupní stream pro zápis do souborů.
> - `ifstream`: Vstupní stream pro čtení ze souborů.
> - `is_open()`: Kontrola, zda se soubor úspěšně otevřel.

---

