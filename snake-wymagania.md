# Snake - wymagania

## 1. Cel

Prosta gra Snake dla jednego gracza. Gracz steruje wężem, zbiera jedzenie i unika kolizji.

## 2. Plansza

- R1. Plansza to siatka 20 x 20 pól.
- R2. Każde pole jest puste, zajęte przez węża albo zajęte przez jedzenie.
- R3. Krawędzie planszy są ścianami (brak przechodzenia na drugą stronę).

## 3. Wąż

- R4. Na starcie wąż ma długość 3 segmentów, stoi na środku planszy i porusza się w prawo.
- R5. Wąż porusza się o jedno pole w każdym takcie gry.
- R6. Gracz zmienia kierunek strzałkami (lub klawiszami W/A/S/D).
- R7. Nie można zawrócić o 180 stopni (np. z ruchu w prawo od razu w lewo) - taki klawisz jest ignorowany.
- R8. W jednym takcie liczy się najwyżej jedna zmiana kierunku.

## 4. Jedzenie

- R9. Na planszy zawsze leży dokładnie jedno jedzenie.
- R10. Jedzenie pojawia się na losowym pustym polu (nigdy na wężu).
- R11. Gdy głowa węża wejdzie na pole z jedzeniem:
  - wąż wydłuża się o 1 segment,
  - wynik rośnie o 1 punkt,
  - pojawia się nowe jedzenie.

## 5. Koniec gry

- R12. Gra kończy się, gdy głowa węża:
  - uderzy w ścianę, albo
  - wejdzie na własny segment ciała.
- R13. Gra kończy się wygraną, gdy wąż zajmie całą planszę.
- R14. Po końcu gry wyświetla się komunikat "Koniec gry" z wynikiem i opcją restartu (klawisz Spacja lub Enter).

## 6. Wynik i tempo

- R15. Aktualny wynik jest widoczny przez cały czas gry.
- R16. Najlepszy wynik (rekord) jest zapamiętywany między sesjami.
- R17. Tempo startowe: 1 takt co 150 ms.
- R18. (Opcjonalnie) co 5 zjedzonych punktów tempo rośnie o 10 ms, ale nie szybciej niż 1 takt co 60 ms.

## 7. Sterowanie grą

- R19. Klawisz P lub Esc włącza i wyłącza pauzę.
- R20. W trakcie pauzy wąż stoi, a naciśnięcia strzałek są ignorowane.

## 8. Poza zakresem

- Tryb wieloosobowy.
- Przeszkody na planszy.
- Dźwięk i muzyka.
- Poziomy trudności do wyboru.

## 9. Kryteria akceptacji (przykłady)

- Wąż długości 3 zjada jedzenie -> ma długość 4, wynik = 1.
- Wąż porusza się w prawo, gracz wciska strzałkę w lewo -> wąż dalej jedzie w prawo.
- Głowa węża wchodzi na krawędź planszy -> gra się kończy, widać komunikat "Koniec gry".
- Nowe jedzenie nigdy nie pojawia się na polu zajętym przez węża.
