# Lern-Bericht
Julian Hartmann

## Einleitung

SQL-Injections auf einer ungesicherten Website duchführen.

## Was habe ich gelernt?

Ich habe gelernt, wie man mithilfe von SQL-Injections die Datenbank von einer Website manipuliert.

## Beschreibung

Klicken Sie auf das Bild, um ein Video dazu zu sehen.

[![Watch the video](https://img.youtube.com/vi/FarGpSSHgL8/sddefault.jpg)](https://www.youtube.com/watch?v=FarGpSSHgL8)

Viele Websiten haben eine zusätzliche Datenbank, in denen Sie die Informationen von Benutzern speichern. Diese Informationen werden oft für das Einloggen in das System verwendet. Um sich in ein ungesichertes System einzuloggen, ohne die benötigten Daten zu haben, kann man dafür eine SQL-injection durchführen. Hätte man Eingabefelder für das Username und das Passwort, würde die Database Query ungefähr so aussehen, wenn wir als Username "admin" und als Passwort "password123" eingeben würden.

```
    SELECT * FROM users WHERE username ='admin' AND password='password'
```
Es wird nachgeschaut, ob es diese Anmeldedaten gibt. So würde die Anmeldung fehlschlagen. Wie man sieht wurden die Eingaben als Strings ausgegeben. Das heisst wir könnten selber Strings hinzufügen. Wir müssen ein Statement hinzufügen, das immer stimmt. "2=2" stimmt immer, also benutzen wir dies. Die Eingabe als Username würde so aussehen: "admin' OR '2'='2".

```
    SELECT * FROM users WHERE username ='admin' OR '1'='1' AND password='password'
```
Man ist erfolgreich eingeloggt.

## Verifikation

Mit dem gegebenen Code-Abschnitt und dem Video wird validiert, dass ich gelernt habe, wie man eine SQL-injection auf eine unsichere Website mache.

# Reflektion zum Arbeitsprozess

👍 Das Verstehen von diesem Konzept ist einfach vergangen, weil ich schon Erfahrungen mit SQL gemacht habe.

👎 Am Anfang hatte ich kleine Probleme, die SQL-injections durchzuführen, da ich meine Strings nicht richtig eingesetzt habe.

**VBV**: Bevor ich mit dem Arbeiten starte, sollte ich mich erst über dieses Thema ein bisschen informieren.
