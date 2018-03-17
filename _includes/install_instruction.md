# Über 
Das {{ page.distro | capitalize }} Repo stellt Pakete für folgende Releases bereit:
{% for release in page.releases %}
 * {{ release }}
{% endfor %}

Das {{ page.distro | capitalize }} Repo stellt Pakete für folgende Architekturen bereit:
{% for arch in page.archs %}
 * {{ arch }}
{% endfor %}

# Einrichtung

Keyring hinzufügen
```
$ wget -q -O - https://packages.norbert-ruehl.de/conf/apt.gpg.key | sudo apt-key add -
```
Überprüfen sie dass der Schlüssel mit dem Fingerprint A707 BA5B 1717 0ACF 28B8 7BD7 F046 C5DF A455 A434 hinzugefügt wurde
```
$ apt-key fingerprint A455A434
pub   rsa4096 2016-05-12 [SC]
      A707 BA5B 1717 0ACF 28B8  7DB7 F046 C5DF A455 A434
uid           [ unknown] Norbert Ruehl <packages@norbert-ruehl.de>
sub   rsa4096 2016-05-12 [E]
```



Eintrag den apt source listen hinzufügen
```
$ sudo sh -c 'echo deb https://packages.norbert-ruehl.de/{{ page.distro }} $(lsb_release -cs) main > /etc/apt/sources.list.d/packages.norbert-ruehl.de.list'
```

Nach dem hinzufügen des Repos sollte das Paket test-norberepo auffindbar sein.
```
$ sudo apt-get update
$ apt-cache search test-norberepo
```

Gegebenenfalls ist es notwendig apt-transport-https nachzuinstallieren
```
$ sudo apt-get install apt-transport-https -y
```


```
$ sudo apt-get install test-norberepo 
$ test-norberepo
Repo Location: https://packages.norbert-ruehl.de
```

