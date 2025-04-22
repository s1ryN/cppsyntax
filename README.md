Základní syntaxe C++

Toto repo obsahuje přehled základní syntaxe jazyka C++ včetně ukázek kódu a vysvětlení klíčových konceptů.

Obsah

Úvod

Hello World

Proměnné a datové typy

Operátory

Řídicí struktury

Funkce

Třídy a objekty

Ukazatele a reference

Hlavičkové soubory a preprocesor

Kompilace a spuštění

Licence

Úvod

C++ je výkonný programovací jazyk s podporou objektově orientovaného, procedurálního i generického programování. Tento přehled pokrývá základní konstrukce, které vám pomohou začít.

Hello World

#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}

#include <iostream>: Zahrnuje knihovnu pro vstup a výstup.

int main(): Vstupní bod programu.

std::cout: Výstup na konzoli.

return 0;: Ukončení programu.

Proměnné a datové typy

int a = 5;             // Celé číslo
float b = 3.14f;       // Desetinné číslo (jednoduchá přesnost)
double c = 2.71828;    // Desetinné číslo (dvojnásobná přesnost)
char d = 'A';          // Jeden znak
bool e = true;         // Pravdivostní hodnota

C++ podporuje základní datové typy: int, float, double, char, bool.

Proměnné lze deklarovat s inicializací nebo bez ní.

Operátory

Typ

Příklad

Popis

Aritmetické

+, -, *, /, %

Základní matematické operace

Přiřazovací

=, +=, -=

Přiřazení a kombinované operace

Relační

==, !=, <, >

Porovnání hodnot

Logické

&&, `



, !`

Logické spojky

Řídicí struktury

Podmínky

if (a > b) {
    // kód
} else if (a == b) {
    // kód
} else {
    // kód
}

Smyčky

// for
for (int i = 0; i < 10; ++i) {
    // kód
}

// while
while (condition) {
    // kód
}

// do-while
do {
    // kód
} while (condition);

Funkce

double sum(double x, double y) {
    return x + y;
}

int main() {
    double result = sum(3.5, 2.5);
    std::cout << "Součet: " << result << std::endl;
    return 0;
}

Deklarace: návratový typ, název a parametry.

Funkce může vracet libovolný datový typ nebo void.

Třídy a objekty

class Person {
public:
    std::string name;
    int age;

    void greet() const {
        std::cout << "Ahoj, jmenuji se " << name << "." << std::endl;
    }
};

int main() {
    Person p;
    p.name = "Jan";
    p.age = 30;
    p.greet();
    return 0;
}

class: Definuje nový typ s poli a metodami.

public: Přístupové modifikátory (public, protected, private).

Ukazatele a reference

int x = 10;
int* ptr = &x;      // ukazatel na x
int& ref = x;       // reference na x

std::cout << *ptr << std::endl; // dereference
ref = 20;          // změní x na 20

Ukazatel (*): ukládá adresu proměnné.

Reference (&): alias pro existující proměnnou.

Hlavičkové soubory a preprocesor

#include: Zahrnuje obsah souborů.

Strážci hlaviček:

#ifndef HEADER_H
#define HEADER_H
// obsah
#endif

Kompilace a spuštění

Kompilace pomocí g++:

g++ -std=c++17 main.cpp -o my_program
./my_program

-std=c++17: Použití standardu C++17.

-o: Název výstupního souboru.
