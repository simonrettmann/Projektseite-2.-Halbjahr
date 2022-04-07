<html>
<head>
<h1 align="center"> Novum Hotplate 2.0 - Projektseite <img align="center" src="https://user-images.githubusercontent.com/88385654/161974070-e4a0fdf8-0add-486b-9a34-8e11fd9d6ffb.png">
 </h1>

<h2 align="center"> Der arduinogesteuerte Gaskocher mit Websteuerung </h2>
</head>
<img align="right" alt="Animation" width="500" height="300" src="https://user-images.githubusercontent.com/88385654/162214959-08398ea4-f3ca-4dee-871f-ff785f1c03f4.gif">
<h4 align="left"> Ein Projekt von David Borgmann und Simon Rettmann</h4>
<h4 align="left"> Stormarnschule Ahrensburg <br/> Informatik, Bl <br/> Schuljahr 2021/22, 2. Halbjahr </br> </h4>

<body>
<h4 align="left"> &#10132; <a href="https://github.com/simonrettmann/Projektseite"> Projektseite 1. Halbjahr</a> </h4> 
<h4 align="left"> &#10132; <a href="https://github.com/simonrettmann/Stundenprotokolle-2.-Halbjahr"> Stundenprotokolle 2. Halbjahr</a> </h4> 
<h4 align="left"> &#10132; <a href="https://github.com/simonrettmann/Stundenprotokolle"> Stundenprotokolle 1. Halbjahr</a> </h4> 
<h4 align="left"> &#10132; <a href="https://www.youtube.com/channel/UCEljeGxqUxyXQlMq9Q-U8_w"> YouTube Kanal - Novum hotplate</a> </h4>
<h4 align="left"> &#10132; <a href="http://gaskocher.stormarnschueler.de/index.php"> Website als Steuerzentrale für den Gaskocher </a> </h4> 
</body>
<hr>
<body>
  
<h2 align="center"> Inhaltsverzeichnis </h2>
  
<b> 1. Allgemeines </b>
<br/>
<ul>
&#10148; <a href="#rückblick"> 1.1 Ausgangslage</a> <br/>
&#10148; <a href="#zielsetzung"> 1.2 Zielsetzung und Vision</a> <br/>
&#10148; <a href="#lernen"> 1.3 erforderliche Fähigkeiten und Vorbereitungen</a> <br/>
&#10148; <a href="#hardware"> 1.4 erforderliche Hardware</a> <br/>
&#10148; <a href="#software"> 1.5 verwendete Programme</a>
&#10148; <a href="#planung"> 1.6 Projektplanung</a>
</ul>
  
<b> 2. Das Projekt</b>
<br/>
<ul>
&#10148; <a href="#arduino"> 2.1 Arduino</a> <br/>
&#10148; <a href="#website"> 2.2 Website, Datenbank, Sever</a> <br/>
&#10148; <a href="#beispiel"> 2.3 Steuerung einer LED</a><br/>
&#10148; <a href="#endprodukt"> 2.4 Das Endprodukt</a>
</ul>
  
<b>Reflexion</b>
<br/>
<ul>
&#10148; <a href="#reflexion"> 3.1 Reflexion des Projekts</a>
</ul>
</body>
<hr>

<h3> <a id="rückblick"> 1.1 Ausgangslage</a></h3>

<body>
Während der letzten Projektphase im 1. Halbjahr arbeitete die Gruppe an einem arduinogesteuerten Gaskocher. Ziel war es einen Gaskocher so steuern zu können, dass eine vorher eingestellte Temperatur in einem Kochtopf erreicht und gehalten werden kann. Für die Eingabe von Werten in °C wurde ein rotary encoder verwendet, sodass man in mehreren Modi die Temperatur gradgenau einstellen kann. Außerdem ist ein Thermometer in dem Topfdeckel integriert, das dauerhauft die Temperatur des Topfinhaltes misst und an den Arduino weitergibt. Die ankommenden Werte werden von dem Arduino verrechnet und über eine logistische Funktion in eine prozentuale Öffnung des Gaskochers umgerechnet. Der Gasfluss zum Gaskocher wird über einen Schrittmotor geregelt. Eine automatische Zündung ist nicht integriert, sodass man diese händisch bei leichter Öffnung des Ventils vornehmen muss. Außerdem speichert der Schrittmotor seine absolute Position leider nicht und diese kann auch nicht angegeben werden, sodass vor der Motor vor jeder Benutzung kalibiert werden muss. 

<details>
 <summary>Bildergalerie</summary>
 
 <h4 align="left"> Bild vom Kochtopf mit integrierten Thermometer</h4>
 <img width="300" alt="Kochtopf" align="left" src="https://user-images.githubusercontent.com/88385654/162032493-22a59161-c6d7-4ef2-a78b-cc23bafafbe6.jpg">

 <h4 align="right"> Bild vom Topf auf dem Gaskocher</h4> 
 <img alt="Gaskocher" align="right" width="300" src="https://user-images.githubusercontent.com/88385654/162033366-8405766e-8f9f-4c3a-960a-1e25023ee066.jpg">
 
 <h4 align="center"> Bild vom Schrittmotor auf der Gasflasche</h4> 
 <img alt="Schrittmotor" align="center" width="300" src="https://user-images.githubusercontent.com/88385654/162031011-f48fb0e4-3051-428b-b170-a0e1aee11551.jpg">

 </details>
</body>


<h3> <a id="zielsetzung"> 1.2 Zielsetzung und Vision </a></h3>

Aufgrund der großen Begeisterung innerhalb der Gruppe für das Projekt, entschied sich die Gruppe auch im 2. Halbjahr am Gaskocher weiterzuarbeiten und diesen noch weiter zu verbessern. Neben der Idee des physical computings, die den Gruppenmitgliedern gut gefallen hat, wurde sich dazu entschieden im zweiten Halbjahr einen größeren Fokus auf die Software zu legen ohne dabei den Bezug zur Praxis zu verlieren, da die Software auf den Gaskocher angewendet werden sollte. Die Idee kam auf den Gaskocher von überall auf der Welt steuern zu können. Diese vielleicht etwas fernliegende Idee hat einen praktischen Hintergrund. Stellen Sie sich vor: Sie kommen von einem langen Tag nach Hause und Ihnen knurrt der Magen. Was gibt es da Schöneres als 20 Minuten vor Ankunft ganz entspannt von unterwegs seinen Herd anzustellen und den am Morgen darauf platzierten Topf mit Wasser zu erhitzen, sodass Sie nach Hause kommen und nur noch die Nudeln in das kochende Wasser geben müssen?
Spinnt man dieses Gedankenexperiment weiter, wäre es natürlich für die tatsächliche Anwendung wichtig einen Not-Aus-Knopf zu haben, eine Webcam, die den Herd überwacht, einen selbstzündenden Gaskocher und eine interaktive Website mit live Wertemonitor. All diese Dinge sind potenzielle Weiterentwicklungsmöglichkeiten, sind aber nicht Ziel dieser Projektarbeit. 
<br/>
Ziel dieses Projekts ist es den im letzten Halbjahr erreichten Zwischenstand so weiterzuführen, dass die Temperatureingabe nicht nur über den rotary encoder, sondern auch über eine eigens dafür gebaute Website, erfolgen kann. Ein weiteres, aber weniger wichtiges Ziel ist die Erstellung eines Wertemonitors, sodass die Website interaktiv ist. Diese Dinge sollten spätestens bis zum 19.4.2022 erledigt sein. Sollte noch mehr Zeit sein, würde sich die Gruppe Zeit für die hardwaretechnische Umsetzung (Verlöten und sorgfältiges Verstauen) und das Einbauen einer elektronsichen Zündung machen. Letzteres bringt jedoch auch ein gewisses Brandrisiko und ist schwer umzusetzen, da es für den Arduino keinen Funkenwerfer oder ähnliche Teile gibt und so evt. mit Kurzschlüssen und Funkenflug gearbeitet werden müsste. 


<h3> <a id="lernen"> 1.3 erforderliche Fähigkeiten und Vorbereitungen</a></h3>

Das Projekt war für die Gruppe großes Neuland. Genau dieser Umstand begeisterte die Gruppe und machte das Projekt interessant und arbeitsaufwendig. Neben der Programmierung des Arduinos, der bereits gesteuert werden konnte, musste sich auch mit einem ESP, einem wlanfähigen Controller, einer Website (HTML, CSS), einer mySql-Datenbank und einen Server auseinandergesetzt werden. Da es sich hierbei um ein relativ komplexes Projekt handelt, müssen alle Schritte funktionieren und zusammenarbeiten oder das Projekt ist nicht erfolgreich. Dies stellt eine neute Situation für die Gruppe dar, da Software wenig handlungsspielraum lässt und das für Hardware typische "Pfuschen" nicht funktioniert. 
<br/>
Konkret mussten folgende Dinge erlernt werden.
<ul>
 <li> Vertiefung der html Kentnisse zum Programmieren der Website</li>
 <li> Einarbeitung in css, damit man Design und Inhalt in Kombination mit einer html-Website trennen kann</li>
 <li> Einarbeitung in php, damit über ein Eingabefeld auf der Website generierte Werte an eine Datenbank gesendet werden können und von dem Arduino ausgelesen werden können</li>
 <li> Einarbeitung in sql zur Erstellung einer mysql-Datenbank</li>
 </ul>
 
 Neben diesen Fähigkeiten, die sich angeeignet werden mussten, mussten im Vorhinein auch ein paar organisatorische Dinge erledigt werden. 
 <ul>
  <li>die erforderliche <a href="#hardware"> Hardware</a> musste angeschafft werden</li>
  <li>da die Website von überall auf der Welt aufgerufen werden soll und nicht nur local gehostet werden soll, wird ein Server als Host für die Website benötigt</li>
 <li>damit die Werte gespeichert werden können wird auch ein Datenbankzugang benötigt</li>
