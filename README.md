# Docker Image für Pandoc 2.3

## Pandoc für *Continuous Integration (CI)*

In seinem Buch "Markdown & Pandoc" (2. Aufl. 10/2018) zeigt Michael Kofler, wie Pandoc in einem Dockercontainer ausgeführt werden kann. Mit diesem Ansatz ist es möglich, verschiedene Pandoc-Versionen zu verwenden.

Ein weiterer Anwendungsfall für Pandoc im Dockercontainer ergibt sich, wenn gemeinsam auf Plattformen wie GitHub oder GitLab mit Pandoc Dokumente generiert werden sollen. GitLab bietet eine ganzheitliche Kette für CI: Jede Änderung an (Quell)texten - egal, von welchen oder wievielen Beitragenden ausgeführt - führt damit zu einer neuen Version des Zielpodukts. Vgl. hierzu [die Dokumentation auf GitLab zu den verschiedenen Szenarien für CI](https://docs.gitlab.com/ce/ci/README.html).

## Dockerfile

Dieses GitHub-Repository enthält neben diesem Text nur noch das [`Dockerfile`](https://github.com/xldrkp/pandoc_23/blob/master/Dockerfile), das dem Buch von Michael Kofler (S. 185f.) entnommen ist und lediglich leicht abgewandelt wurde.

## Image auf Docker Hub

Auf Basis des Dockerfiles wird automatisch auf [Docker Hub ein Dockerimage generiert](https://hub.docker.com/r/xldrkp/pandoc_23_auto/), das für CI mit GitLab verwendet wird.

## GitLab Repository mit Pandoc zum kollaborativen Schreiben

Auf GitLab.com liegt [ein Beispielrepository](https://gitlab.com/xldrkp/collaborative-writing), in dem auf einfachste Weise gezeigt wird, wie Markdowndateien online zu verschiedenen Zieldokumenten konvertiert werden. Dabei kommt das Dockerimage zum Einsatz, das bei Docker Hub liegt.
