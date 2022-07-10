# Vorgehensweise

Im Folgenden wird nun die Vorgehensweise im Projekt beschrieben.

### 1. Thema festlegen

Im ersten Schritt war die Festlegung eines Themas erforderlich. Hierfür wurde die Website der [Dash-Gallery](https://dash.gallery/Portal/) herangezogen, um bereits umgesetzte Dashboards einzusehen. Das sollte als Inspirationsquelle dienen, um eigene Ideen zu entwickeln. Zudem konnte man sich einen Überblick über verschiedenste Visualisierungsformen verschaffen. 

Durch bereits durchgeführte Projekte der vergangenen Semester, waren Kenntnisse im Bereich Web Scraping vorhanden. Aus diesem Grund wurde eine Projektidee erarbeitet, die in dieselbe Themenrichtung geht, da somit auf diesem Wissen aufgebaut werden konnte. Das Projekt ging der Frage nach, wie Produkte der Marke Huawei auf der Online-Shop-Plattform OTTO bewertet werden und welche Kritik von Kund:innen geäußert wird. 

### 2. BIG IDEA Worksheet

Im nächsten Schritt wurde das vom Kurs gestellte Dokument "BIG IDEA Worksheet" genutzt, um das Thema und vor allen Dingen die Zielgruppe des Vortrags zu bestimmmen. Das half dabei die relevantesten Informationen und Gedanken zum Projekt festzuhalten. Bei der weiteren Projektbearbeitung galt dies stets zu berücksichtigen.

### 3. Storyboarding

Auf der virtuellen Whiteboard-Plattform Miro, wurden anschließend Gedanken zum Storyboarding mithilfe der Brainstorming Methode notiert. Die einzelnen Aspekte waren:
- Background
- Analysis
- Recommendation
- Data
- Problem Statement
- Findings

![](miro-board.png)

Daraus ließ sich dann eine Struktur ableiten, die in der Präsentation eingehalten werden sollte. Folglich sollte zunächst das Problem und der Hintergrund beschrieben und dann die Analyse und Ergebnisse präsentiert werden. Am Schluss soll eine Handlungsempfehlung für das fiktive Unternehmen ausgesprochen werden.

### 4. Layout des Dashboards bestimmen

Hierbei wurde sich intensiv mit der Frage beschäftigt: 
> "Wie sollen die vorliegenden Daten visualisiert werden?"

Um eine Antwort auf diese Frage zu finden, konnte die Website von [Data to Viz](https://www.data-to-viz.com/) Abhilfe schaffen. Hier hat man die Möglichkeit, nach den vorliegenden Datentypen zu filtern und bekommt dann passende Visualisierungsformen vorgeschlagen. Eine sehr hilfreiche Plattform, die einen in diesem Zwischenschritt optimal unterstützt. 

Nachdem nun eine Kollektion von möglichen und passenden Darstellungsformen vorlag, wurden diese erstmalig auf Papier skizziert. Diese Skizzen wurden dann final im Dashboard umgesetzt und boten während dem Programmierprozess eine gute Orientierung. 

![](skizzen.jpeg)

### 5. Umsetzung des Dashboards mit Dash und Plotly

Für die technische Umsetzung der Visualisierungen wurde die Python Bibliothek Plotly genutzt. Doch bevor die Diagramme erstellt werden konnten, mussten zunächst die Daten beschaffen werden. Dafür wurden alle Huawei-Produkte, die mindestens drei Rezensionen aufwiesen, in den Produktkategorien: Smartphones, Smartwatches, Tablets und Notebooks auf der Online-Plattform OTTO gescrapt.

:::{note}
Dieser Vorgang fand nicht mithilfe von Python statt, sondern es wurde RStudio und die Programmiersprache R genutzt. Hintergrund dieser Entscheidung war, dass das Programm und die Sprache in früheren Veranstaltungen für denselben Zweck eingesetzt wurden. Daher war die Vorgehensweise bereits bekannt und es konnte auf dem vorhandenen Wissen aufgebaut werden.
:::

Zunächst wurden faktische Daten beschaffen, wie der Produktname, Preis, die Sternebewertung sowie die Weiterempfehlungsrate. Diese numerischen und kategorialen Daten wurden in einem Dataframe abgespeichert und waren die Grundlage für die folgenden Visualisierungsformen: Das Lollipop- und Donut-Diagramm.

Im nächsten Schritt wurden dann die Kommentare der Produkte gescrapt und ebenfalls in einem Dataframe abgespeichert. Diese Daten waren die Grundlage für das Wordcloud-Diagramm. Dabei wurden die Kommentare als ganze Textabschnitte abgespeichert und untersucht, um daraus eine WordCloud zu generieren. 
Für das Balkendiagramm hingegen, mussten die Kommentare für die Häufigkeitsauszählung im Schritt davor tokenisiert werden. Das heißt die Kommentare wurden Wort für Wort voneinander getrennt, sodass im Dataframe in jeder Zelle nur ein einzelnes Wort aufgeführt wurde. Anschließend wurde die Häufigkeit ausgezählt und ebenfalls in einem Dataframe abgespeichert. Mithilfe von Plotly konnte dann ein horizontales Balkendiagramm erstellt werden.

### 6. Erstellung des Reports

Der Report sollte als eine Art Handout denjenigen zur Verfügung stehen, die während der Präsentation nicht anwesend sein konnten. Daher waren ausführlichere schriftliche Erklärungen und Informationen zu den Visualisierungen notwendig, um die Ergebnisse aufzubereiten. Es stellte quasi eine schriftliche Form der Präsentation dar, die man sich im Nachgang jederzeit nochmal durchlesen kann.

### 7. Erstellung der Präsentation

Für die Abschlusspräsentation wurde zunächst [Canva](https://www.canva.com/) genutzt, um ein ansprechendes Design für die Foliensätze zu finden. Später wurde diese nochmal in PowerPoint weiterbearbeitet. Da die Präsentation im fiktiven Szenario an das Unternehmen Huawei gerichtet ist, wurden allgemein dunklere Farben gewählt sowie das akzentreiche Rot aus dem Huawei-Logo. Alle Illustrationen, die verwendet wurden entstammen aus der Open Source Plattform [unDraw](https://undraw.co/). Die Gliederung des Vortrags ergab sich einerseits aus den Kurs-Vorgaben und andererseits aus den Gedanken zum Storyboarding:

1. Hintergrund und Problemstellung
2. Projektziel
3. Vorgehensweise und Metriken
4. Ergebnisse
5. Handlungsempfehlung

Die ersten drei inhaltlichen Punkte sollen zur Einführung ins Unternehmen selbst und dem zugrundeliegenden Projekt dienen. Daher wurde auch das Ziel, die Vorgehensweise und die verwendeten Metriken kurz erläutert, um den Zusammenhang besser nachvollziehen zu können. 
Für die Präsentation der Ergebnisse wurden Screenshots vom Dashboard eingebaut, um den Präsentationsmodus nicht unterbrechen und zu einer anderen Anwendung wechseln zu müssen. Sie entstammen also der eigenen Darstellung.
Allgemein wurde stark darauf geachtet, den Fokus auf das Wesentliche zu lenken, indem PowerPoint-Animationen hinzugefügt wurden. Das ermöglichte es einzelne Stichworte auf den Folien hervorzuheben während die restlichen ausgegraut wurden. Dadurch soll ein besseres Folgen seitens der Zuhörer:innen ermöglicht werden, wie wir es in der Vorlesung bereits thematisiert hatten. Wichtig war auch, dass nicht zu viele Informationen auf den Folien festgehalten wurde, damit das Publikum nicht mit zu vielen Inhalten gleichzeitig konfrontiert wird. Das soll die Konzentration und Aufnahmefähigkeit während der Präsentation gewährleisten.

### 8. Verfassung der Projektdokumentation

Abschließend wurden detaillierte Einzelheiten zur Vorgehensweise in dieser Projektdokumentation festgehalten, um den Aufbau und Hintergrund des Projekts besser nachvollziehen zu können. Dies wurde mithilfe eines Jupyter Books umgesetzt und in Github geteilt, um es öffentlich zugänglich zu machen.