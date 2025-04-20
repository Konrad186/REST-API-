# REST API z regułą decyzyjną
Projekt REST API wykonany w Flask

W repozytorium znajdują się pliki:
- app.py – główny plik z aplikacją
- requirements.txt – biblioteki wymagane do uruchomienia
- Dockerfile – plik do uruchomienia aplikacji w kontenerze Docker
- Lab2.ipynb – notatnik Jupyter z testami działania API
- README.md – instrukcja obsługi projektu

Aby uruchomić projekt lokalnie, należy:
1. Zainstalować wymagane biblioteki poleceniem: pip install -r requirements.txt
2. Uruchomić aplikację: python app.py
3. Otworzyć przeglądarkę i wejść na adres: http://localhost:5000/

Aby uruchomić projekt w Dockerze:
1. W katalogu z plikami uruchomić: docker build -t flask-api .
2. Następnie: docker run -p 5000:5000 flask-api
3. Aplikacja będzie dostępna pod adresem: http://localhost:5000/

Plik Lab2.ipynb zawiera testy wszystkich endpointów API przy użyciu biblioteki requests oraz uruchamianie serwera Flask z poziomu Jupyter Notebook.

Dostępne endpointy:
- / → zwraca "Witaj w moim API!"
- /mojastrona → zwraca "To jest moja strona!"
- /hello?name=Konrad → zwraca "Hello Konrad!" lub "Hello!" bez parametru
- /api/v1.0/predict?num1=3&num2=4 → zwraca JSON z predykcją, np. {"prediction": 1, "features": {"num1": 3.0, "num2": 4.0}}
