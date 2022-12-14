# Lern-Bericht
Julian Hartmann

## Einleitung

✍️ Ein Satz, worum es in dem Projekt ging. Muss für einen externen Leser einfach zu verstehen sein.
SQL-Injections auf einer ungesicherten Website duchführen.

## Was habe ich gelernt?

✍️ Beschreiben Sie in einem Satz **eine** Sache, die Sie bei diesem Projekt gelernt haben und die Sie in diesem Lern-Bericht dokumentieren.
Ich habe gelernt, wie man mithilfe von SQL-Injections die Datenbank manipuliert.

## Beschreibung

✍️ Verwenden Sie drei verschiedene Medien, um zu zeigen, was Sie gelernt haben. Zum Beispiel:

[![Watch the video](https://imgur.com/a/pJp4dZZ.png)](https://www.youtube.com/watch?v=FarGpSSHgL8)

Viele Websiten haben eine zusätzliche Datenbank, in denen Sie die Informationen von Benutzern speichern. Diese Informationen werden oft für das Einloggen in das System verwendet. Um sich in ein ungesichertes System einzuloggen, ohne die benötigten Daten zu haben, kann man dafür eine SQL-injection durchführen. Hätte man Eingabefelder für das Username und das Passwort, würde die Database Query ungefähr so aussehen, wenn wir als Username "admin" und als Passwort "password123" eingeben.

```
    SELECT * FROM users WHERE username ='admin' AND password='password'
```
Es wird nachgeschaut, ob es diese Anmeldedaten gibt. So würde die Anmeldung fehlschlagen. Wie man sieht wurden die Eingaben als Strings ausgegeben. Das heisst wir könnten selber Strings hinzufügen. Wir müssen ein Statement hinzufügen, das immer stimmt. "2=2" stimmt immer, also benutzen wir dies. Die Eingabe als Username würde so aussehen: "admin' OR '2'='2".

```
    SELECT * FROM users WHERE username ='admin' OR '1'='1' AND password='password'
```
Man ist erfolgreich eingeloggt.

## Verifikation

✍️ Erklären Sie kurz und bündig, inwiefern die von Ihnen verwendeten Medien zeigen, was Sie gelernt haben.

# Reflektion zum Arbeitsprozess

👍 Überlegen Sie sich jeweils etwas, was gut an Ihrer Arbeit lief; 

👎 und etwas, was nicht gut lief.

**VBV**: ✍️ Formulieren Sie davon ausgehend einen *handelbaren* Verbesserungsvorschlag.
