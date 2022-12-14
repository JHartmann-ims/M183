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

[![Video](https://img.youtube.com/vi/FwIUkAwKzG8/maxresdefault.jpg)](https://www.youtube.com/watch?v=FarGpSSHgL8)

Viele Websiten haben eine zusätzliche Datenbank, in denen Sie die Informationen von Benutzern speichern. Diese Informationen werden oft für das Einloggen in das System verwendet. Um sich in ein ungesichertes System einzuloggen, ohne die benötigten Daten zu haben, kann man dafür eine SQL-injection durchführen. Hätte man Eingabefelder für das Username und das Passwort, würde die Database Query ungefähr so aussehen, wenn wir als Username "admin" und als Passwort "password123" eingeben.

```
    SELECT * FROM users WHERE username ='admin' AND password='password'
```



* Eine textliche Beschreibung
* Ein deutliches, aussagekräftiges Bild oder eine kommentierte Bildschirm-Aufnahme
* Ein gut dokumentierter Code-Fetzen
* Ein Link zu einem *selbst aufgenommenen* youtube-Video oder `.gif`.

## Verifikation

✍️ Erklären Sie kurz und bündig, inwiefern die von Ihnen verwendeten Medien zeigen, was Sie gelernt haben.

# Reflektion zum Arbeitsprozess

👍 Überlegen Sie sich jeweils etwas, was gut an Ihrer Arbeit lief; 

👎 und etwas, was nicht gut lief.

**VBV**: ✍️ Formulieren Sie davon ausgehend einen *handelbaren* Verbesserungsvorschlag.
