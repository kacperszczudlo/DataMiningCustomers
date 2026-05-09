# Data Mining: Segmentacja i Klasyfikacja Klientów

Projekt eksploracji danych realizujący zaawansowaną analizę profili klientów poczty z wykorzystaniem technik uczenia maszynowego.

## Opis

Aplikacja przeprowadza kompleksową analizę danych klientów poczty, wykorzystując algorytmy grupowania i klasyfikacji. System automatycznie:
- Profiluje klientów na podstawie ich zachowań zakupowych
- Segmentuje klientów w grupy o podobnych cechach (clustering K-means)
- Buduje model predykcyjny do klasyfikacji nowych klientów (drzewo decyzyjne)
- Wizualizuje wyniki analizy

## Funkcjonalności

- **Segmentacja Klientów**: Automatyczne grupowanie klientów w 4 segmenty na podstawie:
  - Wieku i płci
  - Łącznej wartości transakcji
  - Liczby przesyłek
  - Średniej wartości przesyłki
  - Procentu przesyłek priorytetowych

- **Model Predykcyjny**: Drzewo decyzyjne pozwalające przewidzieć segment dla nowego klienta

- **Wizualizacje**: Wykresy segmentacji i macierz pomyłek

## Technologie

- **Python 3.x**
- **Pandas** - przetwarzanie danych
- **Scikit-learn** - algorytmy ML (K-means, Decision Tree)
- **Seaborn / Matplotlib** - wizualizacje
- **PostgreSQL** (psycopg2) - źródło danych
- **NumPy, SciPy** - operacje numeryczne

## Instalacja

1. Sklonuj repozytorium:
```bash
git clone https://github.com/kacperszczudlo/Data-Mining-Customers.git
cd Data-Mining-Customers
```

2. Zainstaluj wymagane biblioteki:
```bash
pip install -r requirements.txt
```

3. Skonfiguruj połączenie z bazą danych w pliku `.env`:
```
DB_HOST=your_host
DB_NAME=your_database
DB_USER=your_username
DB_PASSWORD=your_password
DB_PORT=5432
```

## Uruchomienie

```bash
python analiza_klientow.py
```

## Struktura Projektu

```
Data-Mining-Customers/
├── analiza_klientow.py          # Główny skrypt analizy
├── data/
│   ├── datasources.py           # Połączenie z bazą danych
│   ├── normalization.py         # Normalizacja danych
│   └── mining/
│       ├── descriptive.py       # Analiza skupień (K-means)
│       └── predictive.py        # Modele predykcyjne (Decision Tree)
├── requirements.txt             # Zależności projektu
└── README.md
```

## Wyniki Analizy

Program generuje:
1. **Charakterystykę segmentów** - średnie wartości dla każdej grupy klientów
2. **Wykres segmentacji** - wizualizacja podziału klientów
3. **Raport klasyfikacji** - metryki dokładności modelu
4. **Macierz pomyłek** - analiza błędów klasyfikacji

## Autor

**Kacper Szczudło**

## Licencja

Projekt edukacyjny - eksploracja danych i uczenie maszynowe.

---

**Wersja**: 3.0.1
