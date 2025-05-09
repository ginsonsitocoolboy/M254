# M254

## Ziel des Prozesses
Der Prozess schickt automatisch eine E-Mail an eine Person. In der E-Mail steht, wie das Wetter an einem bestimmten Ort und zu einer bestimmten Zeit ist. Ausserdem ist ein lustiger Dad-joke dabei, damit man beim Lesen auch lachen kann. Das Ziel ist es also einfach bei Planungen das Wetter vorherzusehen


## Inbetriebnahme vom Prozess
Ich habe den Prozess mit Docker Desktop gestartet. Dafür habe ich eine Datei geöffnet. Diese Datei sorgt dafür dass alles startet was man braucht. Es öffnen sich dann viele kleine Programme. Zum Beispiel Camunda und Zeebe. Auch ein Programm das E Mails verschicken kann. Wenn alles fertig ist kann man den Prozess im Browser sehen und starten

## Bedienung vom Prozess
Wenn man den Prozess startet sieht man ein Formular. Dort kann man aufschreiben wo man ist und wann man das Wetter wissen will.
Danach wird es die Wetter Daten und den Dad Joke abrufen. anschliessend kommt wieder ein Formular erscheinen das man bestätig dass, das Mail wirklich gesendet werden soll. Anschliessend sollte es ein Mail mit dem Wetter und Dad Joke senden.

## Wie der Prozess funktioniert
Der Prozess schaut zuerst was du aufgeschrieben hast. Dann fragt er eine Webseite nach dem Wetter. Danach fragt er eine andere Webseite nach einem Witz. Wenn er beides hat schreibt er eine E Mail. Diese EMail wird auf die angegebene Mail geschickt.

## Probleme mit AWS
Ich habe Anfangs mit AWS gearbeitet aber ich hatte viele Probleme wenns ums Camunda operate und taskliste ging. Ich habe 3 Tage lang verbracht an einem Problem das ich schlussendlich gar nicht lösen konnte. Ich habe alles konrtolliert bei AWS und es hat sich nichts getan. Der Fehler war einfach nachdem ich den User Task abgeschlossen habe hat sich Wetter abrufen nicht ausgeführt. Es ist einfach stehen geblieben ohne Error. Ich habe es dann gelöst indem ich es einfach Lokal auf Docker desktop gemacht habe. Ich habe dennoch viel Zeit verloren wegen dem.

## Probleme mit Send grid Mail
Ich habe einen Send grid Account eingerichtet und den API-Key erstellt. Danach einen verified Sender erstellt. Ich habe es ins Camunda eingebaut mit dem Send Grid Outbound Connector. Danach im Camunda operate ist alles bis zum Ende durch. Ich habe aber kein Mail auf meine Email bekommen. Ich habe im Send grid Dashboard nachgeschaut, dort hatte es 4 Requests aber keine wurde zugestellt. Dafür hatte ich jedoch zu wenig Zeit um es zu lösen. 


