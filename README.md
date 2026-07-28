## fork() in C

Hier ist der Beispielcode für die Nutzung von `fork()`:

```c
#include <stdio.h>
#include <unistd.h> // Hier drin steckt fork()

int main() {
    pid_t pid;

    printf("Vor dem fork... (Das druckt nur das Original)\n");

    // Hier passiert die Spaltung!
    pid = fork();

    if (pid < 0) {
        // Fehlerfall
        fprintf(stderr, "Fork fehlgeschlagen!");
        return 1;
    } 
    else if (pid == 0) {
        // Dieser Block wird NUR vom Kindprozess ausgeführt
        printf("Hallo, ich bin das Kind! Mein fork-Rückgabewert ist: %d\n", pid);
    } 
    else {
        // Dieser Block wird NUR vom Elternprozess ausgeführt
        printf("Hallo, ich bin das Elternteil! Das Kind hat die PID: %d\n", pid);
    }

    printf("Dieser Text wird von BEIDEN gedruckt!\n");
    return 0;
}
```
Wieso wird bei pid = fork(); derselbe Befehl rechts vom = nur vom Elternprozess ausgeführt und links vom = von beiden Prozessen ausgeführt? Das ist etwas willkürluch und nicht klar definiert oder getrennt. Aufgrund dieser Bedeutung sind zum Beispiel unterschiedliche Interpretationen oder Ausführungen denkbar. Es kann zum Beispiel sein, dass beide Prozesse mit einer unterschiedlichen pid weiter ausgeführt werden, nämlich jeder Prozess mit der pid, die er ab dieser Ausführung selber hat. Es kann aber auch sein, dass beide Prozesse mit dieser eindeutigen pid weiter ausgeführt werden, die fork() für alle Prozesse links vom = eindeutig zurückgibt.

## Ideen

Blinker vorne rollt und der Blinker hinten nicht 

Nicht-trivialer Hitzeverlauf als Funktion zum Backen im Ofen

Hitze-Ausbreitungsprofile im Ofen zur Analyse nach dem Essen und zur Anpassung für zukünftige Backvorgänge

Einen Abfluss in den Behälter für den WC-Reiniger an der Wand

Eine mit KI trainierte Jura-Box zur Ermittlung des Rechts für Rechtsstreitigkeiten. Es wird viele einfachere Fälle geben, bei denen eine komplexe Analyse durch Juristen gar nicht erforderlich ist. Diese Jura-Box hat als oberstes Ziel den Schutz des Lebens durch die Gesetze des Landes und vertritt keine wirtschaftlichen oder politischen Interessen, die nur von kurzer Dauer sind.

Wieso braucht es die Wahrscheinlichkeitsfunktion einer Zufallsvariablen? Davon abgesehen ist die Wahrscheinlichkeitsfunktion fortlaufend auch in den Sprungstellen als durchgehender Graf darzustellen mit Werten von 0 bis 1. So entspricht es der vollständigen Beschreibung. Wird sie dann um -90° gedreht, erleichtert dies dem Betrachter die Zuordnung zu einer der bekannten Verteilungen.

Nicht Granatapfel, sondern Kernapfel.

Automatische Retourenerkennung in Umsätzen und Hinweis bei Ablauf von Retourenfenstern in einer mobilen App.

Erweiterung des OBD-Standards zur Visualisierung von CAN-Bus-Signalen in Echtzeit.

Die Zyklomatische Komplexität (ZK) eines Softwareprojekts gibt an, an welcher Stelle oder Stellen im Code die Software besonders fehleranfällig sein könnte oder ist. In der Praxis muss das aber nicht damit zusammenhängen, wo bisher überall Softwarefehler wirklich aufgetreten sind oder auftreten. Mit einer mathematischen Wahrscheinlichkeitsverteilung, die die ZK mit betrachtet, lässt sich eine Korrelation zur ZK nur schwer durchführen. Das liegt daran, dass Software so individuell ist und unter so vielen Einflussfaktoren steht, die nicht mehr wirklich berechenbar sind, wie die Umgebung, die Benutzer, die sich ändernden Anforderungen und so weiter.

Salzwasser aus dem Meer zum Befüllen der großen Wasserlöcher unter dem Erdboden.

Das Grillen über Feuer mit Flammen ist besser für das Fleisch als die gleichmäßige Erhitzung über einem Kohlenfeuer oder in einem Ofen.

BaseModel von pydantic sollte PydanticBase heißen.

Ist Druck in der Realität ideal gleichmäßig, zum Beispiel bei einem Springbrunnen bezogen auf die ganze relativ kleine Kreisfläche, durch die das Wasser hochgedrückt wird? Nein. Was macht der Druck mit sich selbst? Der Druck mit sich selbst drückt sich selber weg. Er kann nicht ideal gleichmäßig sein. Lineare Betrachtungen oder Modelle sind daher einfach ausgeschlossen. Ganz anschaulich sieht man das an einem Springbrunnen.

Lichtgeschwindigkeit breitet sich in demselben Medium nach der Konstanten c ja eigentlich immer gleich schnell aus. Das entspricht aber nicht der Realität. Die Lichtgeschwindigkeit breitet sich auch im selben Medium nicht immer gleich schnell aus. Interessant ist die Frage, mit welcher Abweichung sich das Licht im selben Medium nicht gleich schnell ausbreitet. Mit welcher Verteilung oder welchen Verteilungen kann das in Abhängigkeit von den unterschiedlichen Medien beschrieben werden? Und wie sehen die maximale Abweichung und die zu erwartende Abweichung wirklich aus? 

$E = m c^2$ stimmt, aber $c$ ist nicht konstant und $m$ ist immer in Abhängigkeit des inhomogenen Gravitationsfeldes zu betrachten. Damit ist $E$ nicht trivial berechenbar. Das verwundert aber nicht, da in der Praxis die Energie erst wirklich dann nicht mehr wirkt, wenn sie nicht mehr wirken kann.

Depression ist die kontinuierliche Erfahrung von Negierung einer oder mehrerer Möglichkeiten des Lebens
