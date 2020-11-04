:css: style.css

.. title:: AdGuard Home Home Assistant Addon

----

:data-x: r2400

.. image:: images/AdGuard-Home.png
   :width: 350px

Home Assistant Addon: AdGuard Home
==================================

Ein (Ad)Blocker im Heim-Netzwerk

Markus Pöschl

----

.. image:: images/tldr.jpg

Agenda
------

* AdGuard Home
* Wie funktioniert ein DNS?

  * Was ist DoT/DoH?

* Das Addon im Einsatz
* Wo gibt es gute Filterlisten?

----

.. image:: images/AdGuard-Home.png
   :width: 350px

AdGuard Home
------------

* Blockiert, Protokolliert DNS Anfragen von

  * Werbung
  * Tracking
  * NSFW

* Verwaltung benutzter DNS Server
* Unterstützt "DNS over TLS" (DoT) und "DNS over HTTPS" (DoH)


* Installation im Netzwerk
* Keine Veränderung auf den Endgeräten

.. note::

  * AdGuard Home als eigener DNS Server im Netzwerk
  * Geeignet für IoT, da keine Veränderung an Gerät
  * Pi-Hole ist ähnlich, bietet allerding nicht DoT oder DoH out of the box

----

.. image:: images/DNS.png
   :class: big

DNS ?
-----

* "Domain Name System"
* Zuständig für Domain-Namen
* Vergleichbar mit dem Telefonbuch
* Internetanbeiter gibt eigenen als Standard vor
* Werden teilweise für Zensur benutzt

Öffentliche DNS Server:

* `8.8.8.8` - Google Public DNS
* `1.1.1.1` - Cloudflare DNS
* `46.182.19.48` - digitalcourage.de

----

:data-x: r0
:data-y: r1200

.. image:: images/DNS.png
   :class: big

DNS ist sicher?
---------------

Standardmäßig: **Nein**

* Anfragen sind nicht verschlüsselt
* Lesbar für alle
* Angriff durch falsche Antworten

.. note::

  * Mitschneiden auf DNS Port 53 -> Surfverhalten
  * Anderer Server für google.de

----

.. image:: images/DNS.png
   :class: big

DNS over TLS (DoT)
------------------

* Verschlüsselung der Namensauflösung mit TLS
* Kein Mitlesen möglich
* Anfragen verraten nur das es eine DNS Anfrage ist

.. note::

  * DNS-Anfragen Typ durch Port 853 ersichtlich

----

.. image:: images/DNS.png
   :class: big

DNS over HTTP (DoH)
------------------

* Verschlüsselung der Namensauflösung mittels einer HTTPS Verbindung
* Kein Mitlesen möglich
* Wenn der DNS Server auch auf Port 433 läuft, ist die Anfrage als HTTPS-Anfrage "getarnt"

----

:data-x: r2400

.. image:: images/DNS.png
   :class: big

AdGuard Home Addon
------------------

* Eigener DNS im Heimnetz
* Der Router muss die IP Adresse des Servers kennen
* **Home Assistant braucht einen eigenen DNS**

.. note::

  * Router verteilt DNS Server bei Netzwerkanmeldung mit
  * HA muss Namen auflösen, auf sich selbst dreht Kreis

----

:data-x: r0
:data-y: r1200

.. image:: images/DNS.png
   :class: big

AdGuard Home DNS Server
-----------------------

TBD DNS Settings

----

.. image:: images/DNS.png
   :class: big

AdGuard Home Filterlisten
-------------------------

TBD Filter und Kinderschutz

----

:data-x: r2400

.. image:: images/DNS.png
   :class: big

Filterlisten finden
-------------------

TBD Filterlisten
