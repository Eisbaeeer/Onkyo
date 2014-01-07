Onkyo adapter
======

* Aktuelle Version: 0.6.1
* Anzahl verwendeter Variablen in ccu.io: 32

getestet mit Onkyo TX-NR626 

## Dokumentation

* Dieser Adapter ermöglicht die Anbindung eines Onkyo Reveivers an ccu.io
* Es werden Variable in der ccu.io erstellt.
* Die erste Variable kann als Sendevariable zum Onkyo verwendet werden. Wird dort
  z.B. ein "MVLQSTN" gesetzt, wird der Befehl "Abfrage Master Volume" an den Onkyo 
  gesendet. Anschließend wird die Variable wieder geleert.
  
* Konfiguration über settings.js unter adapter:
  enabled:  true|false
  IP:       xxx.xxx.xxx.xxx (Onkyo Reveiver)
  Port:     xxxxx  (Onkyo Port)
  FirstId:  xxxxxx  (Erste ID, über 100000 verwenden!) 

## Todo/Roadmap

* HTML in settings.js integrieren 
* chunk in settings.js auslagern
* abrufen der Variablen vom Onkyo (INIT)
* Requests an Eisbaeeer@gmail.com

## Changelog

### 0.6.1
* Small bugfixes
* Navigation im Netzwerkmodus hinzugefügt

### 0.6
* First launch with basic functions

## Lizenz

Copyright (c) 2014 Eisbaeeer [http://www.weimars.net](http://www.weimars.net)

Lizenz: [CC BY-NC 3.0](http://creativecommons.org/licenses/by-nc/3.0/de/)

Sie dürfen das Werk bzw. den Inhalt vervielfältigen, verbreiten und öffentlich zugänglich machen,
Abwandlungen und Bearbeitungen des Werkes bzw. Inhaltes anfertigen zu den folgenden Bedingungen:

  * **Namensnennung** - Sie müssen den Namen des Autors/Rechteinhabers in der von ihm festgelegten Weise nennen.
  * **Keine kommerzielle Nutzung** - Dieses Werk bzw. dieser Inhalt darf nicht für kommerzielle Zwecke verwendet werden.

Wobei gilt:
Verzichtserklärung - Jede der vorgenannten Bedingungen kann aufgehoben werden, sofern Sie die ausdrückliche Einwilligung des Rechteinhabers dazu erhalten.

Die Veröffentlichung dieser Software erfolgt in der Hoffnung, daß sie Ihnen von Nutzen sein wird, aber OHNE IRGENDEINE GARANTIE, sogar ohne die implizite Garantie der MARKTREIFE oder der VERWENDBARKEIT FÜR EINEN BESTIMMTEN ZWECK. Die Nutzung dieser Software erfolgt auf eigenes Risiko!Onkyo
=====

This project needs ccu.io
This project allow connection to Onkyo network enabled receiver with ISCP protocol
