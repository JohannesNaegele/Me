# A guide through my GitHub repositorys and projects
## German

Hier möchte ich eine kleine Übersicht zu allem Möglichen, das ich auf GitHub so mache, erstellen. Mittlerweile verliere ich nämlich langsam selbst manchmal den Überblick über alle Forks und Stars, sodass das langsam mal an der Zeit ist. Außerdem möchte ich auch gerne Links und Projekte weitergeben, die ich für cool und/oder hilfreich befinde.

Falls jemand etwas interessant findet und/oder mehr Informationen haben möchte, macht gerne ne Issue auf oder schreibt ne Mail.

### LaTeX und Publishing

#### Interaktive Dokumente

In der Vergangenheit habe ich mich an ein paar ziemlich abgespaceten (und extrem unnötigen :D) LaTeX-Projekten versucht. Grundsätzlich hat mich immer extrem genervt, dass ich zwar statische Dokumente in LaTeX super erstellen konnte, sobald es aber mit interaktiven Elementen (z. B. Videos, Animationen, ...) sein sollte (wie etwa bei [desmos](https://learn.desmos.com/sliders) oder [GeoGebra](https://www.geogebra.org)), war das die reinste Katastrophe. Das liegt insbesondere daran, dass das PDF-Format für sich hier erhebliche Mängel mitbringt. In der Theorie ist dort nämlich einiges möglich, in der Praxis ist das aber meistens Mist, weil das dann über Adobe Flash und Shockwave etc. funktioniert. Wir erinnern uns: Bitte nicht das! In der Konsequenz funktioniert das dann (wenn überhaupt) nur mit dem Adobe PDF-Reader und nicht auf mobilen Geräten. Sprich: Man macht sich eine Riesenarbeit, nur dass das dann nachher bei der Hälfte der Leser gar nicht ankommt.

Grundsätzlich kommt aber bei LaTeX noch ein weiteres Problem dazu: Was man haben wollen würde, ist ein Dokument, dass zur Runtime gesetzt wird und somit Animationen *beim Abspielen* generiert werden. Das Problem ist nur: Weil LaTeX sequentiell arbeitet und kleine Änderungen im Code weitreichende Umformatierungen zur Folge haben können, müsste dann jedesmal *das komplette Dokument* neu gesetzt werden. Wenn man aber für 25 Frames/s jedes Mal das Dokument neu generieren muss, ist das offensichtlich Quark. 

Was also tun? Interessanterweise gibt es hier sehr unterschiedliche Ansätze, die alle ziemlich unterschiedlich aussehen:

1.  Man ignoriert die Probleme und arbeitet weiter mit einem PDF und mit Pseudointeraktivität
2.  Man baut einen PDF-Website-Hybrid
3.  Man eskaliert komplett und geht auf low-level TeX-Ebene

Was zur Hölle meine ich mit *Pseudointeraktivität*? Der Punkt ist: Wenn ich nicht zur Runtime rendern kann, dann muss ich "interaktive" Elemente eben vorkompilieren. D. h.: Angenommen, ich habe eine Grafik mit Slidern (Schiebereglern) für *n* verschiedene Parameter (z. B. eine Normalverteilungskurve mit μ und σ²), dann mache ich halt ein Gitter mit *n* Dimensionen und diskretisiere das Ganze. Am Ende habe ich dann z. B. 10 mögliche Werte für μ und 1000 mögliche Werte für σ². Für ein hinreichend feines Gitter bietet das also volle Funktionalität (abgesehen von sehr fortgeschrittenen Anwendungen). Am Ende macht man also einfach einen Film, bei dem jedes Frame einem bestimmen Punkt in der Animation entspricht und von dieser angesteuert werden kann. Hier kommt theoretisch noch ein Link hin, wo das dann demonstriert wird. Problematisch ist dabei aber, dass der Speicherbedarf natürlich mit der Anzahl der Möglichkeiten explodiert. Und niemand möchte ein Uniskript mit 1 GB Größe.

Konkret bindet man dann bei Möglichkeit 1. den Slider (oder was auch immer) extern über das [media9](https://ctan.org/pkg/media9)-Package als .swf (Shockwave) ein. Diesen wiederum erstellt man in Adobe Flex mit einer mxml-Datei (Abfuck). Und die Animation macht man dann in LaTeX mit dem [animate](https://ctan.org/pkg/animate)-Package. Das heißt: Ich sage dem animate-Package: Generiere mir bitte 200 Frames, wobei du mir diesen counter hier erhöhst. Ich gehe dann her und bastele eine Bijektion von dem counter, sodass dieser eindimensionale 

#### Videos & Grafiken

- manim
- TikZ

### Julia

###

## English
Will be updated soon, hopefully.
