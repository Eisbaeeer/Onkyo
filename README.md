Onkyo adapter
======

* Aktuelle Version: 0.7
* Anzahl verwendeter Variablen in ccu.io: 36

getestet mit Onkyo TX-NR626 

## Dokumentation

* Dieser Adapter erm�glicht die Anbindung eines Onkyo Reveivers an ccu.io
* Die erste Variable kann als Sendevariable zum Onkyo verwendet werden. Wird dort
  z.B. ein "MVLQSTN" gesetzt, wird der Befehl "Abfrage Master Volume" an den Onkyo 
  gesendet. Anschlie�end wird die Variable wieder geleert.
* Die n�chsten Variablen sind R�ckmeldungen vom Onkyo (Volume, Mute, ...), 
  welche von der Middleware gef�llt werden. 
* Die letzten Variablen (ab Startvariable +20) sind NET Variable. Diese werden 
  beim Netzwerkbetrieb (smb, HomeMedia, etc.) gef�llt. Eine Anzeige zum 
  Navigieren bieten die letzten 2 Variablen (Startvariable +30 zeigt die aktuelle 
  Position im Netzwerkbetrieb, die Startvariable +31 zeigt die Position im Men� und
  die +32 die aktuelle Anzahl / Gesamtanzahl des Verzeichnisses).
  
* Konfiguration �ber settings.js unter adapter:
  enabled:  true|false
  IP:       xxx.xxx.xxx.xxx (Onkyo Reveiver)
  Port:     xxxxx  (Onkyo Port)
  FirstId:  xxxxxx  (Erste ID, �ber 100000 verwenden!) 

## Todo/Roadmap

* HTML in settings.js integrieren 
* chunk in settings.js auslagern
* abrufen der Variablen vom Onkyo (INIT)
* Requests an Eisbaeeer@gmail.com

## Changelog

### 0.7
* Debug mode in settings.json eingebaut
* Variable +33 (Listening Mode) hinzugef�gt
* Variable +34 (Audio Information) hinzugef�gt
* Variable +35 (Video Information) hinzugef�gt

### 0.6.3
* Bug in "Navigation bei Netzwerk Modus"

### 0.6.2
* Navigation erweitert (Einzelposition VAL31, Summe VAL32)

### 0.6.1
* Small bugfixes
* Navigation im Netzwerkmodus hinzugef�gt

### 0.6
* First launch with basic functions

## Lizenz

Copyright (c) 2014 Eisbaeeer [http://www.weimars.net](http://www.weimars.net)

Lizenz: [CC BY-NC 3.0](http://creativecommons.org/licenses/by-nc/3.0/de/)

Sie d�rfen das Werk bzw. den Inhalt vervielf�ltigen, verbreiten und �ffentlich zug�nglich machen,
Abwandlungen und Bearbeitungen des Werkes bzw. Inhaltes anfertigen zu den folgenden Bedingungen:

  * **Namensnennung** - Sie m�ssen den Namen des Autors/Rechteinhabers in der von ihm festgelegten Weise nennen.
  * **Keine kommerzielle Nutzung** - Dieses Werk bzw. dieser Inhalt darf nicht f�r kommerzielle Zwecke verwendet werden.

Wobei gilt:
Verzichtserkl�rung - Jede der vorgenannten Bedingungen kann aufgehoben werden, sofern Sie die ausdr�ckliche Einwilligung des Rechteinhabers dazu erhalten.
Die Ver�ffentlichung dieser Software erfolgt in der Hoffnung, da� sie Ihnen von Nutzen sein wird, aber OHNE IRGENDEINE GARANTIE, sogar ohne die implizite Garantie der MARKTREIFE oder der VERWENDBARKEIT F�R EINEN BESTIMMTEN ZWECK. Die Nutzung dieser Software erfolgt auf eigenes Risiko!
=====
This project needs ccu.io
This project allow connection to Onkyo network enabled receiver with ISCP protocol
