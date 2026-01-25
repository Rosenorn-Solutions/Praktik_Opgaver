# Opgaver baseret på Niveauer
> Opgaverne stillet her er baseret på niveauer og stiger i sværhedsgraderne. Ligeledes er mængden af hjælp og dokumentation tilpasset niveauet af opgaven. 
_________________

# N1
> Introduktions opgaver.

## Opgave PK Klasser 

I løsningen PK skal der være flere forskellige brugertyper. 

Alle brugere går igennem nogle stadier der skal opnås, før de f.eks. kan være logget ind eller lave en reservation. 


Samme idé er til stede i PK og følgende brugere og flow igennem løsningen skal dokumenteres.

## Service Overview
> Hvad er det? Hvordan virker det? Lav en simpel forklaring på hvad hver service gør, og hvordan servicene arbejder sammen. 

- Hvad er PantmigService?
- Hvad er AuthService? 
- Hvordan interagerer de med hinanden? 
    - Lav et simpelt diagram over interaktioner. 


### User Flow
> Registrering 
- Lav en model der viser registrering på PK som privat-bruger 
- Lav en model der viser registrering på PK som virksomheds-bruger 
- Lav en model der viser kommunikation mellem brugere
- Lav en model der viser Authentication og Authorization (Auth flow)

### User
> Bruger med inhold og aktivitet på platformen
>> Lav modeller eller diagrammer der viser:
- Indhold af en brugers profil
- En bruger med to opslag
    - Opslag 1: En trailer -> Tilgængelig fra Nu til 31. December 2026 
    - Opslag 2: En trailer -> Tilgængelig fra om to dage - enhed er optaget
- Der viser distance-funktionen når der søges efter en enhed

```mermaid


```

### Booking flow
> Lav modeller over følgende
- Flow af booking af en trailer
- Flow på at få lejet sin trailer ud

### Data og Databaser
- Lav et diagram over DB (Bruger) og relation mellem bruger og opslag

*Nedenunder ses en model for User Registration Flow Nedenunder er en model, der viser hvordan brugeren starter på start punktet og møder log-in/ registrerings muligheder.* 
![ALTTEXT](https://creately.com/static/assets/guides/user-flow-diagram/user-registration-flow-diagram.webp)

_________________
# N2
> Introduktions opgaver + 10% 


### Service
- Lav en Service Overview Model, der viser high-level ansvar og funktioner for AuthService og PantmigService

### Messaging
- Lav en model der viser Real Time Messaging (message broker interactions)


### Validation og File Handling
- Lav en model der viser hvordan File Validation fungerer ved upload
- Lav en model der viser Listing Validation og publication


![ALTTEXT](https://imgs.search.brave.com/KE45xOGUTM8uLXp195sxfl0LycXPKpC8O3Pnn25GeDw/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly9jbGlj/a3VwLmNvbS9ibG9n/L3dwLWNvbnRlbnQv/dXBsb2Fkcy8yMDI0/LzExL1VNTC1hY3Rp/dml0eS1kaWFncmFt/LnBuZw)




_________________


# N3
> 

### Background jobs og Hosted Services



_________________
# N4
>



_________________

# N5
>




_________________
