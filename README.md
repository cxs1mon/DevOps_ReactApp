
# App Ref. Card 02
React Application (serverless)

---
title: App Ref. Card 01
author: Rinaldo Lanza, BBW
date: 12. Februar 2023
---

Link zur Übersicht<br/>
https://gitlab.com/bbwrl/m347-ref-card-overview


### Projekt bauen und starten
Die Ausführung der Befehle erfolgt im Projektordner
Builden mit Node/npm<br/>
```$ npm install```

Das Projekt wird gebaut und die entsprechenden Dateien unter dem Ordner node_modules gespeichert.
Die App kann nun mit folgendem Befehl gestartet werden<br/>
```$ npm start```

Die App kann nun im Browser unter der URL http://localhost:3000 betrachtet werden.


### Dockerhub
Um das Projekt auf Dockerhub zu deployen, muss folgendes gemacht werden:
- .github/workflow.main.yaml erstellen
- Workflow beispiel von https://bbw-it.github.io/324_main_rupe/12_CI-CD_Pipelines/12.3.2_GitHubCIMitDeploy/ Docker Hub kopieren
- main.yaml anpassen
    - images zu ${{ secrets.DOCKERHUB_USERNAME }}/react-app ändern
    - Steps Set up JDK & Build & test mit Set up Node.js & Install dependencies and build React app ersetzen (hilfe ChatGPT)
- Dockerfile erstellen und befüllen (hilfe ChatGPT)
  - falls noch nicht bereits gemacht:
  - 2 Secrets im Github Repository hinterlegen
      - DOCKERHUB_USERNAME: Username von Dockerhub
      - DOCKERHUB_TOCKEN: kann man auf Dockerhub unter account settings -> Personal Access Tokens erstellen
- commit und push -> workflow wird automatisch ausgeführt und kann im action tab des repositories überprüft werden
- nach dem pushen überprüfen
    - ob der workflow korrekt durchgelaufen ist: https://github.com/cxs1mon/DevOps_ReactApp/actions
    - ob es korrekt deployed wurde: https://hub.docker.com/repository/docker/dedede456/react-app/general



