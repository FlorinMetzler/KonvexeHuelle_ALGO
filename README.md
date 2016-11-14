#ALGO Konvexe Huelle
�bungsaufgabe zur Erstellung einer minimalen Konvexen H�lle um gegebene Punkte

##Main
In dem File Convex.cpp ist die main Methode. Da man prinzipiell einen performance optimierten Modus und einen graphischen step-by-step Modus bereitstellen soll, 
habe ich in der main einen Functionpointer erstellt *loop*, der standardm��ig die Funktion *graphicalLoop* benutzt. �ber die Kommandozeilenangabe *--performance*
kann diesem Funkctionpointer auf die Funktion *performanceOptimizedLoop* zugewiesen werden. 

Die Kommandozeilenargumentauswertung findet in der Funktion *processArguments* statt, ist bisher aber fehleranf�llig also auf korrekte Kommandozeilenargumente achten!

##GUI
In der main wird eine Referenz auf ein Objekt der Klasse *ConvexGUI* erstellt. Diese GUI erh�lt au�erde den Vektor mit den verschiedenen Punkten.
�ber eine *update* Methode wird das Display erneuert, sollte also nach jedem step des Algorithmus aufgerufen werden.

##Struktur
Bis jetzt habe ich die Ordner:
* *InputFiles*, in dem ich Beispieldateien mit Vertice Daten speichere - z.B. *20Points.txt*
* *include*, in dem ich alle Include files verwalte
* *src*

Der *src* Ordner enth�lt seinerseits:
* *model* enth�lt bisher nur die *Point* Klasse aber, beinhaltet alle models des Projekts
* *utils* Sammlung hilfreicher Funktionen, bisher nur *DataInput.h*, welche sich um die generierung/das Auslesen von vertices k�mmert
* *view* enth�lt alle GUI spezifischen files

###Notes:
Derzeit basiert die *ConvexGUI* Klasse auf SFML, aber ich habe ein *I_View* Interface erstellt, k�nnen also problemlos auf eine andere Technologie �berspringen.
