# Opgaver Uge 4
## Baseret på PantMigService 

> Siden introduktion til programmering og kode er nødvendig, for at fuldt forstå emnet, løsningen der arbejdes med under resten af praktikken. Forståelsen af løsningen er udgangspunktet for fremtidige opgaver, og interesse-baseret opgaver. 

Opgaver Undersøge og dokumentere PantMigService-løsningen:
- Lave eget Repo til Praktik Dokumentation
- Bruge UML-, API-diagrammer og flowcharts til at visualisere funktioner
- Selvskrive tekniske forklaringer i Servicen
    - Bruger opretter et opslag --> 
    - Hvad er et opslag? (Samling af tekst + billede + lokation + dato info i (Meta data))
    - Hvordan gemmes det? (I en row på en DB)
    - Hvordan er det bundet til bruger? (Ejer/ brugerid 1:1 forhold)
    - Hvilke processer sker der i kæden fra start til slut? (Knapper trykkes på, pop-up, input af meta data, gemningen, live opslag) 

## Specifikke opgaver
> Stillet d. 19/1
- Beskrive og forklare hvordan PantMigService -> AuthService fungerer
    - Endpoints/ AuthEndpoints (Brugerne)
    - ApplicationDbContext, ApplicationUser og RefreshToken
    - IAuthService
    - IEmailSender
    - UserAccountService, UsernameGenerator og UserManagerExtensions
