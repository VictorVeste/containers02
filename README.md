# Raport de progres: Containerizare cu Docker - Rezumat

## Obiectiv

Această lucrare de laborator a avut ca scop familiarizarea cu conceptele de bază ale containerizării și pregătirea mediului de lucru pentru activități viitoare legate de Docker.

## Activități

### Pregătire

Am instalat Docker Desktop pe calculatorul meu, urmând pașii de configurare și verificând funcționarea acestuia.

### Implementare

1. Am creat un nou repozitoriu denumit `containers02` și l-am clonat local pentru a începe lucrul.
2. În directorul `containers02`, am definit fișierul `Dockerfile`, specificând un container bazat pe imaginea `debian:latest`, copiind conținutul directorului `site` în locația `/var/www/html/` și configurând comanda de pornire pentru a afișa un mesaj de salut.
3. Am creat directorul `site` și am adăugat un fișier `index.html` cu conținut arbitrar.
4. Am construit imaginea Docker folosind comanda `docker build -t containers02 .`, monitorizând timpul necesar pentru acest proces.
5. Am pornit un container din imaginea creată cu comanda `docker run --name containers02 containers02` și am notat mesajul de salut afișat în terminal.
6. Am șters containerul și l-am repornit în mod interactiv folosind comanda `docker rm containers02` și apoi `docker run -ti --name containers02 containers02 bash`, navigând în directorul `/var/www/html/` și afișând conținutul acestuia.
7. Am încheiat sesiunea interactivă cu `exit`.

## Descrierea Proiectului

- **Scopul Lucrării:** Inițierea în containerizarea cu Docker și stabilirea mediului de lucru.
- **Activități Realizate:**
  - Instalarea și configurarea Docker Desktop.
  - Crearea și configurarea imaginii Docker și a containerelor asociate.
  - Monitorizarea și înțelegerea timpului necesar pentru construirea imaginii.
  - Interacțiunea cu containerele Docker pentru verificarea și explorarea conținutului.
- **Concluzii:** Am obținut o înțelegere inițială a Docker-ului și a procesului de containerizare, pregătindu-ne pentru activități viitoare mai complexe.
- **Resurse Utile:**
  - [Documentația Docker](https://docs.docker.com/)
  - [Curs Containerizarea Aplicațiilor](https://moodle.usm.md/course/view.php?id=6807)
