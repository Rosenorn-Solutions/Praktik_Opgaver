# Opgaver baseret på Niveauer
> Opgaverne stillet her er baseret på niveauer og stiger i sværhedsgraderne. Ligeledes er mængden af hjælp og dokumentation tilpasset niveauet af opgaven. 
_________________




# N1
> Introduktions opgaver.

## PK 
> I løsningen PK skal der være flere forskellige brugertyper.   Alle brugere går igennem nogle stadier der skal opnås, før de f.eks. kan være logget ind eller lave en reservation.  
-----

## Klasse diagram
### User
> Bruger med inhold og aktivitet på platformen. Lav modeller eller diagrammer der viser:
- Indhold af en brugers profil:
    - Privatbruger
    - Virksomhedsbruger
- Listing Service Domæne Model: 
    - Listing (opslag)
    - Katorier
    - TilgængelighedsSlot
    - ListingMedia (Billeder) 
- Booking Service Domæne Model:
    - Booking entity med status states
    - Booking-lister og booking-bruger relationships
    - Booking timlines og lifecycles 
- Betalings (Payment) Service Domæne Model:
    - Betalings-provider integration
    - Booking-Betalings forhold
- Besked (Messaging) Domæne Model: 
    - Besked og kommentar-Entities
    - Bruger-tråd forhold (Ejer/ Lejer)
    - Thread-Listing association (Tråd bundet til listing/ bruger)
- Media Service Domæne Model:
    - Medie metadata-entities
    - Upload processing
    - Storage abstraktions lag
- Notifikations Service Domæne Model:
    - Notifikations template
        - Event template
    - Notifikations-outbox til delivery-pipeline
    - Event-to-notification mapping

### Cross-reference
- API-gateway integration pattern:
    - Service discovery
    - Request/ response pipeline
- Event bus
    - Domæne events (ListingCreated, BookingConfirmed, PaymentCapture)
    - Event publishers og subscribers
    - Thread update (Review/ kommentar)
-  Common types:
    - Penge, Adresser, TlfNummer, Lokation (Alt der kan genbruges af andre services skal her ned)
    - Fælles Enums (Currency, Statustype)¨
    - Results/ Reponse patterns


### Infrastructure og Patterns
- 

Lav en model der viser: 
- En bruger med to opslag
    - Opslag 1: En trailer -> Tilgængelig fra Nu til 31. December 2026 
    - Opslag 2: En trailer -> Tilgængelig fra om to dage - enhed er optaget
- Viser distance-funktionen når der søges efter en enhed


![Alt text](https://d3n817fwly711g.cloudfront.net/uploads/2012/02/Class-diagram.jpg)

### User Flow
> Bruger registrering, sikkerhed og  aktivitet. 
- Lav en model der viser registrering på PK som privat-bruger 
    - PK åbnes, personen trykker på opret bruger, tilføjer informationer, afslutter og bliver registreret 
- Lav en model der viser registrering på PK som virksomheds-bruger 
    - PK åbnes, personen trykker på virksomheds-bruger, tilføjer information, afslutter og bliver registreret
- Lav en model der viser kommunikation mellem brugere
- Lav en model der viser Authentication og Authorization (Auth flow)

![Alt text](https://cdn-proxy.slickplan.com/wp-content/uploads/2021/07/website-login-user-flow.png)
-----




-----

### Booking flow
> Lav modeller over følgende
- Flow af booking af en trailer
- Flow på at få lejet sin trailer ud

![Alt text](https://www.researchgate.net/profile/Samrat-Dey-3/publication/338071049/figure/fig10/AS:896784356356116@1590821460568/Flowchart-of-Booking-process.ppm)

-----

### Data og Databaser
- Lav et diagram over DB (Bruger) og relation mellem bruger og opslag
- Lav en model over dataene i PK (alle typer og deres relationer)
     - Brug beskrivende sprog til at forklare hvad og hvordan. 

*Nedenunder ses en model for User Registration Flow Nedenunder er en model, der viser hvordan brugeren starter på start punktet og møder log-in/ registrerings muligheder.* 





_________________
# N2
> Introduktions opgaver + 10% 

## PantMig 

### Service Overview
> Lav dokumentation baseret på repository: https://github.com/Rosenorn-Solutions/PantmigService

> Hvad er det? Hvordan virker det? Lav en simpel forklaring på hvad hver service gør, og hvordan servicene arbejder sammen. 

- Hvad er PantmigService?
- Hvad er AuthService? 
    - Beskriv authentication/authorization flow og krav
- Hvordan interagerer de med hinanden? 
    - Lav et simpelt diagram over interaktioner. 

### PantmigService dokumentation

- Lav en kort service-beskrivelse (formål, ansvar og scope)
- Beskriv høj-niveau arkitektur (lag, centrale moduler og afhængigheder)
- Kortlæg API-endpoints (input/output, statuskoder og fejlscenarier)
- Lav en “data-kontrakter” sektion for DTO’er (felter, krav, validering)
- Dokumentér centrale domæne-modeller og deres relationer
- Beskriv konfiguration (miljøvariabler, secrets og default-værdier)
- Notér baggrundsprocesser/hosted services (hvad de gør og hvornår de kører)
- Lav en “Getting Started” sektion (build, run, test og lokal opsætning)
- Lav en fejl- og supportsektion (typiske fejl, troubleshooting, logs)


### Service
- Lav en Service Overview Model, der viser high-level ansvar og funktioner for AuthService og PantmigService
     - Vis med model hvilke regler de skal følge
     - Bonus: Er der nogen åbne huller?
-----

### Messaging
- Lav en model der viser Real Time Messaging (message broker interactions)
     - Forklar forhold mellem publisher/ consumer
- Lav et sekvensdiagram for en besked fra client → broker → consumer
- List events/queues og hvad de bruges til
- Beskriv retries, dead-lettering og idempotency (hvad sker ved fejl?)
- Angiv krav til payloads (schema, versionering, størrelse)
-----

### Validation og File Handling
- Lav en model der viser hvordan File Validation fungerer ved upload
- Lav en model der viser Listing Validation og publication
- Dokumentér fil-typer, størrelsegrænser og sikkerhedstjek
- Beskriv virus-/malware-scan flow (hvis relevant) og fallback
- Beskriv hvor filer lagres (path/bucket), og hvordan adgang styres
- Lav en tjekliste for fejlhåndtering (hvad vises til bruger, hvad logges)
-----


### Handlinger
- Lav en liste over handlinger der laves, og hvilke relationer handlinger har til hinanden og løsningen



_________________


# N3
> Beskriv automatiske processer, og hvilken betydning de har for løsningernes 

### Background jobs og Hosted Services

- Enpoints og deres funktioner
- IAuthService 

###

###

_________________
# N4
>



_________________

# N5
>



_________________
>>    - Endpoints/ AuthEndpoints (Brugerne)
>>    - ApplicationDbContext, ApplicationUser og RefreshToken
>>    - IAuthService
>>    - IEmailSender
>>    - UserAccountService, UsernameGenerator og UserManagerExtensions