</ul>
<br/>
Bezüglich des Serverplatzes und des Datenbankzugangs wurde der Tipp von Herrn Buhl gegeben sich mit Herrn Andy Adiwidjaja in Verbindung zu setzen, da dieser schon seit längerer Zeit Stormarnschüler bei ihren Informatikprojekten unterstützt. Nach kurzer E-Mailkorrespondenz stellte Herr Adiwidjaja netterweise sowohl Serverplatz mit einer Website (erreichbar unter http://gaskocher.stormarnschueler.de/index.php), als auch einen Datenbankzugang zur Verfügung. Vielen Dank auch an dieser Stelle für die Hilfsbereitschaft, da das Projekt ohne diese Hilfe nicht möglich gewesen wäre. 
<br/>
<br/>
Zur Erlernung der erforderlichen Programmierfertigkeiten und den Programmiersprachen wurde verschiedene Quellen zu Rate gezogen.

<details>
 <summary>Quellenverzeichnis</summary>
 
<b>Erstellung der Website</b>
<ul>
 <li>https://youtu.be/qmTNnZCDJY0https://youtu.be/qmTNnZCDJY0</li>
 <li>https://wiki.selfhtml.org/wiki/HTML/Tutorials</li>
 <li>https://www.html-seminar.de/erste-html-seite.htm</li>
 <li>https://docs.microsoft.com/de-de/learn/modules/build-simple-website/</li>
 <li>http://www.css-lernen.net/css-grundlagen.html</li>
 <li>https://youtu.be/RI2niB0kJFA</li>
 <li>https://www.mediaevent.de/html/input.html</li>
</ul>

<b> Hosten eines Servers</b>
<ul>
 <li>https://www.exone.de/ratgeber/der-server-einfach-erklaert/</li>
 <li>https://hartmut.homelinux.org/Linux/Server-Praxis.html</li>
 </ul>
 
<b> Grundlagen von php</b>
<ul>
 <li>https://www.php.net/manual/de/intro-whatis.php</li>
 <li>https://www.php-einfach.de</li>
 <li>https://wiki.selfhtml.org/wiki/PHP</li>
 <li>https://www.php-kurs.com/erstes-php-programm.htm</li>
</ul>

<b>mysql-Datenbank</b>
<ul>
 <li>https://www.mysql.com/de/</li>
 <li>https://www.datenbanken-verstehen.de/sql-tutorial/</li>
 <li>https://kinsta.com/de/wissensdatenbank/was-ist-mysql/</li>
</ul>

<b>Kommunikation zwischen ESP und Arduino</b>
<ul>
<li>https://forum.arduino.cc/t/esp8266-kommunikation-mit-dem-arduino/571608</li>
<li>https://dronebotworkshop.com/i2c-arduino-arduino/</li>
<li>http://fmh-studios.de/</li>
<li>https://www.arduino.cc/reference/de/language/variables/data-types/array/</li>
</ul>

<b> Kommunikation zwischen Datenbank und ESP</b>
<ul>
<li>https://www.mikrocontroller.net/topic/461310</li>
<li>https://randomnerdtutorials.com/esp32-esp8266-mysql-database-php/</li>
<li>https://steinlaus.de/super-simpler-esp32-nach-mysql-datenlogger/</li>
</ul>

</details>
<h3> <a id="hardware"> 1.4 erforderliche Hardware </a></h3>

Wie bei dem letzten Projekt wird ein <a href="https://www.amazon.de/Arduino-Uno-Rev-3-Mikrocontroller-Board/dp/B008GRTSV6">Arduino Uno R3</a> verwendet. Durch die einfache Bedienung und die diversen Anschluss- und Einsatzmöglichkeiten bietet dieser Microkontroller weiterhin die Grundlage für das Projekt.
<br/>
Als zusätzlicher Microkontroller wird zudem ein NodeMCU Amica Modul V2 benutzt, welches ein ESP8266 ESP-12F als Herzstück trägt. Dabei handelt es sich um einen eigenständigen, mit der Arduino IDE (Entwicklungsumgebung) programmierbaren und durch ein integriertes Modul WLAN-fähigen Microkontroller. Dieser ermöglicht eine Integration in das Netzwerk. Es wurde sich für ein ESP-Modul entschieden, da es mit einem Preis von etwa 8€ sehr preiswert, aber dennoch recht leistungsstark ist, und durch die Eigenständigkeit die Kapazitäten des Arduinos geschont werden. Außerdem handelt es sich um ein gängiges Produkt, weshalb viele Tipps und Fehlerbehebungen im Internet zu finden sind. Wir haben uns aufgrund der hohen Verfügbarkeit für das <a href="https://www.amazon.de/AZDelivery-NodeMCU-Amica-V2-Parent/dp/B07ZZHY25Y"> Modell von „AZDelivery“</a>entschieden.
<br/>
Des Weitern findet erneut das im letzten Halbjahr beschriebene <a href="https://www.amazon.de/ANGEEK-MAX6675-thermocouple-Temperature-arduino/dp/B07X41RG6K/ref=sr_1_2_sspa?__mk_de_DE=ÅMÅŽÕÑ&dchild=1&keywords=max6675&qid=1630502970&sr=8-2-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUE3WkxHNEVaR0RIODUmZW5jcnlwdGVkSWQ9QTAzODIyOTMxVUI3TVFJTVk4VzNZJmVuY3J5cHRlZEFkSWQ9QTA2ODY3NDQxUTUxRVNaSlU2QTdSJndpZGdldE5hbWU9c3BfYXRmJmFjdGlvbj1jbGlja1JlZGlyZWN0JmRvTm90TG9nQ2xpY2s9dHJ1ZQ==">Thermoelement MAX6675</a>, das <a href="https://www.az-delivery.de/products/lcd-display-16x2-mit-blauem-hintergrund-und-i2c-converter-bundle?variant=8192126353504&utm_source=google&utm_medium=cpc&utm_campaign=SSC&utm_term=&gclid=Cj0KCQiA47GNBhDrARIsAKfZ2rAnj0JM_XPeS0Z1rtCZJ93HEfahyNPcxbsyNrfys7dtyzNWtuK33gMaAhgnEALw_wcB"> I2C-LC-Display</a>, <a href="https://www.digikey.de/de/products/detail/adafruit-industries-llc/918/5629415?utm_adgroup=Stepper%20Motors&utm_source=google&utm_medium=cpc&utm_campaign=Shopping_Product_Motors%2C%20Solenoids%2C%20Driver%20Boards%2FModules_Returning&utm_term=&productid=5629415&gclid=Cj0KCQiA47GNBhDrARIsAKfZ2rCAzhqzbNzZGrUsjejqYNCxjTkvTUfVFHDXiyRKR401iU-asx9D3XMaAojuEALw_wcB"> der einfache Schrittmotor inkl. Driverboard</a>, ein variables Netzteil zur Versorgung des Schrittmotors, der modifizierte Topf, der Gaskocher und ein Steckbrett mit Verbindungskabeln Verwendung. 
Nicht mehr verwendet wird der rotary encoder, da die Einstellung der Temperatur über die Website erfolgt, weshalb auch der entsprechende Programmteil entfernt wurde. Deshalb wird ein internetfähiges Endgerät mit einem Browser benötigt, sodass die Website als Steuerzentrale aufgerufen werden kann.

<details>
	<summary>Bildergalerie</summary>
<b>Arduino Uno</b> <img src="https://user-images.githubusercontent.com/88385654/162329333-18241b43-b320-4245-8aca-39932448ed29.jpg">
<br/>
<br/>
<b>NodeMCU</b> <img src="https://user-images.githubusercontent.com/88385654/162329415-50b0d213-f8b5-42c4-8eb5-f158721e6df4.jpg">
<br/>
<br/>
<b>Thermoelement MAX6675</b> <img src="https://user-images.githubusercontent.com/88385654/162329561-a4f05024-65e1-4b3d-93e7-5a1e04912812.jpg">
<br/>
<br/>
<b>LC-Display</b> <img src="https://user-images.githubusercontent.com/88385654/162329629-399847d7-35d3-474c-8287-7dca34646fca.jpg">
<br/>
<br/>
<b>Schrittmotor</b> <img src="https://user-images.githubusercontent.com/88385654/162329800-4a22aaa4-93aa-42f2-a44f-57672c1de31d.jpg">
</details>

<h3> <a id="software"> 1.5 verwendete Programme</a></h3>

<img align="left" width="50" src="https://user-images.githubusercontent.com/88385654/162216442-6b213f8b-9ab6-4c8b-a1ef-9fb5bb28b9e5.png"> 
<b>Visual Studio Code</b><br/>
<a href="https://code.visualstudio.com/">Visual Studio Code</a> ist ein kostenloser Quelltexteditor und ist in der Informatikwelt weit verbreitet. Besonders hilfreich ist die automatische Färbung des Quellcodes während des Schreibens und die automatische sehr übersichtliche Unterteilung in verschiedene Code-Ebenen.
<br/>

<details>
 <summary>Visual Studio Code - Bilder</summary>
<img src="https://user-images.githubusercontent.com/88385654/162217609-d03f41a5-bebb-47a6-bce0-654b1227a87d.png">

</details>

<img align="left" width="50" src="https://user-images.githubusercontent.com/88385654/162218087-85a6771b-7c7f-43be-9c90-dd594e06b684.png">
<b>CyberDuck</b><br/>
<a href="https://cyberduck.io/">CyberDuck</a> ist ein kostenloser FTP-Client, der den Zugriff auf Sever ermöglicht. So wird ermöglicht, dass lokal gespeicherte und erstellte Dokumente auf den Server geladen werden können. 
<br/>

<details>
 <summary>CyberDuck - Bilder</summary>
<img src="https://user-images.githubusercontent.com/88385654/162220411-d2c8a4f6-9dbb-4031-9ddd-2a1b77940fe8.png"><br/>
<img src="https://user-images.githubusercontent.com/88385654/162220425-b921302c-cec1-4d54-8069-3a19cdbee3dc.png">
 
</details>

<img align="left" width="50" src="https://user-images.githubusercontent.com/88385654/162222149-c9971214-9a89-4cd0-8eec-5c60f0df86a6.png">
<b>Fritzing</b><br/>
<a href="https://fritzing.org/">Fritzing</a> ist ein Programm zur Digitalisierung von Schaltplänen. Das Programm wurde sich bereits während der letzten Projektphase gekauft und auch dieses Halbjahr, wenn auch deutlich weniger, benutzt.
<details>
 <summary>Fritzing - Bilder</summary>
<img src="https://user-images.githubusercontent.com/88385654/162222942-a2534ad8-fa7f-46db-8d3e-05522e736223.png">

</details>

<img align="left" width="50" src="https://user-images.githubusercontent.com/88385654/162223091-b2dca110-6384-422f-9708-bbe419281338.png">
<b>Arduino</b><br/>
<a href="https://www.arduino.cc/">Arduino</a> ist eine aus Soft- und Hardware bestehende Plattform. Der eigene Codeeditor wurde auch dieses Projekt wieder viel benutzt und der Arduino stellt das Herzstück des Projekts dar. 
<details>
 <summary>Arduino - Bilder </summary>
<img src="https://user-images.githubusercontent.com/88385654/162223731-b526657f-9fbc-44f2-90b0-40e76a443f68.png">                                       </details>

<h3> <a id="planung"> 1.6 Projektplanung</a>
	
<img alt="Übersichtsskizze" src="https://user-images.githubusercontent.com/88385654/162335480-27590c81-ecdf-4a94-a0be-b45e95934eac.jpg">
	
<hr>

<h3> <a id="arduino"> 2.1 Arduino </a></h3>

Einige Teile vom Code des Projekts des ersten Halbjahrs konnten beibehalten werden. Da die Verarbeitung der eingestellten Temperatur zu einer Ventilstellung des Gaskochers, also der  Temperaturregulierung, zufriedenstellend gelang, wurde dieser Teil des Codes übernommen. Auch die Ansteuerung des Schrittmotors ist identisch. 
Bei dem Code für den Arduino Uno hat sich im Wesentlichen nur die Art der Werteeingabe geändert. Im Vergleich zu dem Projekt des letzten Halbjahrs wird der Wert der eingestellten Temperatur extern erzeugt und dann an den Uno übermittelt. Die ISR-Funktion, welche für die Registrierung der Eingabewerte zuständig war, wurde entfernt. Die Aktualisierung des I2C-LCDs ist im neuen Code keine Aufgabe mehr des Unos. Diese Aufgabe erfüllt jetzt NodeMCU. Deshalb sind die entsprechenden Programmteile vom Code des Arduinos auf den NodeMCU übertragen worden.  
Die größte Veränderung des Codes des Arduinos ist die Anbindung an den I2C-Datenbus. Das bedeutet, dass der Arduino als Teilnehmer an eine und plattform- und geräteübergreifende Kommunikationsmethode angeschlossen wird. Die I2C-Technologie ist zwar sehr universell einsetzbar und in ihren Grundzügen simpel, jedoch macht die hardwarenähe das Programmieren komplex. Die serielle Datenübertragung über zwei Leitungen erfolgt byteweise, weshalb alle Daten zunächst in Bytes zerlegt werden müssen, um diese zu übermitteln. Anschließend benötigt es einen entsprechenden Code, welcher die Bytes decodieren und interpretieren kann. 
Der Datenbus kann von bis zu 128 Teilnehmern (wie Microkontrollern, Sensoren oder Displays, etc.) gleichzeitig verwendet werden. Alle Teilnehmer werden parallel an die SDA-Leitung zur Datenübertragung und an die SCL-Leitung zur Taktgebung geschaltet. Die Kommunikation ist klar geregelt. Es gibt zwei Typen von Teilnehmern: „Master“ und „Slave“.
Der „Master“ bestimmt, wann die Kommunikation mit welchem Teilnehmer stattfindet. Die „Slaves“ können angesprochen werden und auch reagieren, jedoch nicht selbstständig die Kommunikation starten und nur Daten senden, wenn sie dazu aufgefordert werden. Jeder „Slave“ hat eine Adresse, mit welcher er angesteuert wird. Die Kommunikation findet immer zwischen dem „Master“ und den angeschlossenen „Slaves“ statt: Der „Master“ sendet Daten an „Slaves“ oder fordert diese dazu auf Daten zu senden. <br/>
In diesem Projekt arbeitet der Arduino Uno als „Slave“. Wird dieser über die Adresse angesprochen, wird die „empfangfunktion ()“ ausgeführt. 

<details>
	<summary>empfangfunktion()</summary>

```c

void empfangfunktion(){            //entreffende Informationen werden verarbeitet

  byte buf[2];
  for ( int i = 0; i < 2; i++)
  {
    buf[i] = Wire.read();          //eintreffende Bytes werden als Array zwischengespeichert
  }
  eingestellteTemp = setzeZahlZusammen(buf[1] , buf[0]);    //die beiden Bytes werden zu einer Integer-Variablen zusammengesetzt
}

	
```

</details>

Die Bytes, welche über die Leitung gesendet werden, werden in einen Array, also in eine Reihe von Bytes, gespeichert. Anschließend wird die Information zu einer Integer-Variable zusammengesetzt. Dazu dient die Funktion „setzeZahlZusammen()“, welche Integer-Variablen erzeugt, indem die Informationen aus zwei Bytes kombiniert werden. Über diesen Eingang erzeugt der Arduino die Variable „eingestellteTemp“ welche anschließend weiterverarbeitet wird.
	
<details>
	<summary>setzeZahlZusammen();</summary>
	
```c
	
int setzeZahlZusammen(unsigned int high, unsigned int low) {        //Funktion, um aus zwei Bytes eine Integer-Variable zu kombinieren 
 
  int kombiniert;
  kombiniert = high;
  kombiniert = kombiniert * 256;
  kombiniert |= low;
  return kombiniert;
}

```

</details>

Des Weiteren wird die „antwortfunktion()“ ausgelöst, wenn vom „Master“ Daten gefordert werden. Hierbei werden zunächst alle wichtigen Variablen der Kennwerte des Gaskocherzustands in Bytes zerlegt und anschließend byteweise an den „Master“ übertragen. Zu beachten ist, dass Float-Variablen (Kommazahlen mit 2 Nachkommastellen) zunächst mit 100 multipliziert und anschließend in eine Integer-Variable umgewandelt werden. Nach der Übertragung wird der Prozess rückgängig gemacht, wobei keine Informationen verloren gehen. Da Float-Variablen aus 4 Bytes bestehen, könnte es ansonsten zu Schwierigkeiten durch eine Veränderung des vorher gewählten 2-Byte-Leserasters kommen. 
Als Folge der Kommunikation sind alle Kennzahlen auf dem „Master“ und auf dem „Slave“ synchron.

<details>
	<summary>antwortfunktion()</summary>
	
```c
	
void antwortfunktion(){            //eintreffende Aufforderung zur Datenübertragung wird verarbeitet
  byte buffer[6];
 
  buffer[0] = lowByte(gemesseneTemperaturInt);        //Variablen werden in Bytes zerlegt und in einem Array zwischengespeichert
  buffer[1] = highByte(gemesseneTemperaturInt);         
  buffer[2] = lowByte(eingestellteTemp);
  buffer[3] = highByte(eingestellteTemp);
  buffer[4] = lowByte(pVentilInt);
  buffer[5] = highByte(pVentilInt);
   
  Wire.write( buffer, 6);                             //Daten des Arrays werden byteweise übertragen
}

```
	
</details>

Ein weiteres Gerät, welches an den I2C-Datenbus angeschlossen ist, ist das I2C-LCD. Durch eine eigene „Slave-Adresse“ kann das Display angesteuert und die Anzeige aktualisiert werden. Da der Arduino Uno ebenfalls als „Slave“ arbeitet, können beide Teilnehmer nicht kommunizieren. Deshalb wird das LCD bei dem fortgeführten Projekt nicht vom Arduino Uno, sondern von NodeMCU angesteuert. Unter anderem aus diesem Grund muss zunächst die gemesse Temperatur vom Arduino auf NodeMCU übertragen werden, um anschließend die Werte auf dem Display darzustellen. Die Ansteuerung des LC-Displays wird durch eine passende Bibliothek erleichtert, wobei die Codierung, Übertragung und Decodierung von der Bibliothek übernommen wird.
<br/>
Der NodeMCU Code ist weitestgehend neu. Zunächst muss die Arduino IDE auf dem Microcontroller und die Boardkonfigurationen über den Boardverwalter des Arduino-Programms installiert werden. Anschließend kann mit der Entwicklungsoberfläche von Arduino programmiert werden.
NodeMCU hat die Aufgabe sowohl mit der Datenbank, als auch mit dem Arduino und dem LC-Display zu kommunizieren. Das Board führt alle Netzwerkfunktionen aus. Um Zugang zu dem Netzwerk zu haben, wird der integrierte WLAN-Chip verwendet. Dabei werden drei verschiedene „libraries“ verwendet, welche das Programmieren vereinfachen. Alle für das Projekt verwendete Libraries können „verwendete libraries für das Projekt“ gefunden werden.
Die Verbindung zu allen gängigen WLAN-Typen erfolgt durch den Befehl „WiFi.begin(*ssid*, *passwort);“. Anschließend wird sichergestellt, dass die Verbindung zum Netzwerk erfolgreich war. Der entscheidende Schritt ist die Verbindung zu der Datenbank über einen http-request. NodeMCU sorgt durch die URL http://gaskocher.schormarnschueler.de/GetData.php dafür, dass das php-Dokument „GetData.php“ auf dem Server ausgeführt wird und die verarbeitete Information als „Payload“, also als Rückgabe, empfangen werden kann. So wird der gewünschte Wert, welcher in der Datenbank gespeichert ist, durch das php-Dokument ausgelesen und an das ESP8266 übergeben. Nachdem der Payload, also die eingestellte Temperatur als Variable im NodeMCU Code gespeichert wurde, wird die Verbindung zum Server geschlossen. Je öfter diese Verbindung stattfindet, desto schneller ist die Übertragung der Daten von der Website bis zum ESP. Ausgiebig experimentiert wurde mit dem umgekehrten Prozess: dem Upload von Daten des NodeMCUs in die Datenbank. Hier ergaben sich jedoch Stabilitätsprobleme, weshalb angesichts der kurzen Projektzeit von dieser Funktion abgesehen wurde. Grundsätzlich ist dies jedoch möglich. 
Die Codeabschnitte für die I2C-Kommunikation des „Masters“ (ESP) funktionieren ähnlich zu denen des „Arduino-Slaves“. Der große Unterschied besteht in der Fähigkeit, eigenständig die Kommunikation zu starten. Wird „sendeWerte();“ ausgeführt, wird die eingestellte Temperatur, welche vorher aus der Datenbank gezogen wurde, zerlegt und versendet. Dazu muss auch die Slave-Adresse angegeben werden, sodass die Daten am richtigen Teilnehmer ankommen.

<details>
	<summary>sendeWert();</summary>

```c
	
void sendeWerte(){                            //eingestellteTemp wird via I2C an den Arduino gesendet
  byte buffer[2];
 
  buffer[0] = lowByte(eingestellteTemp);      //Integer-Variable wird in 2 Bytes getrennt 
  buffer[1] = highByte(eingestellteTemp);
  
  Wire.beginTransmission(10);                 //Verbindung zum Arduino (Slave-Adresse: 10)
  Wire.write( buffer, 2);                     //Übertragung der Bytes
  Wire.endTransmission();                     //Ende der Übertragung
}	
	
```

</details>
	
Bei „rufeWertAb();“ werden die Daten angefragt und empfangen, welche durch die „antwortfunktion()“ des „Slaves“ übermittelt wurden. Hier ist es die Aufgabe des „Masters“ die Daten zu decodieren, um diese anschließend weiterzuverarbeiten.

<details>
	<summary>rufeWertAb();</summary>

```c
	
void rufeWertAb() {                           //Werte werden vom Arduino abgefragt
 
  byte buf[5];
 
  int n = Wire.requestFrom(10, 6);            //es werden 6 Bytes vom Arduino (Slave-Adresse 10) abgefragt
  for ( int i = 0; i < n; i++)
  {
    buf[i] = Wire.read();                     //empfangene Bytes werden als Array zwischengespeichert
  }
  gemesseneTempInt = setzeZahlZusammen(buf[1] , buf[0]);    //Jeweil ein Paar (immer 2) von den Bytes werden zu Integer-Variablen zusammengesetzt
  eingestellteTemp = setzeZahlZusammen(buf[3] , buf[2]);
  pVentilInt = setzeZahlZusammen(buf[5] , buf[4]);
  tatTemp = (float)gemesseneTempInt /100 ;                  //Integers werden in Floats umgewandelt
  pVentil = (float)pVentilInt /100 ;
}	
	
```
	
</details>
	
<h3> <a id="website"> 2.2 Website, Dantenbank, Server </a></h3>

Zuerst wurde eine recht simple Website mit Hilfe von html und ein wenig css erstellt. Dafür wurde bei visual studio code eine index.html - Datei und ein stylesheet.css angelegt. Die Website ist absichtlich sehr simpel gehalten und soll vor allen Dingen funktional sein. Die beiden Bilder auf der rechten Seite sind eine kleine Spielerei und sollen an das Layout der Stundenprotokolle erinnern. Da die Website als Steuerzentrale funktionieren soll, befindet sich dort ein html-input Feld. Über das Feld können verschiedene Dinge wie Typ, Maximalwert, Minimalwert und Ausgangswert eingestellt werden. Um ein einheitliches und ansprechendes Design zu erreichen wurden mit Hilfe von dem stylesheet Ramen und andere Verschönerung programmiert. Diese Schritte funktionierten nach einer Einarbeitungsphase relativ problemlos und schnell. 

<details>
 <summary>index.html</summary>
 
<!DOCTYPE html>

<html>

    <head>
        <link rel="stylesheet" href="stylesheet.css">
        <title>Arduinogesteuerter Gaskocher</title>
        <meta charset="UTF-8">
    </head>

    <body>
       <h1 class="überschrift">Arduinogesteuerter Gaskocher</h1>
       <h2 class="überschrift2"> Steuerzentrale</h2>

       
        <div id="square"></div>

        <img id="bild1" src="/IMG_1042.jpg">
        <img id="bild2" src="/IMG_1966.jpg">

        <p class="text"> 
                Geben Sie hier die gewünschte Temperatur in °C ein:
        </p>


        <form action="formular.php" method="post">
            <input class="eingabefeld" type="number" name="temperatureingabe" step="1" max="300" min="0">
            <input type="submit">
        </form>

        <?php require("config.php") ?>


        <?php
        require("tabelle.php")
        ?>
    </body>
</html>


</details>
 
 <details>
 <summary>stylesheet.css</summary>

```
.überschrift {
    font-size: 48pt;
    color:black;
    text-align: center;
}

.überschrift2 {
font-size: 30pt;
color: black;
margin-left: 10px;
margin-right: 10px;
}

.square {
width: 300pt;
height: 300pt;
background: white;
border: 10pt solid;
border-color: black;
}

#bild1 {
width: 150px;
height: 200px;
float: right;
border: 2px solid black;
margin-left: 10px;
margin-top: -100px;
margin-right: 10px;
}

#bild2 {
width: 150px;
height: 200px;
float: right;
border: 2px solid black;
margin-top: -100px;
}

.text {
  color: black;
  font-size: 23px;
  font-family:'Times New Roman', Times, serif;
  margin-left: 2px;
}

.eingabefeld {
width: 100px;
border:  2px solid black;
text-align: center;
background-color: rgb(185, 185, 185);
margin-left: 10px;
}

table, th, td, caption {
  border: thin solid black;
  margin-left: 10px;
  margin-right: 10px;
  margin-top: 50px;
}
	 
```
 
</details>
 
<details>
 <summary>Screenshot der Website</summary>
 <img src="https://user-images.githubusercontent.com/88385654/162228599-0879e232-9569-42cc-8d70-3606e7b99b68.png">
</details>

Damit die Website nicht nur im lokalen Netwerk, sondern im Internet zu sehen sein sollte, wurde mit den Zugangsdaten von Herrn Adiwidjaja und Cyberduck eine Verbindung zum Server aufgebaut und die entsprechenden Dokumente konnten platziert werden, sodass die Website abrufbar war. 
Allerdings funktionierte das input-Feld noch nicht, dafür musste erst das passende php Skript geschrieben werden und eine Datenbank erstellt werden. Dei Erstellung der Datenbank erfolgte nach erfolgreicher Anmeldung bei https://phpmyadmin.atw.io/, konnte eine Datenbank erstellt werden. Um die dort erstellte Tabelle mit Werten von der Website zu füllen, wurde das Dokument formular.php erstellt. Dieser Code bekommt die Daten aus dem Eingabefeld übermittelt und definiert sie als Variable. Anschließend wird das Dokument config.php über eine require Funktion eingebunden und so der Datenbankzugang hergestellt. Anschließend werden die Daten über die prepare und execute Funktion in die passende Tabelle und Spalte eingefügt.

<details>
 <summary>config.php</summary>

 ```
 <?php

$pdo = new PDO('mysql:host=localhost;dbname=sschuelersql4', 'sschuelersql4', 'lycquzesjb');

?>
```
</details>
 
<details>
 <summary>formular.php</summary>
 
```
 <?php
 $eintemperatur = $_POST["temperatureingabe"]; //Werte des Eingabefelds auf der Website werden als Variable definiert
echo $eintemperatur; //Werte werden zur Kontrolle ausgegeben

require("config.php"); //Zugangsdaten der Datenbank

$statement = $pdo ->prepare("INSERT INTO gaskocher(eintemperatur) values (?)"); //über die prepare und execute Funktion werden die Daten in die passende Tabelle (gaskocher) und Spalte (eintemperatur) eingefügt
$statement->execute(array($eintemperatur));

header("location:index.php")

?>
 
```
 
</details>

<details>
 <summary>Screenshot der Datenbank</summary>
<img src="https://user-images.githubusercontent.com/88385654/162234026-015ea17f-364c-419d-9ecd-68ea77ffab41.png">
 
</details>

Damit die Werte auch von dem Arduino als Temperatureingabe genutzt werden können, greift der ESP auf die Datenbank zu und kann Daten von dort abgreifen. Dazu ist der ESP mit dem Internet verbunden und führt mehrere auf dem Server gespeicherten php Skripte aus. Das Dokument database.php sorgt für den Verbindungsaufbau zwischen ESP und Datenbank. Sobald der ESP mit der Datenbank verbunden ist, wird der Code 200 (erfolgreiches verbinden) im seriellen Monitor ausgegeben. Nachdem die Verbindung hergestellt ist wird der Wert mit der höchsten id (WHERE ID(max) ausgegeben und ebenfalls im seriellen Monitor angezeigt. Nachdem der ESP die Daten empfangen hat, können diese an den Arduino transportiert werden und die Temperatur wird reguliert. 
Auch wenn die Theorie hinter diesem Schritt ziemlich simpel ist, gestaltete sich die Umsetzung sehr schwierig. Dies liegt daran, dass zwei Programmiersprachen und Artn miteinander verbunden werden mussten. Da dieser Schritt lange nicht gelang, wurde ein Video mit einem ähnlichen Zweck als Beispiel durchgearbeitet und nachgebaut. Es stellte sich jedoch heraus, dass die Umsetzung nicht so einfach war wie gedacht und dass selbst die aus dem Internet kopierten Beispiele nicht funktionierten. Daher vergingen mehrere Wochen des Debuggings, in denen die einzelnen Codes verändert wurden. Kurz vor den Ferien gelang der Gruppe jedoch ein Durchbruch und die LED ließ sich über eine dafür vorgesehene Website steuern. Weitere Informationen zu dem Beispiel gibt es in dem <a href="https://www.youtube.com/watch?v=J9ziYzmiW9I"> Originalvideo</a>, unserem <a href="https://www.youtube.com/watch?v=xTHpKBRuh9c"> Versuchsvideo </a> und dem <a href="#beispiel">Unterpunkt 2.3 Beispiel</a>.

<details>
 <summary>database.php</summary>
 
```
<?php
	class Database {
		private static $dbName = 'sschuelersql4' ;
		private static $dbHost = 'localhost' ;
		private static $dbUsername = 'sschuelersql4';
		private static $dbUserPassword = 'lycquzesjb';
		 
		private static $cont  = null;
		 
		public function __construct() {
			die('Init function is not allowed');
		}
		 
		public static function connect() {
		  // One connection through whole application
		  if ( null == self::$cont ) {     
        try {
          self::$cont =  new PDO( "mysql:host=".self::$dbHost.";"."dbname=".self::$dbName, self::$dbUsername, self::$dbUserPassword); 
        }
        catch(PDOException $e) {
          die($e->getMessage()); 
        }
		  }
		  return self::$cont;
		}
		 
		public static function disconnect() {
			self::$cont = null;
		}
	}
?>
 
```
</details>

<details>
 <summary>GetData.php</summary>
 
```
 <?php

  $dbName = 'sschuelersql4';
  $dbHost = 'localhost';
  $dbUsername = 'sschuelersql4';
  $dbUserPassword = 'lycquzesjb';
 $pdo = new PDO( "mysql:host=$dbHost;dbname=$dbName", $dbUsername, $dbUserPassword); //Verbindung mit der Datenbank

  $sql = 'SELECT * FROM gaskocher  WHERE   ID = (SELECT max(ID) From gaskocher)'; //Wert mit der höchsten ID wird aus der Tabelle Gaskocher ausgelesen
  foreach ($pdo->query($sql) as $row) {
    echo $row['eintemperatur'];
  }
?>
 ```
</details>

Grundsätzlich wäre es sinnvoll, wenn der Arduino über den Eintrag in die Datenbank Werte wie momentane Öffnung des Ventils in Prozent und die gemessene Temperatur ausgeben würde. So wäre die Website interaktiv und ein großer Schritt hin zur Praktikabilität wäre gemacht. Um einen Wert aus der Datenbank auf der Website anzeigen zu lassen, wurde das Dokument tabelle.php erstellt. Dabei wird mit Hilfe der select Funktion ein Wert aus einer Tabelle ausgewählt und auf der Website dargestellt. Auch hier wird der Wert mit der höchsten id ausgewählt, sodass immer nur der neuste Wert angezeigt wird und es nicht zu Verwirrungen kommt. All das funktioniert, sodass unter der Eingabe immer der Wert mit der höchsten id angezeigt wird.
Leider funktioniert die Datenübertragung von ESP auf die Datenbank nicht, weil der Upload von Daten durch den ESP kurzzeitig zu einem so hohen Strombedarf kommt, dass der ESP sich selber ausschaltet und abstürzt. Daher können keine gemessenen Werte vom Arduino in die Datenbank eingetragen werden, sodass als prove of concept der Wert der höchsten id der eingestellten Temperatur ausgegeben wird. So hat man eine Kontrolle, ob der eingestellte Wert in die Datenbank übernommen wurde. Es ist schade, dass der Upload nicht funktioniert, da ein Verbraucher so keine Rückmeldung hat, ob der Gaskocher eingeschaltet ist und wie heiß das Wasser ist. Ein aktiver Wertemonitor wäre ohne diese hardwaretechnischen, bauartbedingten Fehler beim ESP gut möglich und die softwaretechnischen Vorraussetzungn sind durch tabelle.php und connect.php gegeben. Damit sich dieses Problem in der Praxis nicht ganz so stark bemerkbar macht, wurde wie im letzten Projekt ein LC-Display verwendet, auf dem man alle relavanten Informationen ablesen kann. 

<details>
	<summary>tabelle.php</summary>	

```
<?php

$sql = "SELECT * FROM gaskocher WHERE   ID = (SELECT max(ID) From gaskocher)";
?>


<?php
foreach($pdo->query($sql)as $row){
 $temperatur = $row['eintemperatur'];
 echo $temperatur; 
}
?>
	
```

</details>

<details>
	<summary>connect.php</summary>
	
```
<html>
<body>

<?php

$dbname = 'sschuelersql4';
$dbuser = 'sschuelersql4';  
$dbpass = 'lycquzesjb'; 
$dbhost = 'localhost'; 

$connect = @mysqli_connect($dbhost,$dbuser,$dbpass,$dbname);

if(!$connect){
	echo "Error: " . mysqli_connect_error();
	exit();
}

echo "Connection Success!<br><br>";

$temperature = $_GET["temperature"];
$humidity = $_GET["humidity"]; 


$query = "INSERT INTO wertemonitor (temperature, humidity) VALUES ('$temperature', '$humidity')";
$result = mysqli_query($connect,$query);

echo "Insertion Success!<br>";

?>
</body>
</html>

```
	
</details>

<details>
	<summary>Screenshot von der Website</summary>
<img src="https://user-images.githubusercontent.com/88385654/162257440-10de68cd-84b2-40a1-b8e4-4e1f06b7171f.png">
	
</details>

<h3> <a id="beispiel"> 2.3 Steuerung einer LED</a></h3>

Da die Kommunikation zwischen dem ESP und der Datenbank lange nicht funktionierte und sehr problematisch war, entschied sich die Gruppe anhand eines YouTube Tutorials die Schritte nachzuvollziehen. Dafür wurde sich das <a href="https://www.youtube.com/watch?v=J9ziYzmiW9I"> Tutorial</a> von <a href="https://www.youtube.com/channel/UCk8rZ8lhAH4H-75tQ7Ljc1A"> Uteh Str </a> genau angeschaut und nachgebaut. Interessanterweise funktionierten die übernommenen Codes jedoch nicht auf anhieb. Ein Problem war, dass auf dem Server das Leitdokument index.php und nicht main.php heißen muss. Außerdem sollte der ESP über ein php-Dokument mit if-Schleife die Daten aus der Datenbank nehmen. Da die Schleife allerdings fehlerhaft war, wurde sie nicht außgeführt. Der Fehler, der am längsten zum Beheben gebraucht hat war ein Versionsunterschied in der Adresse der Website. Statt https ist die verwendete Website nämlich in http geschrieben, sodass ein simpler Schreibfehler lange Zeit den Erfolg des Codes verhindert hat. 
Nachdem all diese Unwegbarkeiten jedoch behoben waren, funktionierte der Code und die Steuerung einer LED über eine Website war möglich. Dies sieht man auch in folgendem <a href="https://www.youtube.com/watch?v=ujq6IXgyYq8&t=16s"> Video</a>. Auch wenn der Erfolg des Versuchs lange auf sich warten ließ, war das Projekt dennoch erfolgreich, da das Script in ähnlicher Form für den Gaskocher verwendet werden konnte und die Gruppe viel aus dem Experiment gelernt hat. 

<details>
	<summary>index.php</summary>
	
```
<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta charset="utf-8">
    <style>
      html {
          font-family: Arial;
          display: inline-block;
          margin: 0px auto;
          text-align: center;
      }
      
      h1 { font-size: 2.0rem; color:#2980b9;}
      h2 { font-size: 1.25rem; color:#2980b9;}
      
      .buttonON {
        display: inline-block;
        padding: 15px 25px;
        font-size: 24px;
        font-weight: bold;
        cursor: pointer;
        text-align: center;
        text-decoration: none;
        outline: none;
        color: #fff;
        background-color: #4CAF50;
        border: none;
        border-radius: 15px;
        box-shadow: 0 5px #999;
      }
      .buttonON:hover {background-color: #3e8e41}
      .buttonON:active {
        background-color: #3e8e41;
        box-shadow: 0 1px #666;
        transform: translateY(4px);
      }
        
      .buttonOFF {
        display: inline-block;
        padding: 15px 25px;
        font-size: 24px;
        font-weight: bold;
        cursor: pointer;
        text-align: center;
        text-decoration: none;
        outline: none;
        color: #fff;
        background-color: #e74c3c;
        border: none;
        border-radius: 15px;
        box-shadow: 0 5px #999;
      }
      .buttonOFF:hover {background-color: #c0392b}
      .buttonOFF:active {
        background-color: #c0392b;
        box-shadow: 0 1px #666;
        transform: translateY(4px);
      }
    </style>
  </head>
  <body>
    <h1>Controlling LED on NodeMCU ESP12E ESP8266 with MySQL Database</h1>
    
    <form action="updateDBLED.php" method="post" id="LED_ON" onsubmit="myFunction()">
      <input type="hidden" name="Stat" value="1"/>    
    </form>
    
    <form action="updateDBLED.php" method="post" id="LED_OFF">
      <input type="hidden" name="Stat" value="0"/>
    </form>
    
    <button class="buttonON" name= "subject" type="submit" form="LED_ON" value="SubmitLEDON" >LED ON</button>
    <button class="buttonOFF" name= "subject" type="submit" form="LED_OFF" value="SubmitLEDOFF">LED OFF</button>  
  </body>
</html>
```
</details>

<details>
	<summary>updateDBLED.php</summary>
	
```
	
<?php     
  require 'database.php';
  
  if (!empty($_POST)) {
    $Stat = $_POST['Stat'];
      
    // insert data
    $pdo = Database::connect();
    $pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    $sql = "UPDATE statusled SET Stat = ? WHERE ID = 0";
    $q = $pdo->prepare($sql);
    $q->execute(array($Stat));
    Database::disconnect();
    header("Location: index.php");
  }
?>
	
```
	
</details>

<details>
	<summary>GetData.php</summary>

```
	
<?php

  $dbName = 'sschuelersql4';
  $dbHost = 'localhost';
  $dbUsername = 'sschuelersql4';
  $dbUserPassword = 'lycquzesjb';
 $pdo = new PDO( "mysql:host=$dbHost;dbname=$dbName", $dbUsername, $dbUserPassword); //Verbindung mit der Datenbank

  $sql = 'SELECT FROM statusled  WHERE   ID = (0); //Wert mit der ID=0 wird aus der Datenbank ausgelesen und als Status 0,1 weitergegeben
  foreach ($pdo->query($sql) as $row) {
    echo $row['eintemperatur'];
  }
?>
	
```
	
</details>
	
<details>
	<summary>Screenshot der Website</summary>
<img src="https://user-images.githubusercontent.com/88385654/156559570-7df79162-2da5-44c5-bc18-5d1365f89a2d.png">
</details>

<details>
	<summary>Video der Steuerung der LED - novum hotplate</summary>
	<div align="center">
  			<a href="https://www.youtube.com/watch?v=xTHpKBRuh9c"><img src="https://user-images.githubusercontent.com/88385654/161727389-0f1cf787-5f1d-463c-ac45-d298d5613ecc.png" alt="Fernsteuerung LED"></a>	
	</div>
</details>

<h3> <a id="endprodukt"> 2.4 Das Endprodukt </a></h3>

Nach langer Einarbeitungsphase und vielen Stunden des Debuggings steht nun ein funktionstüchtiges Endprodukt. Es gibt eine öffentlich zugängliche Website, auf der man Werte über ein input-Feld eintragen kann. Diese Werte werden an eine dafür eingerichtete Datenbank gesendet und dort in einer Tabelle gespeichert. Auch ohne Kontakt zu einem Computer kann ein ESP auf die Datenbank zugreifen und die Werte auslesen. Demensprechend ist unser Endprodukt nur strom- und wlan- allerdings nicht computerabhängig. Der ESP gibt die Werte an den Arduino weiter, der aufgrund von eingestellter und gemessener Temperatur eine Differenz bildet und über eine Funktion diese Differenz in eine prozentuale Öffnung des Gaskochers umrechnet. Die Öffnung des Ventils geschieht über einen Schrittmotor. Die eingestellte und gemessene Temperatur wird über ein LC-Display ausgegeben. Da die Verrechnung von eingestellter und gemessener Temperatur immer wieder passiert und die Funktion sehr präzise ist, gelingt es sich einem Temperaturwert zu nähern und diesen weitestgehend zu halten.
Die softwaretechnischen Voraussetzungen sind erfüllt, sodass der Arduino theoretisch die gemessene Temperatur und die prozentuale Öffnung des Ventils an die Website schicken könnte. Leider klappt dies aufgrund der Instabilität des ESPs nicht.

<details>
	<summary>Video zum Endprodukt</summary>
<a href="https://www.youtube.com/watch?v=ZekT9gXA-Eo"><img src="https://user-images.githubusercontent.com/88385654/162266251-90478a47-8a7e-4983-9f2e-75f7b61711ad.png"></a>
</details>

<details>
	<summary>Übersichtsskizze</summary>
	
<img src="https://user-images.githubusercontent.com/88385654/162335381-01b1191d-fb1b-463f-a06a-f6e42d10cb77.jpg">

</details>

<details>
	<summary>index.php</summary>

```
<!DOCTYPE html>

<html>

    <head>
        <link rel="stylesheet" href="stylesheet.css">
        <title>Arduinogesteuerter Gaskocher</title>
        <meta charset="UTF-8">
    </head>

    <body>
       <h1 class="überschrift">Arduinogesteuerter Gaskocher</h1>
       <h2 class="überschrift2"> Steuerzentrale</h2>

       
        <div id="square"></div>

        <img id="bild1" src="/IMG_1042.jpg">
        <img id="bild2" src="/IMG_1966.jpg">

        <p class="text"> 
                Geben Sie hier die gewünschte Temperatur in °C ein:
        </p>


        <form action="formular.php" method="post">
            <input class="eingabefeld" type="number" name="temperatureingabe" step="1" max="300" min="0">
            <input type="submit">
        </form>

        <?php require("config.php") ?>


        <?php
        require("tabelle.php")
        ?>
    </body>
</html>
```
</details>

<details>
	<summary>stylesheet.css</summary>

```
.überschrift {
    font-size: 48pt;
    color:black;
    text-align: center;
}

.überschrift2 {
font-size: 30pt;
color: black;
margin-left: 10px;
margin-right: 10px;
}

.square {
width: 300pt;
height: 300pt;
background: white;
border: 10pt solid;
border-color: black;
}

#bild1 {
width: 150px;
height: 200px;
float: right;
border: 2px solid black;
margin-left: 10px;
margin-top: -100px;
margin-right: 10px;
}

#bild2 {
width: 150px;
height: 200px;
float: right;
border: 2px solid black;
margin-top: -100px;
}

.text {
  color: black;
  font-size: 23px;
  font-family:'Times New Roman', Times, serif;
  margin-left: 2px;
}

.eingabefeld {
width: 100px;
border:  2px solid black;
text-align: center;
background-color: rgb(185, 185, 185);
margin-left: 10px;
}

table, th, td, caption {
  border: thin solid black;
  margin-left: 10px;
  margin-right: 10px;
  margin-top: 50px;
}
	
```
	
</details>

<details>
	<summary>database.php</summary>

```
<?php
	class Database {
		private static $dbName = 'sschuelersql4' ;
		private static $dbHost = 'localhost' ;
		private static $dbUsername = 'sschuelersql4';
		private static $dbUserPassword = 'lycquzesjb';
		 
		private static $cont  = null;
		 
		public function __construct() {
			die('Init function is not allowed');
		}
		 
		public static function connect() {
		  // One connection through whole application
		  if ( null == self::$cont ) {     
        try {
          self::$cont =  new PDO( "mysql:host=".self::$dbHost.";"."dbname=".self::$dbName, self::$dbUsername, self::$dbUserPassword); 
        }
        catch(PDOException $e) {
          die($e->getMessage()); 
        }
		  }
		  return self::$cont;
		}
		 
		public static function disconnect() {
			self::$cont = null;
		}
	}
?>
```
	
</details>

<details>
	<summary>formular.php</summary>
	
```
<?php
 $eintemperatur = $_POST["temperatureingabe"]; //Werte des Eingabefelds auf der Website werden als Variable definiert
echo $eintemperatur; //Werte werden zur Kontrolle ausgegeben

require("config.php"); //Zugangsdaten der Datenbank

$statement = $pdo ->prepare("INSERT INTO gaskocher(eintemperatur) values (?)"); //über die prepare und execute Funktion werden die Daten in die passende Tabelle (gaskocher) und Spalte (eintemperatur) eingefügt
$statement->execute(array($eintemperatur));

header("location:index.php")

?>
	
```
	
</details>

<details>
	<summary>GetData.php</summary>
	
```
<?php

  $dbName = 'sschuelersql4';
  $dbHost = 'localhost';
  $dbUsername = 'sschuelersql4';
  $dbUserPassword = 'lycquzesjb';
 $pdo = new PDO( "mysql:host=$dbHost;dbname=$dbName", $dbUsername, $dbUserPassword); //Verbindung mit der Datenbank

  $sql = 'SELECT * FROM gaskocher  WHERE   ID = (SELECT max(ID) From gaskocher)'; //Wert mit der höchsten ID wird aus der Tabelle Gaskocher ausgelesen
  foreach ($pdo->query($sql) as $row) {
    echo $row['eintemperatur'];
  }
?>
	
```
	
</details>

<details>
	<summary>config.php</summary>
	
```
	
<?php

$pdo = new PDO('mysql:host=localhost;dbname=sschuelersql4', 'sschuelersql4', 'lycquzesjb');

?>
	
```
	
</details>

<details>
	<summary>tabelle.php</summary>
	
```
<?php

$sql = "SELECT * FROM gaskocher WHERE   ID = (SELECT max(ID) From gaskocher)";
?>


<?php
foreach($pdo->query($sql)as $row){
 $temperatur = $row['eintemperatur'];
 echo $temperatur; 
}
?>
	
```
	
</details>

<details>
	<summary>connect.php</summary>
	
```
<html>
<body>

<?php

$dbname = 'sschuelersql4';
$dbuser = 'sschuelersql4';  
$dbpass = 'lycquzesjb'; 
$dbhost = 'localhost'; 

$connect = @mysqli_connect($dbhost,$dbuser,$dbpass,$dbname);

if(!$connect){
	echo "Error: " . mysqli_connect_error();
	exit();
}

echo "Connection Success!<br><br>";

$temperature = $_GET["temperature"];
$humidity = $_GET["humidity"]; 


$query = "INSERT INTO wertemonitor (temperature, humidity) VALUES ('$temperature', '$humidity')";
$result = mysqli_query($connect,$query);

echo "Insertion Success!<br>";

?>
</body>
</html>
```
	
</details>

<details>
	<summary>ESP-Code</summary>
	
```c

//Dieser Code ist für das ESP8266 Modul, welches als Master die I2C-Kommunikation steuert und die Daten aus der Datenbank abfragt:

//Einbindung der benötigten Libaries: Zusammenfassung aller verwendeter Libaries, welche nicht direkt über den Bibliothek-Verwalter vorinstalliert sind, kannn auf der Projektseite gefunden werden.
#include <ESP8266WiFi.h>            
#include <WiFiClient.h>
#include <ESP8266HTTPClient.h>
#include <LiquidCrystal_I2C.h>   
#include <Wire.h>

LiquidCrystal_I2C lcd(0x3F, 16, 2); //LCD mit der SLave-Adresse wird initialisiert
 

int eingestellteTemp;
int gemesseneTempInt;
float tatTemp;
int pVentilInt;
float pVentil;



const char* ssid = "**********";        //Name des WLAN-Netzes
const char* password = "**********";    //Passwort des WLAN-Netzes


void setup() {
 
  Serial.begin(9600);    //der serielle Monitor wird initialisiert
  Wire.begin();          //der I2C-Datenbus wird initalisiert
  
  delay(500);
  
  lcd.begin();           //das LC-Display wird gestartet  
  lcd.backlight();       //die Hintergrundbeleuchtung des LCDs wird aktiviert 
  

  WiFi.mode(WIFI_STA);
  WiFi.begin(ssid, password);                 //Verbindung zum WLAN wird aufgebaut 
  Serial.println("");
    
  Serial.print("Connecting");                 //es wird gewartet,solange noch keine Verbindung besteht
  while (WiFi.status() != WL_CONNECTED) {
    Serial.print(".");
    delay(500);
  }

  Serial.println("");
  Serial.print("Successfully connected to : ");
  Serial.println(ssid);
  Serial.print("IP address: ");
  Serial.println(WiFi.localIP());
  Serial.println();

 
}

void loop() {
  
  HTTPClient http;                        //ein http-Client wird delariert

  String LinkGet, getData;
  int id = 0; 
  
  LinkGet = "http://gaskocher.stormarnschueler.de/GetData.php";   //diese URL wird ausgeführt
  getData = "ID=" + String(id);
  
  Serial.println("----------------Connect to Server-----------------");
  Serial.println("Get LED Status from Database");
  Serial.print("Request Link : ");
  Serial.println(LinkGet);
  http.begin(LinkGet);                                                    //Verbindung zu dem Server mit der URL wird aufgebaut
  http.addHeader("Content-Type", "application/x-www-form-urlencoded");    //Definiert die Art des Inhaltes
  int httpCodeGet = http.POST(getData);                                   //Anfrage wird gesendet
  
  String payloadGet = http.getString();                                   //Abfrage des Payloads vom Server
  Serial.print("Response Code : "); 
  Serial.println(httpCodeGet);                                            //Antwort-Code vom Server wird ausgegeben. Bei Erfolg lautet der http-Responsecode "200"
  Serial.print("Returned data from Server : ");
  Serial.println(payloadGet);                                             

  eingestellteTemp = payloadGet.toInt();                                  //Inhalt des Payloads wird als Varaible gespeichert
   Serial.println(eingestellteTemp);
  
  Serial.println("----------------Closing Connection----------------");
  http.end();                                                             //Verbindung wird geschlossen
  Serial.println();
  Serial.println("Please wait x seconds for the next connection.");
  Serial.println();
  delay(1000);                                                            //Die Abfrage der Datenbank findet jede Sekunde statt
                                                                          
sendeWerte();     
rufeWertAb();

lcd.clear();                         //leert das LCD, damit neue und alte Werte sich nicht überlagern
  lcd.setCursor(0, 0);                 
  lcd.print("ein.Temp: ");
    lcd.print(eingestellteTemp);
    lcd.setCursor(15, 0);
    lcd.print("C");
  lcd.setCursor(0, 1);
  lcd.print("akt.Temp: ");
    lcd.print(tatTemp);
    lcd.setCursor(15, 1);
    lcd.print("C");
   
}

void sendeWerte(){                            //eingestellteTemp wird via I2C an den Arduino gesendet
  byte buffer[2];
 
  buffer[0] = lowByte(eingestellteTemp);      //Integer-Variable wird in 2 Bytes getrennt 
  buffer[1] = highByte(eingestellteTemp);
  
  Wire.beginTransmission(10);                 //Verbindung zum Arduino (Slave-Adresse: 10)
  Wire.write( buffer, 2);                     //Übertragung der Bytes
  Wire.endTransmission();                     //Ende der Übertragung
}
  
void rufeWertAb() {                           //Werte werden vom Arduino abgefragt
 
  byte buf[5];
 
  int n = Wire.requestFrom(10, 6);            //es werden 6 Bytes vom Arduino (Slave-Adresse 10) abgefragt
  for ( int i = 0; i < n; i++)
  {
    buf[i] = Wire.read();                     //empfangene Bytes werden als Array zwischengespeichert
  }
  gemesseneTempInt = setzeZahlZusammen(buf[1] , buf[0]);    //Jeweil ein Paar (immer 2) von den Bytes werden zu Integer-Variablen zusammengesetzt
  eingestellteTemp = setzeZahlZusammen(buf[3] , buf[2]);
  pVentilInt = setzeZahlZusammen(buf[5] , buf[4]);
  tatTemp = (float)gemesseneTempInt /100 ;                  //Integers werden in Floats umgewandelt
  pVentil = (float)pVentilInt /100 ;
}
 
int setzeZahlZusammen(unsigned int high, unsigned int low) {        //Funktion, um aus zwei Bytes eine Integer-Variable zu kombinieren 
 
  int kombiniert;
  kombiniert = high;
  kombiniert = kombiniert * 256;
  kombiniert |= low;
  return kombiniert;
}
			 
```
			 
</details>
	
<details>
	<summary>Arduino-Code</summary>

```c


//Dieser Code ist für den Arduino Uno, welcher als Slave an der Kommunikation beteiligt ist und alle Prozesse der Temperaturregulierung steuert

// in diesem Abschnitt werden die benötigten Bibliotheken eingebunden: Zusammenfassung aller verwendeter Libaries, welche nicht direkt über den Bibliothek-Verwalter vorinstalliert sind, kannn auf der Projektseite gefunden werden.
//#include <LiquidCrystal_I2C.h>                       //ermöglicht eine einfache Komunikation mit dem LC-Display mit nur 2 Datenpins; Quelle: https://github.com/fdebrabander/Arduino-LiquidCrystal-I2C-library                                                                                                                      
#include <Wire.h>                                      //wird für die I2C-LCD Bibliothek zusätzliche für die Kommunikation benötigt benötigt; Quelle: Vorinstallierte Arduino-Bibliothek
#include <AccelStepper.h>                              //ermöglicht einfache Programmierung des Schrittmotors; Quelle: Arduino-Biliotheken-Verzeichnis
#include "max6675.h"                                   //ist für die Auslese des Thermosensors zuständig; Quelle: Arduino-Biliotheken-Verzeichnis von Adafruit

//in diesem Abschnitt werden alle benötigten Variablen und Konstanten definiert:
  //zunächst werden die Pin-Belegung:
const int PinA = 2;   //CLK: Clock-Pin für den Rotary-Encoder
const int PinB = 3;   //DT:  Daten-Output-Pin des Rotary-Encoder
const int PinSW = 8;  //SW:  Knopf-Pin des Rotary-Encoder

const int soPin = 4;  //SO: Serieller Output-Pin für das Thermoelement
const int csPin = 5;  //CS: Chip-Select-Pin für das Thermoelement
const int sckPin = 6; //SCK: Serieller Clock-Pin für das Thermoelement

#define motorPin1 9   //Die 4 benötigten Pins für den Schrittmotor werden festgelegt 
#define motorPin2 10
#define motorPin3 11
#define motorPin4 12

  //außerdem werden verschiedene Variablen für die Programmierung benötigt:
float tatTemp;                                //Variable für die gemessene Temperatur in Grad Celsius (float: mit 2 Nachkommastellen)
int gemesseneTemperaturInt;
int lastCount = 0;                            //speichert den letzten Wert des rotary encoders
volatile int eingestellteTemp = 0;            //eingestellte Temperatur: wird durch die ISR (Interrupt Service Routine) aktualisiert
float pVentil = 0;                            //Ventilstellung in Prozent (100% entspricht vollständiger Öffnung)
int pVentilInt;
int stepperPosition = 0;                      //Position des Schrittmotors in Schritten (4096 Schritte = 360°)
float tempDifferenz;                          //Differenz zwischen eingestellter Temperatur und gemessener Temperatrur  
const float schritteproprozent = 71.68;       //71.68 Schritte des Schrittmotors entpricht 1° Ventilöffnung 
int rotarySchrittwert = 5;                    //Wertigkeit jedes am Rotaryencoder eingestellten Schrittes

#define HALFSTEP 8                            //der Schrittmotor soll im Halfstep-Modus betrieben

AccelStepper stepper1(HALFSTEP, motorPin1, motorPin3, motorPin2, motorPin4);    //das Objekt "stepper1" wird initialisiert

MAX6675 thermo(sckPin, csPin, soPin);                                           //das Objekt "thermo" wird initialisiert


//Der folgende Programmteil wird nur einmal abgerufen:
void setup()       
{
  Serial.begin(9600);    //die serielle Kommunikation wird gestartet
    delay(1000);         //Zeit, damit sich die Sensoren kalibrieren können 
  
  Wire.begin(10);                     //der I2C-Datenbus wird initalisiert
  Wire.onRequest(antwortfunktion);    //wenn eine Datenabfrage ankommt, wird "antwortfunktion" ausgeführt 
  Wire.onReceive(empfangfunktion);    //wenn Daten empfangen werden, wird "empfangfunktion" ausgeführt
 
  stepper1.setCurrentPosition(0);     //die aktuelle Position des Schrittmotors wird = 0 gesetzt
  stepper1.setMaxSpeed(1000.0);       //die maximale Geschwindigkeit des Steppers wird auf 1000 Schritte pro Sekunde gesetzt 
  stepper1.setAcceleration(1000.0);   //die Beschleunigung des Steppers wird auf 1000 Schritte pro Sekunde^2 gesetzt 
  stepper1.setSpeed(1000);            //die Geschwindigkeit des Steppers wird auf 1000 Schritte pro Sekunde festgelegt 

  pinMode(PinA, INPUT);               //PinA und PinB sind INPUTs, um die Signale des Rotary-Encoders zu lesen
  pinMode(PinB, INPUT);
  pinMode(PinSW, INPUT_PULLUP);       //der SW-Pin ist potentailfrei; es wird ein Widerstand benötigt, dafür wird der im Arduino verbaute Pullup-Widerstand verwendet

  Serial.println("Start");  //das Setup ist ausgeführt; im seriellen Monitor wir das mit "Start" signalisiert
} 

//Der folgende Programmteil wird bei Vollendung wiederholt
void loop()
{
  float tatTemp = thermo.readCelsius();               //das Thermomenter wird ausgelesen und der Wert als Variable überführt
  gemesseneTemperaturInt = tatTemp * 100;
         delay(300);
  
delay(100);                           //0,1 Sekunden Pause, damit die Sensoren neue Werte bilden können

  tempDifferenz = eingestellteTemp - tatTemp;               //Differenz aus eingestellter Temperatur und gemessener Temperatur wird gebildet und als int Variable gespeichert

  stepperPosition = pVentil * schritteproprozent;           //die Position des Steppers ist das Produkt der gewünschten Ventilstellung und der Anzahl der Schritte, welche für 1% benötigt werden

                                                             
  pVentil= 80/(1+ pow(1.15, -tempDifferenz + 35)) +0.3;     //mathematische Funktion, welche die Temperaturdifferenz in eine Ventilstellung umsetzt
  pVentil = min(100, max(0, pVentil));                      //der Wertebereich der Ventilöffnung wir zwischen 0% und 100% begrenzt
  pVentilInt = pVentil * 100;

  stepperPosition = min(7168, max(0, stepperPosition));     //um sicherzugehen, dass der Motor nicht zu weit dreht und die Hardware beschädigt, wird auch die maximale Drehung begrenzt

//dieser Programmabschnitt aktuallisert die Position des Schrittmotors:
stepper1.moveTo(stepperPosition);                     
stepper1.runToPosition();          //leider wird der Code an diese Stelle pausiert; der Schrittmotor sollte also möglichst schnell drehen
stepper1.disableOutputs();         //die Pins für den Schrittmotor werden deaktiviert. Somit wird Strom gespart und eine Überhitzung des Motors verhindert

//der serielle Monitor dient unserem Projekt als Kontrollbildschirm, deshalb werden alle wichtigen Werte abgebildet: 
  Serial.print("Eingestellte Temperatur: ");          
  Serial.println(eingestellteTemp);
         Serial.println(" ");
         
  Serial.print("Gemessene Temperatur in C: ");
  Serial.println(tatTemp);
         Serial.println(" ");
         
  Serial.print("Ventilöffnung in Prozent: ");
  Serial.println(pVentil);
         Serial.println(" ");

  Serial.println("------------------------------------");  //dient der Übersicht im seriellen Monitor


void empfangfunktion(){            //entreffende Informationen werden verarbeitet

  byte buf[2];
  for ( int i = 0; i < 2; i++)
  {
    buf[i] = Wire.read();          //eintreffende Bytes werden als Array zwischengespeichert
  }
  eingestellteTemp = setzeZahlZusammen(buf[1] , buf[0]);    //die beiden Bytes werden zu einer Integer-Variablen zusammengesetzt
}

void antwortfunktion(){            //eintreffende Aufforderung zur Datenübertragung wird verarbeitet
  byte buffer[6];
 
  buffer[0] = lowByte(gemesseneTemperaturInt);        //Variablen werden in Bytes zerlegt und in einem Array zwischengespeichert
  buffer[1] = highByte(gemesseneTemperaturInt);         
  buffer[2] = lowByte(eingestellteTemp);
  buffer[3] = highByte(eingestellteTemp);
  buffer[4] = lowByte(pVentilInt);
  buffer[5] = highByte(pVentilInt);
   
  Wire.write( buffer, 6);                             //Daten des Arrays werden byteweise übertragen
}

int setzeZahlZusammen(unsigned int high, unsigned int low) {        //Funktion, um aus zwei Bytes eine Integer-Variable zu kombinieren 
 
  int kombiniert;
  kombiniert = high;
  kombiniert = kombiniert * 256;
  kombiniert |= low;
  return kombiniert;
}
			 
```
			 
</details>

<details>
	<summary>Bildergalerie</summary>
<img src="https://user-images.githubusercontent.com/88385654/162285762-33a34b93-8f7b-4fb2-a711-8fb98e651993.jpg">
<img src="https://user-images.githubusercontent.com/88385654/162286244-802831b5-fc2f-45b2-b197-70e9fe4a1865.jpg">

</details>

<hr>

<h3> <a id="relexion"> 3.1 Reflexion des Projekts </a></h3>

Dieses Projekt hat von uns einiges abverlangt. Daher sind wir umso glücklicher und stolzer, dass jetzt dieses unserer Meinung nach sehr ansehnliche Endprodukt entstanden ist. Grundsätzlich lässt sich erneut sehr positiv festhalten, dass die Chemie innerhalb der Gruppe immer gestimmt hat. Allerdings wurden wir bei diesem Projekt vor mehr Hürden gestellt als beim Letzten. Dementsprechend sind leider auch ein paar Dinge, die wir fest geplant hatten umzusetzen, nicht erreicht worden. Dies liegt zum einen an dem deutlich größeren Zeitaufwand als eingangs erwartet und der aufgrund des Abiturs generell knappen Zeit. <br/>
Während der Projektfindungsphase hatten wir die Wahl, ob wir uns für ein neues Projekt entscheiden und softwarelastig arbeiten oder ob wir in unserem Komfortbereich, dem physical computing mit Hilfe von Arduino, bleiben. Das Resultat dieser Projektfindungsphase war interessanterweise ein Kompromiss aus beiden Möglichkeiten. Da der arduinogesteuerte Gaskocher wirklich ein Herzensprojekt geworden ist, fiel es uns schwer dieses einfach abzuhaken. Allerdings wollten wir auch neue Dinge lernen, ausprobieren und testen. Vor dem Hintergrund der praktischen Anwendung in einer kommenden softwarelastigen Welt, hat uns vor allem das Programmieren von Websiten und das Zusammenspiel aus Website und Servern interessiert. Der logische Schluss aus diesen beiden Anliegen ist ein ferngesteuerter Gaskocher. Die Idee des webgesteuerten Gaskocher war geboren. <br/>
Die Kombination dieser Ideen wirkt vielleicht nicht zwingend, aber sie erlaubte uns uns neu auszuprobieren und zu beweisen, aber unser Herzensprojekt weiterzuführen. Außerdem lassen sich auch mit etwas Fantasie durchaus praktische Anwendungen finden, die das Potenzial haben das Kochen und vor allem das "convinience Kochen" zu verändern. <br/>
Da das Projekt mit Allem, was es erfordert für uns Neuland darstellte, begann eine lange Einarbeitungsphase. Im Nachhinein war diese evt. ein wenig zu lang, allerdings eigentlich auch erforderlich und gewinnbringend, da Grundlagen für das Projekt gelegt wurden und auch viel Wissen für das spätere Leben erlangt wurde. Nachdem die Einarbeitungsphase abgeschlossen war, begann die konkrete Planungsphase wie ein solches Projekt zu realisieren ist und welche Dinge, sowohl auf Software- als auch auf Hardwareebene, erforderlich sind. Die Hardware wurde bestellt und sich auf die Suche nach Serverplatz begeben. Glücklicherweise war Herr Adiwidjaja so nett uns Serverplatz und einen Datenbankzugang zur Verfügung zu stellen, da unser Projekt wahrscheinlich sonst an dieser Stelle gescheitert wäre oder zumindest deutlich komplizierter geworden wäre.<br/>
Sobald der ESP angekommen war und der Server bereit stand, begann die Arbeitsphase. Wir versuchten aus Zeitgründen das Projekt von zwei Seiten aus anzugehen. Auf der einen Seite wurde an der Website und der Kommunikation zwischen Website und Datenbank gearbeitet. Auf der Anderen wurde an der Kommunikation zwischen ESP und Arduino als Slave und Master gearbeitet. Die Erstellung der Website gestaltete sich relativ einfach, weil bereits Vorkentnisse in html vorhanden waren. Auch die Einarbeitung in css erfolgte relativ schnell. Außerdem musste die Website nur funktional und simpel sein, sodass dieser Punkt nicht sonderlich komplex war. Auch das Hosten der Website auf dem Server klappte schnell. Problematisch war allerdings die Kommunikation zwischen Server, Website und Datenbank, da dafür php erforderlich war und sich diese Programmiersprache deutlich von html unterscheidet. Auffällig ist, dass die Befehle und erforderlichen Skripte oft sehr kurz sind und einfach aussehen. Die Kunst liegt jedoch im Detail und man muss genau die richtige Funktion auswählen oder das gesamte Skript funktioniert nicht. Trotz der Schwierigkeiten, waren jedoch die zu erldigenden Schritte relativ schnell erreicht. 
So ähnlich verhielt es sich mit der Kommunikation zwischen ESP und Arduino. Auch hier gab es einige Tücken, die für Probleme gesorgt haben. Unterm Strich war allerdings auch dieser Zwischenschritt schnell erreicht. Sodass für ein funktionierendes Produkt nur noch die Kommunikation zwischen ESP und Datenbank fehlte. Die Fusion aus Arduino und php sorgte allerdings für deutlich mehr Probleme als gedacht. Es war frustrierend zu sehen, wie so kurz vor dem Durchbruch sich immer wieder neue Probleme aufgetan haben, Zeit verging, kein Fortschritt erreicht wurde und das Projekt zu scheitern drohte. Diese Schnittstelle ist ein Beweis dafür wie eng in der Informatikwelt alles zusammenhängt und von einem kleinen Problem der Erfolg des gesamten Projekts abhängen kann. Um ein Erfolgserlebnis zu haben, entschieden wir uns dazu ein einfacheres Projekt mit Vorlage aus dem Internet anzugehen. Allerdings erwarteten uns auch hier Probleme und das Frustrationslevel stieg noch einmal deutlich an. Nach über zwei Wochen und der Hilfe von Herrn Buhl und Henrik gelang schließlich der Durchbruch. Die Freude darüber war dementsprechend groß und die Motivation das Projekt jetzt gut zu Ende zu führen ebenfalls. <br/>
Nach diesen etlichen Stunden Arbeit wartete jetzt die Belohnung: Die Finalisierung des Projekts. Auch wenn es auch noch Arbeit bedeute die Codes zusammenzuführen und auf unser Projekt zu übertragen gelangen diese Schritte vergleichsweise schnell und unproblematisch. Nachdem der Meilenstein erreicht wurde und das fertige Produktvideo aufgenommen wurde, war innerhalb der Gruppe eine große Erleichterung zu spüren. 
<br/> <br/>
Aus einer Retroperspektive war dieses Projekt sehr lehrreich. Auch wenn die Dinge deutlich länger gedauert haben als wir dachten, konnten wir viel daraus lernen und mitnehmen. Es lohnt sich durchzuhalten und weiterzumachen, weil irgendwann der Durchbruch passieren wird. Leider hatte diese Verzögerung zur Folge, dass einige Ziele, wie die Verschönerung der Hardware, nicht umgesetzt wurden. Dies ist sehr schade, weil so eine erhoffte Teilnahme an "Jugend forscht" sehr unrealistisch erscheint. Auch wäre es schön gewesen, wenn die Website interaktiv mit einem Wertemonitor wäre. Daher ist es besonders schade, dass die Umseztung durch die Hardware scheitert. Für eventuelle Weiterarbeiten sind jedoch die Weichen gestellt, da die Software bereits vorhanden ist. 
Auch wenn nicht alles zu 100 % nach Plan lief und wir durch das erste Projekt sehr erfolgsverwöhnt waren, ist es schön zu sehen was aus all dieser Arbeit geworden ist und dass es am Ende ein funktionierendes Enprodukt gibt. Aus vielen kleinen Zahnrädern, die einzeln erstellt wurden, ist am Ende eine funktionierende und sinnige Einheit entstanden. Darauf sind wir sehr stolz, sodass das Projekt auf jeden Fall ein Erfolg war!


