# Arbeidskrav i Cloud: docker-compose

Denne består av en web (nginx som omvent proxy), API (Golang:alpine) og db (MySQL).
Disse er satt opp til å kjøre i Docker-containere ved hjelp av docker-compose. 

## Prosjektets struktur
arbeidskrav/
├── Api/
│   ├── main.go > hoved Go-kildekoden
│   ├── go.mod > Go-moduledefineringen
│   ├── go.sum > Go-avhengigheter
│   ├── Dockerfile > bygger container for Golang API
├── nginx/
│   ├── default.conf > Konfigurasjonsfilen for Ngins som setter opp omvendt proxy
│   └── Dockerfile > Bygger Nginx-container
├── db/
│   └── init.sql > SQL fil som intiliserer MySQL-databasen
├── .gitignore
├── docker-compose.yml > Definerer de tre tjenstene, og deres avhengigheter.
└── README.md



### Krav
- [Docker] (https://www.docker.com/get-started)

### Klone og bygge prosjektet
- git clone
- cd Test-Compose
- docker-compose up --build

### TEST prosjektet
"curl http://localhost/entitiets" i terminalen, eller "http://localhost/entitiet" i nettleseren.

#### Feilsøking
- docker-compose logs
  
