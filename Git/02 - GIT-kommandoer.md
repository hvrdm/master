### Kilde
https://git-scm.com/book/en/v2

### Installere på Linux

https://git-scm.com/download/linux

```bash
apt install git-all

# Sjekk versjon
git version
```

### Legge til bruker
https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup 

```bash
# git config lar deg sette eller hente globale konfigurasjonsvariuabler som brukes i git. Disse må settes kun en gang på hvert system

# Legg til bruker
git config --global user.name "Håvard Myrbakken"
git config --global user.email "havmyr@fagskolen-innlandet.com"

# Velg tekst editor
git config --global core.editor nano

# Sette main branch navn
# Kan velge noe annet enn main hvis versjon >= 2.28
git config --global init.defaultBranch main

# Se konfigurasjon og hvor det er lagret
git config --list
# Se konfig + hvor det er lagret
git config --list --show-origin
```

### Lage et nytt git repository
2 måter å opprette et repository:
##### 1. Opprette nytt repository
Gå til prosjektmappa og kjør:
```bash
# Opprett en undermappe som heter .git
git init <filsti>

# Legg til alle filene du vil spore
git add *.tf
git add README

# kjør en commit
git commit -m 'Versjon 1'
```
##### Klone et eksisterende repository
Lag en prosjektmappe og kjør:
```bash
git clone repository targetdirectory
```

### Sjekke prosjektstatus
```bash
git status 
```

### Sjekke endringer mellom filer
```bash
git diff
git diff file path
git diff commit id file path
git diff commitid1 commitid2 file path
git diff filepath1 filepath2
```

### Legge til filer
```bash
# Legge endrede filer til staging area
## Legge til en fil
git add filsti+navn1
## Legge til flere filer
git add filsti+navn1 filsti+navn2 filsti+navn3
## Legge til alle endrede filer
git add .


```

### Slette filer
```bash
git rm filsti+navn1
git rm filsti+navn1 filsti+navn2 filsti+navn3
git rm .
```

### Oppdatere repository
```bash
# Legger alle endrede filer som nå er i staging area inn i repo
git commit

# Med en melding
git commit -m "melding"
```

### Oppdatere remote repository
Sende det du har lokalt til det offentlige repo'et:
```bash
git push origin branchname
```
Oppdatere ditt lokale repo med endringene fra det offentlige repo'et:
```bash
git pull
git pull branchname
```

### Branching
```bash
# Opprette ny branch fra main (parentbranch)
git branch newbranch parentbranch

# Gå inn i ny branch
git switch newbranch

# Slette en branch
git branch -d newbranch

# List ut alle branch
git branchm
## Eller
git branch --list

# Slå sammen branch (merging)
git merge branch
```

### .diff filer
Sjekk hva som er forskjell på to filer:
![[Pasted image 20230328195739.png]]

### GitHub
##### Registrer bruker
https://github.com/join

#####