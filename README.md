# Notebooks zu E1/E1p: Mechanik

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/SoftmatterLMU-RaedlerGroup/notebooks_E1_WS2019-20/master)

Dieses Repository enthält Jupyter-Notebooks zur Vorlesung [E1/E1p: Mechanik](https://www.physik.uni-muenchen.de/lehre/vorlesungen/wise_19_20/E1/index.html) im Wintersemester 2019/20.

Die Notebooks können lokal oder [online](https://mybinder.org/v2/gh/SoftmatterLMU-RaedlerGroup/notebooks_E1_WS2019-20/master) ausgeführt werden.

## Hinweise zur Online-Ausführung
Beachten Sie, dass Sitzungen, die Sie online auf Binder starten, nur eine begrenzte Laufzeit haben und bereits nach 10 Minuten Inaktivität automatisch beendet werden.
Alle Änderungen, die Sie online vornehmen, gehen nach Beenden der Sitzung verloren.
Denken Sie also daran, Ihre Ergebnisse regelmäßig zu sichern.

## Hinweise zur lokalen Ausführung
Für die lokale Ausführung wird eine Python-3.7-Installation benötigt.
Sie können Python 3.7 und die benötigten Pakete beispielsweise über Anaconda installieren; fortgeschrittene Nutzer können auch direkt mit `pip` arbeiten.

### Einrichtung mit Anaconda
* [Laden](https://docs.conda.io/projects/continuumio-conda/en/latest/user-guide/install/download.html) Sie sich die Python-3.7-Version von Anaconda oder Miniconda herunter und installieren Sie auf Ihrem Rechner.
* Öffnen Sie das Programm „Anaconda Prompt“.
* Laden Sie dieses Repository als ZIP-Datei herunter (Klick auf „Clone or download“ > „Download ZIP“ oben rechts) und entpacken Sie die ZIP-Datei.
* Führen Sie in der Anaconda Prompt den Befehl `conda install --file requirements.txt` aus, wobei `requirements.txt` gegebenenfalls durch den Pfad zur Ihrer lokalen Kopie der Datei `requirements.txt` aus diesem Repository zu ersetzen ist.
* Starten Sie nun den Notebook-Server, wie unten beschrieben.

### Einrichten des Repositories im CIP-Pool
Im CIP-Pool ist Python bereits installiert.

#### Einmalige Einrichtung
Führen Sie die folgenden Anweisungen aus, um das Repository einzurichten.
Diese Anweisungen sind nur einmalig auszuführen.

Zuerst öffnen Sie ein Terminal-Fenster.
Laden Sie das Repository herunter; da im CIP-Pool Git installiert ist, führen Sie dazu einfach den folgenden Befehl aus:

```
git clone https://github.com/SoftmatterLMU-RaedlerGroup/notebooks_E1_WS2019-20.git
```

Wechseln Sie nun in das Verzeichnis des Repositories:

```
cd notebooks_E1_WS2019-20
```

Laden Sie den `conda`-Befehl:

```
module load python
```

Erstellen Sie ein neues Environment (im Folgenden beispielhaft „e1“) und installieren Sie die benötigten Pakete, die in der Datei `requirements.txt` abgelegt sind:

```
conda create -n e1 python=3.7
conda install --file requirements.txt
```

Starten Sie nun den Notebook-Server, wie unten beschrieben.

#### Vorbereitung zum Starten des Notebook-Servers
Führen Sie folgende Befehle durch, um eine neue Sitzung zu starten.

Laden Sie den `conda`-Befehl und aktivieren Sie das Environment (z.B. `e1`):

```
module load python
conda activate e1
```

Aktualisieren Sie Ihre lokale Kopie des Repositories. Wechseln Sie dazu zuerst in das Verzeichnis des Repositories und laden Sie die neue Version mit Git herunter. Speichern Sie Ihre Änderungen gegebenenfalls in einem neuen Git-Branch.

```
cd notebooks_E1_WS2019-20
git checkout master
git pull
```

Starten Sie nun den Notebook-Server, wie unten beschrieben.


### Starten des Notebook-Servers
Starten Sie den Notebook-Server mit dem Befehl `jupyter notebook`.
Es öffnet sich automatisch ein Browserfenster mit einer Übersicht der Dateien im aktuellen Verzeichnis.
Navigieren Sie in das Verzeichnis, in dem sich die Notebooks (Dateien mit der Endung `.ipynb`) befinden und klicken Sie auf das Notebook, das Sie öffnen möchten.
