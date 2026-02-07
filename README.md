# Zadanie 1 - Maksimum w tablicy

## Cel
Celem zadania jest znalezienie maksymalnego elementu
w tablicy za pomocą liniowego przeszukiwania

## Opis algorytmu
Algorytm polega na jednokrotnym przejściu przez tablicę.
Pierwszy element tablicy przyjmowany jest jako aktualne
maksimum. Następnie każdy kolejny element porównywany jest z 
aktualnym maksimum.Jeżeli element jest większy, aktualizujemy
wartość maksimum. Po przejściu całej tablicy zwracana jest
największa wartość.

##algorytm
1. Wczytaj liczbę n określającą rozmiar tablicy.
2. Wczytaj n elementów tablicy.
3. Ustaw pierwszy element tablicy jako aktualne maksimum.
4. Przejdz przez pozostałe elementy tablicy:
   - jeżeli element jest większy od maksimum, zaaktualizuj 
   maksimum.
5. Wyświetl maksymalny element tablicy.

## Pseudokod
Wczytaj n 
Dla i od 0 do n-1
	Wczytaj tab[i]

max = tab[0]

Dla j od 1 do n-1
	Jeżeli tab[i] > max
		max = tab[j]
Wypisz max

## Złożoność obliczeniowa 
- Złożoność czasowa: 0(n)
- Złożoność pamięciowa: 0(1)

# Przykład
Dla danych:
[4, 6, 3, 2, 1]
Algorytm zwróci wartość 6.

##Wady rozwiązania
Algorytm wymaga sprawdzenia każdego elementu tablicy, co
oznacza jednokrotne przejście przez całą tablicę. Nie 
istnieje szybsze rozwiązanie dla tego problemu w liniowym
przeszukiwaniu. 

## Zadanie 2 - NWD (Algorytm Euklidesa)

## Pseudokod
FUNKCJA NWD(a,b)
DOPÓKI B =! 0
r=a mod b
a=b
b=r
KONIEC DOPÓKI
ZWRÓĆ a

## Zadanie 3 - Sortowanie bąbelkowe

## DIAGRAM BLOKOWY (opis tekstowy):
Start
→ Inicjuj i = 0, n = długość tablicy
→ Pętla zewnętrzna: i < n - 1
→ Pętla wewnętrzna: j = 0 do n - i - 2
→ Jeśli tab[j] > tab[j + 1], zamień miejscami
→ Zwiększ j
→ Koniec pętli wewnętrznej
→ Zwiększ i
→ Koniec

## Implementacja (C)
#include <stdio.h>

int main() {

    int n;

    scanf("%d", &n);

    int tab[n];

    for(int i = 0; i < n; i++) {

        scanf("%d", &tab[i]);

    }

    for(int i = 0; i < n - 1; i++) {

        for(int j = 0; j < n - i - 1; j++) {

            if(tab[j] > tab[j + 1]) {

                int tmp = tab[j];

                tab[j] = tab[j + 1];

                tab[j + 1] = tmp;

            }

        }

    }

    for(int i = 0; i < n; i++) {

        printf("%d ", tab[i]);

    }

    return 0;

}
 
##Test 

Przykład:
Dane wejściowe: 64, 34, 25, 12, 22, 11, 90
Wynik: 11, 12, 22, 25, 34, 64, 98