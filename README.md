# Proiect PIU

## Titlul proiectului

Aplicație de testare a cunoștințelor în programare

## Descrierea proiectului

Proiectul constă în realizarea unei aplicații interactive care permite evaluarea cunoștințelor utilizatorilor din domeniul programării, sub forma unui test tip quiz. Utilizatorul poate selecta domeniul sau limbajul de programare pentru test: C/C++, Java, Python sau concepte generale de programare.

Aplicația afișează întrebări cu variante de răspuns,în care utilizatorul trebuie să interpreteze codul. Interfața este intuitivă și ușor de utilizat: meniul principal permite selectarea domeniului și vizualizarea rezultatelor.

Implementările actuale includ:

* **Binding și validare**: formularul pentru utilizatori folosește MVVM minimal, proprietățile sunt validate automat (Nume, Prenume, Vârsta) și conectate prin binding la interfață.
* **MVVM simplificat**: clasele `UtilizatorFormViewModel` și `IntrebareViewModel` gestionează datele și logica de prezentare.
* **CRUD complet**: pentru entitățile `Utilizator` și `Intrebare` cu salvare în fișiere text.
* **Tema dark și stil modern**: culori întunecate, panouri rotunjite și butoane colorate.

## Diagrama claselor

```text
+-----------------------+
|       Intrebare       |
+-----------------------+
| IdIntrebare           |
| Domeniu               |
| TextIntrebare         |
| Variante[]             |
| RaspunsCorect         |
| Dificultate           |
| TipCunostinte         |
+-----------------------+
          ^
          |
+-----------------------+
|   IntrebareViewModel  |
+-----------------------+
| Proprietati pentru UI  |
| Logica prezentare     |
+-----------------------+

+-----------------------+
|      Utilizator       |
+-----------------------+
| IdUtilizator          |
| Nume                  |
| Prenume               |
| Varsta                |
+-----------------------+
          ^
          |
+-----------------------+
| UtilizatorFormViewModel|
+-----------------------+
| Nume                  |
| Prenume               |
| VarstaText            |
| Validare proprietati  |
+-----------------------+

+----------------------------+
| AdministrareIntrebariFisier|
+----------------------------+
| Add, Get, Update, Delete   |
+----------------------------+

+-----------------------------+
| AdministrareUtilizatoriFisier|
+-----------------------------+
| Add, Get, Update, Delete      |
+-----------------------------+
```

