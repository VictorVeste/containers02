# Lucrare de laborator: Containerizare cu Docker - Darea de Seamă

## Scop

Această lucrare de laborator a avut ca obiectiv familiarizarea cu elementele de bază ale containerizării și pregătirea spațiului de lucru pentru următoarele activități practice.

## Sarcina

Am urmat pașii indicati pentru instalarea Docker Desktop și am verificat funcționarea acestuia.

## Pregătire

Am descărcat și instalat Docker Desktop.

## Execuție

1. Am creat repozitoriul `containers02` și l-am clonat pe computerul meu.
2. În directorul `containers02` am creat fișierul `Dockerfile` cu conținutul:

   ```Dockerfile
   FROM debian:latest
   COPY ./site/ /var/www/html/
   CMD ["sh", "-c", "echo hello from $HOSTNAME"]
   ```

3. Am creat directorul `site` în același director de proiect și am adăugat un fișier `index.html` cu conținut arbitrar.
4. Deschizând terminalul în directorul `containers02`, am executat comanda:

   ```bash
   docker build -t containers02 .
   ```

5. Am notat durata necesară pentru crearea imaginii Docker, acest timp find 20.07 secunde.
6. Am pornit containerul cu comanda:

   ```bash
   docker run --name containers02 containers02
   ```

7. Am prezentat mesajul afișat în consolă.
8. Am șters containerul și l-am repornit folosind comenzile:

   ```bash
   docker rm containers02
   docker run -ti --name containers02 containers02 bash
   ```

9. În fereastra terminalului deschis, am navigat în directorul `/var/www/html/` și am afișat conținutul acestuia cu comanda `ls -l`.
10. Am prezentat rezultatul afișat pe ecran.
11. Am închis fereastra terminalului cu comanda `exit`.

## Descrierea Proiectului

- **Lucrare de laborator:** Containerizare cu Docker
- **Scopul lucrării:** Familiarizarea cu elementele de bază ale containerizării și pregătirea spațiului de lucru pentru activități viitoare.
- **Sarcina:** Instalarea Docker Desktop și verificarea funcționării acestuia.
- **Descrierea Execuției Lucrării:**
  - Pasul 4: Am construit imaginea Docker.
  - Pasul 6: Am rulat containerul și am prezentat mesajul din consolă.
  - Pasul 9: Am afișat conținutul directorului `/var/www/html/`.
- **Concluzii:** Am experimentat cu succes procesul de containerizare folosind Docker, facilitând dezvoltarea și distribuirea aplicațiilor.
- **Bibliografie:** [Documentația Docker](https://docs.docker.com/)
- [Curs Containerizarea aplicațiilor](https://moodle.usm.md/course/view.php?id=6807)
