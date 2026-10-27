# BVB Salesforce Admin Workshop

Übungs-Repository für den zweitägigen Salesforce-Admin-Workshop.

## So arbeitest du mit dem Repo

```bash
# 1. Repo klonen
git clone git@github.com:amirjafari-ger/bvb-schulung.git
cd bvb-schulung

# 2. Eigene Org verbinden
sf org login web --alias bvb-dev --set-default

# 3. Eigenen Branch anlegen
git switch -c feature/bvb-workshop-<vorname>

# 4. Alles aus der Org holen, was im Manifest steht
sf project retrieve start --manifest manifest/package.xml

# 5. Committen und pushen
git add force-app manifest
git commit -m "BVB Workshop: Spieler, App, Rechte, Flow"
git push -u origin feature/bvb-workshop-<vorname>
```

## Struktur

| Pfad | Inhalt |
|---|---|
| `manifest/package.xml` | Liste der Komponenten aus dem Workshop |
| `force-app/main/default/` | Metadaten aus deiner Org (nach dem Retrieve) |
| `sfdx-project.json` | Projektkonfiguration der Salesforce CLI |

Bitte nie direkt auf `main` pushen – immer über den eigenen Branch.
