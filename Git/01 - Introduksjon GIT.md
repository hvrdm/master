### Versjonskontrollsystem
- Et system som håndterer  endringer og lagrer endringer til filer.
- Lagrer orginal-filer og en "logg" av endringer i et "repository" (repo).
- Dette gjør at flere personer kan arbeide på samme prosjektet uten at de overskriver hverandres endringer.
- Man har kontroll på hvem som har endret filer, når de ble endret og hvorfor.
- Kan arbeide på et program og legge til ny funksjonalitet uten at det stopper programmet fra å kjøre mens man arbeider med det.
- Kan reversere endringer hvis noe går galt.
- Repo kan lagres lokalt eller på server.
### Typer systemer
##### Local Version Control System (LVCS)
Kjøres lokalt for en bruker. Brukes ofte for å kunne reversere endringer som ødelegger programvare/script.
![[Pasted image 20230328112547.png]]
##### Centralized Version Control System (CVCS)
Bruker en klient/server modell. Repo lagres på server og hver bruker som vil endre noe må låse filen i repo'et (kan ikke ha flere som arbeider samtidig), kopiere det til klienten, endre, så kopiere tilbake og låse den opp igjen.
![[Pasted image 20230328112931.png]]
##### Distributed Version Control System (DVCS)
Satt opp som P2P-system, men det brukes ofte en felles server for main repo. En bruker som skal endre noe må kopiere hele repo til sin klient. På denne måten kan flere arbeide med hele systemet og samme fil samtidig. Når endringer er gjort kopierer man endrede filer til main-repo. DVCS vil da sjekke om noen av endringene som er gjort skaper konflikt.
![[Pasted image 20230328112823.png]]

### GIT
- GIT er et DVCS. 
- En Git-klient må være installert på klient-pc'er. Oftest terminal-basert.
#### GIT's 3 tilstander
![[Pasted image 20230328113656.png]]
##### GIT-filer's 3 tilstander
1. committed: Denne fila er lagret i main-repo.
2. modified: Denne fila er lagret i working directory, har blitt endret men ikke sendt til staging area.
3. staged: Endret fil som er klar til å sendes til main-repo.

### GIT Branching
Main-repo = main branch. Dette er ofte den publiserte versjonen av en programvare. Hver gang en ny klient henter repo for å gjøre en endring opprettes det en ny branch.
![[Pasted image 20230328114317.png]]
- Kan da arbeide uavhengig av andre programmerere.
- Kan arbeide på forskjellige ting samtidig.
- Eksperimentere med nye ideer uten å ødelegge det gamle.

### GitHub
GitHub er en tjeneste fra Microsoft som fungerer som en hosting tjeneste for Git. I tillegg til Git får man ekstra funksjonalitet som:
-  code review
-  documentation
-  project management
-  bug tracking
-  feature requests
Finnes andre tjenester som Gitlab og Bitbucket som gjøre mye av det samme.