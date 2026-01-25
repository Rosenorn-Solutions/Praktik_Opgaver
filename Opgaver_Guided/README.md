# Opgaver baseret på Niveauer
> Opgaverne stillet her er baseret på niveauer og stiger i sværhedsgraderne. Ligeledes er mængden af hjælp og dokumentation tilpasset niveauet af opgaven. 
_________________

# N1
> Introduktions opgaver.

## PantMig 
### Service Overview
> Hvad er det? Hvordan virker det? Lav en simpel forklaring på hvad hver service gør, og hvordan servicene arbejder sammen. 

- Hvad er PantmigService?
- Hvad er AuthService? 
- Hvordan interagerer de med hinanden? 
    - Lav et simpelt diagram over interaktioner. 

## PK 
> I løsningen PK skal der være flere forskellige brugertyper.   Alle brugere går igennem nogle stadier der skal opnås, før de f.eks. kan være logget ind eller lave en reservation.  

### User Flow
> Bruger registrering, sikkerhed og  aktivitet. 
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


# Beginner-Friendly Documentation Models for PantmigService & AuthService

Below are 10 beginner-friendly documentation models you can create to help new developers understand and contribute to the PantmigService and AuthService projects.

---

## 1. Service Overview
**What it is:**
A simple explanation of what each service does and how they work together.

**What to include:**
- What is PantmigService?
- What is AuthService?
- How do they interact?

---

## 2. Data Models (Entities)
**What it is:**
A list of the main data objects (like User, City, Listing) and what information they store.

**What to include:**
- Short description of each entity (e.g., User, City, Notification)
- Key properties for each entity

---

## 3. API Endpoints
**What it is:**
A list of the main API routes you can call, what they do, and what data they need.

**What to include:**
- Example endpoint: `/api/auth/login`
- What it does
- What data you send and get back

---

## 4. Authentication & Authorization
**What it is:**
How users log in, get tokens, and how the system keeps things secure.

**What to include:**
- How to log in
- How tokens work
- How user roles/permissions work

---

## 5. Messaging & Integration
**What it is:**
How the services talk to each other or to other systems (like using RabbitMQ).

**What to include:**
- What messaging is used for
- Simple example of a message

---

## 6. Database & Persistence
**What it is:**
How data is saved, what databases are used, and how to set them up.

**What to include:**
- What database is used
- How to run migrations
- How to seed data

---

## 7. Background Jobs & Hosted Services
**What it is:**
Tasks that run in the background, like seeding the database or sending emails.

**What to include:**
- What background jobs exist
- What they do

---

## 8. Real-time Features & Notifications
**What it is:**
How the app sends real-time updates (like chat or notifications) to users.

**What to include:**
- What real-time features exist
- How notifications work

---

## 9. Validation & File Handling
**What it is:**
How the app checks if data is correct and how it handles file uploads.

**What to include:**
- How data is validated
- How files are checked for safety

---

## 10. Configuration & Logging
**What it is:**
How to set up the app (like with `appsettings.json`) and how logging works.

**What to include:**
- How to configure the app
- How to find logs

---

*Use these models as a starting point for writing clear, simple documentation that helps new developers get started quickly!*


_________________
