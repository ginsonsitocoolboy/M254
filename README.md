# M254

## Ziel des Prozesses
Der Prozess schickt automatisch eine E-Mail an eine Person. In der E-Mail steht, wie das Wetter an einem bestimmten Ort und zu einer bestimmten Zeit ist. Ausserdem ist ein lustiger Dad-joke dabei, damit man beim Lesen auch lachen kann. Das Ziel ist es also einfach bei Planungen das Wetter vorherzusehen


## Inbetriebnahme vom Prozess
Ich muss nur Docker desktop öffnen und den Container starten. Danach muss ich das BPMN mit localhost deployen. Anschliessend öffne ich im browser mit localhost:8081 und localhost:8082 die Camunda Operate und Tasklist Seite. 

## Bedienung vom Prozess
Wenn man den Prozess startet sieht man ein Formular. Dort kann man aufschreiben wo man ist und wann man das Wetter wissen will.
Danach wird es die Wetter Daten und den Dad Joke abrufen. anschliessend kommt wieder ein Formular erscheinen das man bestätig dass, das Mail wirklich gesendet werden soll. Anschliessend sollte es ein Mail mit dem Wetter und Dad Joke senden.

## Funktionsweise des Prozesses
Der Prozess beginnt mit einem Formular, in dem man den Ort und die Uhrzeit eingibt, für die man das Wetter wissen möchte. Danach fragt der Prozess automatisch ein openweathermap nach dem Wetter und holt sich zusätzlich einen lustigen Witz von icanhazdadjoke.

Bevor die EMail abgeschickt wird, erscheint ein weiteres Formular. Dort kann man mit einer Checkbox auswählen, ob man die E-Mail wirklich bekommen möchte. Wenn man das Häkchen setzt, wird die EMail versendet. Wenn nicht, wird der Prozess beendet.

Wenn man sich für den Versand entscheidet, schreibt der Prozess eine E-Mail mit dem Wetter und dem Witz und verschickt sie an die eingegebene Adresse.


## Probleme mit AWS
Ich habe Anfangs mit AWS gearbeitet aber ich hatte viele Probleme wenns ums Camunda operate und taskliste ging. Ich habe die meiste Zeit verbracht an einem Problem das ich schlussendlich gar nicht lösen konnte. Ich habe alles kontrolliert bei AWS und es hat sich nichts getan. Der Fehler war einfach nachdem ich den User Task abgeschlossen habe hat sich Wetter abrufen nicht ausgeführt. Es ist einfach stehen geblieben ohne Error. Ich habe es dann gelöst indem ich es einfach Lokal auf Docker desktop gemacht habe. Ich habe dennoch viel Zeit verloren wegen dem.

## Probleme mit Send grid Mail
Ich habe einen Send grid Account eingerichtet und den API-Key erstellt. Danach einen verified Sender erstellt. Ich habe es ins Camunda eingebaut mit dem Send Grid Outbound Connector. Danach im Camunda operate ist alles bis zum Ende durch. Ich habe aber kein Mail auf meine Email bekommen. Ich habe im Send grid Dashboard nachgeschaut, dort hatte es 4 Requests aber keine wurde zugestellt. Dafür hatte ich jedoch zu wenig Zeit um es zu lösen. 


