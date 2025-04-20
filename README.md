# REST API z regułą decyzyjną
Projekt REST API wykonany w Flask w ramach Lab2.

Pliki:
- app.py – główny plik z kodem API
- requirements.txt – biblioteki wymagane do uruchomienia
- Dockerfile – plik do uruchomienia w Dockerze

Uruchomienie lokalne:
1. Zainstaluj zależności: pip install -r requirements.txt
2. Uruchom aplikację: python app.py
3. API będzie dostępne pod adresem: http://127.0.0.1:5000/

Uruchomienie w Dockerze:
1. Zbuduj obraz: docker build -t flask-api .
2. Uruchom kontener: docker run -p 5000:5000 flask-api
3. Wejdź na: http://localhost:5000/

Endpointy:
- / – strona główna
- /mojastrona
- /hello?name=TwojeImie
- /api/v1.0/predict?num1=3&num2=4
