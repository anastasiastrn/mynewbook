# WordCloud

Das WordCloud Diagramm zeigt ein Abbild der verfassten Kommentare zu den Produkten gefiltert nach ihrer Kategorie. In diesem Fall selektiert man nicht mithilfe eines Auswahltools, sondern kann von Tab zu Tab navigieren, um die Ansicht zu wechseln. 

Die Tabs wurden entsprechend des Designs gestaltet. Der aktive und ausgewählte Tab ist mit einer weißen Schriftfarbe und einem hellgrauen Hintergrund gehighlighted. Zudem ist die obere Umrandung des aktiven Tabs in der Kategoriefarbe eingefärbt. Das führt zu Übersichtlichkeit, sodass man jederzeit erkennen kann, in welcher Ansicht man sich befindet. Im Titel der WordCloud wird auch nochmal die Produktkategorie farblich hervorgehoben für eine bessere Übersicht.

Die eingesetzten Farben in der WordCloud wurden anhand der [matplotlib Colormaps](https://matplotlib.org/2.0.2/examples/color/colormaps_reference.html) ausgesucht. Es wurde darauf geachtet, dass die Farben mit dem Design zusammenpassen, jedoch auch viel Kontrast mitbringen, um auf dem dunklen Hintergrund gut lesbar zu sein. Letztendlich fiel die Auswahl auf eine qualitative Colormap namens 'tab20b'.