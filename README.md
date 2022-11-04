Titel:      Dokumentattion von Git/Github Repository
Date:       03-11-2022
Author:     Renato Palavecino, bearbeitet von Stefan Sell
Keywords:   Git, Github, Linux

# Bilder und Links
![ArchLinux](https://github.com/StefanSellIT/Projekt1_ArcoLinux/blob/master/Bilder/archlinux.jpg)
[ArchWiki](https://wiki.archlinux.org/)

# ssh Schlüssel erstellen
ssh-keygen

ssh -i Ubuntu-StefanS-Key.pem ec2-54-93-36-94.eu-central-1.compute.amazonaws.com


# Git Repository loka erstellen

## Projekt Umgebung vorbereiten

git remote add git@github.com:StefanSellIT/Projekt1_ArcoLinux.git


#### Erstellen Sie ein Vezeichnis mit dem Name Projekt1

    cd
    mkdir Projekt1

#### Dateien und Verzeichnisse fuer das Projekt "Statische Webseite"

    touch index.html style.css backend.py 
    mkdir Secret
    cd Secret
    touch Geheimnisse.txt
    cd ..
    mkdir Bilder
    cd Bilder
    touch Bild1.jpg Bild2.jpg Bild3.jpg Bild1.png Bild2.png
    cd ..
    touch .gitignore

#### Falls dass Sie sensibel Daten Verstecken wollen, schreiben Sie welche in .gitignore File und speicher die Aenderungen

    nano .gitignore

Code-Blocke

    Secret/
    Bilder/*.png

#### Git Umgebung vorbereiten

    git config --global user.name "Name Nachname"
    git config --global user.email "valid-email"

#### git Kontrollversionierung initialisiren

    git init

#### From Working Area nach Stagin Area nach Repositoty

    git status
    git add -A
    git commit -m "Erstes Commit"
    git status
