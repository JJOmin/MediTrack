# MediTrack
Ein System zur Verwaltung und Überwachung von Patientendaten, einschließlich Vitaldaten ( und Behandlungshistorie) mit automatischen Benachrichtigungen bei kritischen Werten.

**Funktonale Anforderungen:**
* **Patientenregistrierung und Authentfizierung:** Paienten und medizinisches Personal sollten sich registrieren und anmelden können.
* **Erfassung von Patientendaten:** Eingabe und Verwaltung von grundlegenden Gesundheitsinformationen (Name, Geburtsdatum, Krankheitsgeschichte).
* **Eingabe von Vitaldaten:** Patienten oder medizinisches Personal können Vitaldaten (z. B. Blutdruck, Puls, Temperatur) eingeben.
* **Benachrich.gungssystem:** Automatische Benachrichtigungen an Ärzte oder Pflegepersonal, wenn Vitalwerte kritische Schwellen überschreiten.
* **Behandlungsübersicht:** Zugriff auf eine Historie der bisherigen Behandlungen und medizinischen Eingriffe.

## Was ist Git und warum sollte es verwendet werden?

**Git** ist ein verteiltes Versionskontrollsystem, das hilft, Änderungen an Dateien zu verfolgen.  
Es wird vor allem für Softwareprojekte verwendet, eignet sich aber für jede Art von Dokumenten oder Projekten, bei denen mehrere Personen zusammenarbeiten.

### Vorteile von Git:

- **Versionskontrolle:** Jede Änderung wird gespeichert, sodass man zu früheren Versionen zurückkehren kann.
- **Teamarbeit:** Mehrere Personen können gleichzeitig am gleichen Projekt arbeiten, ohne dass die Arbeit der anderen verloren geht.
- **Branches:** Neue Funktionen oder Änderungen können in separaten Zweigen (Branches) entwickelt werden, ohne den Hauptprojektstand zu beeinflussen.
- **Sicheres Backup:** Durch das Pushen in ein Remote Repository (z. B. GitHub) ist die Arbeit gesichert und von überall zugänglich.

### Beispiel:
Ein Team arbeitet an einem Dokument. Mit Git können sie:

1. Änderungen lokal speichern (committen)
2. Änderungen mit dem Team teilen (pushen)
3. Konflikte erkennen und lösen, wenn mehrere Leute gleichzeitig Änderungen machen

Git hilft also, Ordnung zu behalten und Fehler rückgängig zu machen, was besonders in Teamprojekten sehr wichtig ist.

## Grundlegende Git-Befehle

Hier werden die wichtigsten Git-Befehle für den Einstieg erklärt.

###  git init
Initialisiert ein neues Git-Repository im aktuellen Ordner.

```bash git init```

### git status
Zeigt den aktuellen Status der Dateien an (geänderte, neue oder nicht verfolgte Dateien).

```bash git status```

### git add
Fügt Änderungen zur nächsten Commit-Phase hinzu.

```bash git add```

```bash git add dateiname.txt``` 


### git commit
Speichert die Änderungen im lokalen Repository.

```bash git commit -m "Beschreibung der Änderungen"```

### git log
Zeigt die Historie aller Commits an.

```bash git log```


### git remote
Verwaltet Remote-Repositories (GitHub, GitLab).

```bash git remote add origin URL_des_Repositories```

### git push / git pull
Push: Änderungen ins Remote-Repository hochladen
Pull: Änderungen vom Remote-Repository holen und lokal zusammenführen

```bash git push origin main```

```bash git pull origin main```


## Branches und Merge-Konflikte

### Was ist ein Branch?
Ein paralleler Entwicklungszweig in Git.  
Man kann damit neue Funktionen oder Änderungen entwickeln, ohne den Hauptzweig (main) zu verändern.

---

### Branch erstellen und wechseln

### Neuen Branch erstellen
```bash git branch neuer-branch```
### Zum Branch wechseln
```bash git checkout neuer-branch```
### Branch zusammenführen (Merge)

```bash git checkout main```

```bash git merge neuer-branch ```

### Merge-Konflikte lösen
Wenn zwei Änderungen kollidieren, zeigt Git:
```bash
<<<<<<< HEAD
Text von main
=======
Text vom Branch
>>>>>>> neuer-branch
```

Dann:
1. Gewünschte Version auswählen oder zusammenführen
2. Datei als gelöst markieren:
```bash git add README.md```

```bash git commit -m "Merge-Konflikt gelöst"```


### Git in IntelliJ/PyCharm verwenden

IntelliJ und PyCharm haben eine **integrierte Git-Unterstützung**, die viele Befehle über die Benutzeroberfläche ausführt.

---

### 1. Repository klonen
1. Öffne IntelliJ/PyCharm → **Get from Version Control**  
2. Repository-URL eingeben (z. B. `https://github.com/deinname/git-handout.git`)  
3. Zielordner auswählen → **Clone**



### 2. Änderungen committen
1. Dateien im Projekt ändern  
2. Menüleiste → **Git → Commit**  
3. Commit-Nachricht schreiben  
4. **Commit** oder **Commit and Push** auswählen

---

### 3. Push ins Remote Repository
- Wenn nur committen: lokal gespeichert  
- Mit **Push** werden die Änderungen auf GitHub/GitLab hochgeladen  
  Menüleiste → **Git → Push**  

---

### 4. Branches verwalten
1. Menüleiste → **Git → Branches**  
2. Neuer Branch: **New Branch** → Name eingeben  
3. Wechseln: auf Branch klicken → **Checkout**  
4. Merge oder Pull Request: Über **Git → Merge Changes** bzw. auf GitHub erstellen

---

### Vorteile der IDE-Integration
- Visualisierung von Änderungen  
- Einfacher Zugriff auf Branches, Commits, Push/Pull  
- Merge-Konflikte werden direkt hervorgehoben

### Nützliche Git-Tools und Plattformen
  GitHub / GitLab / Bitbucket
  Sourcetree / GitKraken
  VSCode
  IntelliJ / PyCharm
  
---

## Dokumentation der Zusammenarbeit

| Teammitglied | Beitrag                                                         |
|----------|-----------------------------------------------------------------|
| Maximilian Jahrmärker| Erstellen des Git-Repositories und Anlegen der `README.md`-Datei. |
| Norma Roth | Ausformulierung und Beschreibung der Inhalte in der `README.md`. |

