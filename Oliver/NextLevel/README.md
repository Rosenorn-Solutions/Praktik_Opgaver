# Advanceret kommende opgaver 

**Profil-setup wizard**

- **Kontekst**: Efter login (Login.tsx) lander brugere på profilsiden (Profile.tsx), som kan virke overvældende. Vi skal have et guidet, trin-for-trin “Profil-Setup”-forløb for nye brugere og dem, der vil opdatere deres profil.
- **Mål**: Lav en multi-step wizard, der kører automatisk for ufuldstændige profiler og kan startes igen senere. Gem progression pr. trin, tillad genoptagelse, slut med review og send brugeren tilbage til profilsiden.

**Foreslåede trin (justér efter behov)**
- Basisinfo: navn, titel/headline, lokation.
- Kontakt: e-mail, telefon, links.
- Kompetencer: tilføj/fjern tags.
- Erfaring & Uddannelse: mindst én post hver, eller tillad skip med advarsel.
- Jobpræferencer: lokationstype, foretrukne roller, kategorier.
- Review & bekræft.

**Routing og triggere**
- Tilføj route `/profile/setup` til wizarden.
- Efter succesfuldt login: tjek profil-fuldkommenhed; hvis ufuldstændig → redirect til `/profile/setup`, ellers til `/profile`.
- På profilsiden: knap “Rediger via setup wizard” der linker til `/profile/setup`.

**Definition af “profil komplet” (kan justeres)**
- Har navn og headline/titel.
- Har lokation (by/region).
- Har kontakt-e-mail.
- Har mindst én kompetence.
- Har mindst én erfaring eller uddannelse.
- Mangler noget af ovenstående → ufuldstændig.

**Data og API’er**
- Brug `useUser` for `userId` og `accessToken`.
- Brug eksisterende API-klienter fra ApiFactory.ts og profil-API’er i src/findjobnu-api/ (ProfileApi, UserProfileApi, WorkProfileApi osv.).
- Hent initial profil ved wizard-load; gem per trin via PATCH/PUT når brugeren går videre. Hold lokal state og evt. localStorage for robusthed.

**UI/UX-krav**
- Stepper med labels og progression (x/6).
- Næste/Tilbage; Næste disabled indtil påkrævede felter er valide.
- Inline validering; “Spring over” på ikke-kritiske sektioner med mild advarsel.
- Hold formularer fokuserede og korte; slutskærm med “Afslut” der returnerer til `/profile`.
- Genbrug Tailwind/daisyUI-stil.
- Se components fra DaisyUI: https://daisyui.com/components/
-- F.eks. kan 'Steps' og 'Progress' bruges.

**Komponenter der skal laves**
- Side: `ProfileSetupWizard` (ejer state, routing, data fetch/save).
- Layout: `WizardLayout` (stepper, progress, nav-knapper).
- Steps: BasicInfoStep, ContactStep, SkillsStep, ExperienceEducationStep, PreferencesStep, ReviewStep (fx under src/components/profileSetup/).
- Evt. shared helpers/typer tæt på wizarden eller i helpers.

**State og validering**
- Parent holder wizard-state; giv slice + setters til steps.
- Påkrævet: navn, headline/titel, lokation, e-mail; kompetencer må ikke være tomme; erfaring/uddannelse mindst én eller skip med advarsel; præferencer mindst ét valg eller skip med advarsel.
- Blokér Næste hvis påkrævede felter er ugyldige; markér skip som advarsel i review.

**Fejlhåndtering**
- Ved save-fejl: vis inline/toast; bevar lokal state så brugeren kan prøve igen.
- Tillad retry pr. trin; tab ikke data ved navigation.

**Test (tilføj til eksisterende setup)**
- Step-navigation: Næste disabled indtil valid; Tilbage virker.
- Skip-adfærd: skip tilladt, viser advarsels-badge/flag.
- Redirect-logik: ufuldstændig profil → wizard; fuld profil → profil.
- Review-skærm viser samlet data før Afslut.

**Implementeringsrækkefølge (forslag)**
- Tilføj `/profile/setup` route og scaffold wizard-skel med mock-steps.
- Wire validering til at gate Næste/Afslut.
- Fetch initial profildata; hydrer wizard-state.
- Implementér per-step save på Næste/Afslut; optimistisk UI.
- Opdatér login-redirect-logik så ufuldstændige profiler går til wizarden.
- Tilføj “Rediger via setup wizard”-knap på profilsiden.
- Tilføj tests for navigation, validering og redirects.
- Tilføj kort README-note i wizard-mappen om flow og fuldkommenhedsregler.

**Ide til bred opgave beskrivelse:**
- Start med at få forståelse af produkt (Jobnu, PantMig) --> hvad er struktur, funktioner, løsning samlet, løsning for brugerne
- Identificere områder der skal dokumenteres, så løsning kan komme på Appstores --> udgangspunkt i tillært viden + brug af standarder for pre-release på appstore 
- Identificere områder for "egen interesse" --> jeres hoved-fokus for praktikken, varende to måneder. (Kan være flere ting!)