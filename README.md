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
</ul>
  
<b> 2. Das Projekt</b>
<br/>
<ul>
&#10148; <a href="#arduino"> 2.1 Arduino</a> <br/>
&#10148; <a href="#website"> 2.2 Website, Datenbank, Sever</a> <br/>
&#10148; <a href="#endprodukt"> 2.3 Das Endprodukt</a>
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

<b> Kommunikation zwischen Datenbank und ESP</b>

</details>
<h3> <a id="hardware"> 1.4 erforderliche Hardware </a></h3>



<h3> <a id="software"> 1.5 verwendete Programme</a></h3>

<img align="left" width="50" src="https://user-images.githubusercontent.com/88385654/162216442-6b213f8b-9ab6-4c8b-a1ef-9fb5bb28b9e5.png"> 
<b>Visual Studio Code</b><br/>
Visual Studio Code ist ein kostenloser Quelltexteditor und ist in der Informatikwelt weit verbreitet. Besonders hilfreich ist die automatische Färbung des Quellcodes während des Schreibens und die automatische sehr übersichtliche Unterteilung in verschiedene Code-Ebenen.
<br/>

<details>
 <summary>Visual Studio Code - Bilder</summary>
<img src="https://user-images.githubusercontent.com/88385654/162217609-d03f41a5-bebb-47a6-bce0-654b1227a87d.png">

</details>

<img align="left" width="50" src="https://user-images.githubusercontent.com/88385654/162218087-85a6771b-7c7f-43be-9c90-dd594e06b684.png">
<b>CyberDuck</b><br/>
CyberDuck ist ein kostenloser FTP-Client, der den Zugriff auf Sever ermöglicht. So wird ermöglicht, dass lokal gespeicherte und erstellte Dokumente auf den Server geladen werden können. 
<br/>

<details>
 <summary>CyberDuck - Bilder</summary>
<img src="https://user-images.githubusercontent.com/88385654/162220411-d2c8a4f6-9dbb-4031-9ddd-2a1b77940fe8.png"><br/>
<img src="https://user-images.githubusercontent.com/88385654/162220425-b921302c-cec1-4d54-8069-3a19cdbee3dc.png">
 
</details>

<img align="left" width="50" src="https://user-images.githubusercontent.com/88385654/162222149-c9971214-9a89-4cd0-8eec-5c60f0df86a6.png">
<b>Fritzing</b><br/>
Fritzing ist ein Programm zur Digitalisierung von Schaltplänen. Das Programm wurde sich bereits während der letzten Projektphase gekauft und auch dieses Halbjahr, wenn auch deutlich weniger, benutzt.
<details>
 <summary>Fritzing - Bilder</summary>
<img src="https://user-images.githubusercontent.com/88385654/162222942-a2534ad8-fa7f-46db-8d3e-05522e736223.png">

</details>

<img align="left" width="50" src="https://user-images.githubusercontent.com/88385654/162223091-b2dca110-6384-422f-9708-bbe419281338.png">
<b>Arduino</b><br/>
Auch dieses Halbjahr wurde der Arduino mit dem eigenen Codeeditor viel genutzt. 
<details>
 <summary>Arduino - Bilder </summary>
<img src="https://user-images.githubusercontent.com/88385654/162223731-b526657f-9fbc-44f2-90b0-40e76a443f68.png">                                       </details>

<h3> <a id="arduino"> 2.1 Arduino </a></h3>


<h3> <a id="website"> 2.2 Website, Dantenbank, Server </a></h3>

Zuerst wurde eine recht simple Website mit Hilfe von html und ein wenig css erstellt. Dafür wurde bei visual studio code eine index.html - Datei und ein stylesheet.css angelegt. Die Website ist absichtlich sehr simpel gehalten und soll vor allen Dingen funktional sein. Die beiden Bilder auf der rechten Seite sind eine kleine Spielerei und sollen an das Layout der Stundenprotokolle erinnern. Da die Website als Steuerzentrale funktionieren soll, befindet sich dort ein html-input Feld. Über das Feld können verschiedene Dinge wie Typ, Maximalwert, Minimalwert und Ausgangswert eingestellt werden. Um ein einheitliches und ansprechendes Design zu erreichen wurden mit Hilfe von dem stylesheet Ramen und andere Verschönerung programmiert. Diese Schritte funktionierten nach einer Einarbeitungsphase relativ problemlos und schnell. 

<details>
 <summary>index.html</summary>
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
 <summary>Screenshot der Website</summary>
 <img src="https://user-images.githubusercontent.com/88385654/162228599-0879e232-9569-42cc-8d70-3606e7b99b68.png">
</details>



<hr>
<h3> <a id="endprodukt"> 2.3 Das Endprodukt </a></h3>


<h3> <a id="relexion"> 3.1 Reflexion des Projekts </a></h3>


